# GPU passthrough

For VMs | For containers




### GPU passthrough for containers
lxd cuda passthrought
https://discuss.linuxcontainers.org/t/nvidia-cuda-inside-a-lxd-container-ubuntu-20-04/11223
NVidia CUDA inside a LXD container Ubuntu 20.04

https://ubuntu.com/blog/nvidia-cuda-inside-a-lxd-container
GPU inside a container
With containers, rather than passing a raw PCI device and have the container deal with it (which it can’t), we instead have the host setup with all needed drivers and only pass the resulting device nodes to the container.



### PCI/GPU passthrough for VMs

[https://wiki.archlinux.org/title/QEMU/Guest_graphics_acceleration#SR-IOV](https://wiki.archlinux.org/title/QEMU/Guest_graphics_acceleration#SR-IOV)
[https://wiki.archlinux.org/title/QEMU/Guest_graphics_acceleration#Virgil3d_vi...](https://wiki.archlinux.org/title/QEMU/Guest_graphics_acceleration#Virgil3d_virtio-gpu_paravirtualized_device_driver)

#### PCI/GPU passthrough for VMs - 3.23+ /post
[PCI/GPU passthrough for VMs - 3.23+](https://discuss.linuxcontainers.org/t/pci-gpu-passthrough-for-vms-3-23/7194)
https://discuss.linuxcontainers.org/t/pci-gpu-passthrough-for-vms-3-23/7194

I have a use case where I need to manage containers and VMs on a cluster in an integrated fashion. Some of the VMs need access to a raw NVIDIA GPU device (without there being any drivers on the LXD server).
I see that 3.20+ brings the ability to configure a physical-nic device (using QEMU PCI passthrough) for a VM, and was wondering if similar capability is available or forthcoming for a generic (non-NIC) device.

xxxxxxxxxxxxx

After doing the usual IOMMU and vfio stuff (to isolate the desired PCI device from the host), the device can be passed through to the host as shown in the commands below:

```
akriadmin@c4akri01:~$ lxc profile show vm
config:
  raw.qemu: -device vfio-pci,host=41:00.0
description: LXD profile for virtual machines
devices: {}
name: vm
used_by: []
```

xxxxxxxxxxxxxxx

PCI passthrough via vfio is what I did as well.

If your card is in use by another driver (for example in case of a GPU) you have to unbind it first. For GPUs add the following to `/etc/default/grub` (NOTE: The ID is the `<vendor>:<product>` combination you can find with `lspci -nn`)

`GRUB_CMDLINE_LINUX_DEFAULT="video=vesafb:off,efifb:off vfio-pci.ids=1002:67c7,1002:aaf0"`

Where the PCI ids are the ones of your GPU. In this case the GPU has also an audio PCI device which has to be passed to VFIO within the same group, otherwise Qemu will fail to forward. Also add

`vfio-pci  vfio_iommu_type1`

to your `/etc/modules` and create `/etc/modprobe.d/vfio.conf` with the following content

`options vfio-pci ids=1002:67c7,1002:aaf0 softdep radeon pre: vfio-pci softdep amdgpu pre: vfio-pci softdep nouveau pre: vfio-pci softdep drm pre: vfio-pci`

Now run

`$ update-grub $ update-initramfs -u -k all`

and finally reboot the system. Once back up the PCI device can now be forwarded via a `raw.qemu: -device vfio-pci,host=01:00.0`.

xxxxxxxxxxxxxxxxxx





### [Совместный ресурс видеокарты.](https://www.linux.org.ru/forum/development/17459178) LOR /post

 [passthrough](https://www.linux.org.ru/tag/passthrough), [видеокарта](https://www.linux.org.ru/tag/%D0%B2%D0%B8%D0%B4%D0%B5%D0%BE%D0%BA%D0%B0%D1%80%D1%82%D0%B0), [виртуализация](https://www.linux.org.ru/tag/%D0%B2%D0%B8%D1%80%D1%82%D1%83%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F), [виртуальная машина](https://www.linux.org.ru/tag/%D0%B2%D0%B8%D1%80%D1%82%D1%83%D0%B0%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F%20%D0%BC%D0%B0%D1%88%D0%B8%D0%BD%D0%B0)
Имеем следующее: мощный комп (i9, 128 гб) с quadro 6000. Есть потребность дать разным пользователям доступ к ресурсу видеокарты.

В целом, нарезаем пользовательских логинов, проверяем права и живём в шоколаде. Но эксплуатационно это скорее всего будет требовать много внимания от всех, да и свобода разработки у пользователей будет упираться в их права.

Хочется каждому дать по виртуалке, и уже оттуда доступ ресурсу видюхи. Очевидно приходит в голову следующее: мастер-виртуалка в которую проброшена видеокарта, у каждого пользователя по своей виртуалке, общение с мастером через брокер или ещё каким-нибудь механизмом отправки заданий.

Количество пользователей: 3-5, но раз в пару месяцев будут меняться.

Вопрос: может быть есть что по-умнее, или вообще какое-нибудь готовое/конкретное решение?

Dispetcher14](https://www.linux.org.ru/people/Dispetcher14/profile)  21.12.23  


> но насколько могу понять из рекламных брошюр nVidia, quadro rtx 6000 умеет в аппаратную виртуализацию. Возможно, тебе будет достаточно настроить sr-iov, и отдать виртуальные устройства виртуалкам? Правда я не в курсе, можно ли в этом случае контролировать, сколько именно ресурса доступно каждой ВМ, и чтопроисходит с видеопамятью.




> Nvidia да и другие карты часто пробрасывают в докер, что по сути точно такое же разделение на пользователей.
