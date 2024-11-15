---
aliases:
  - Diarization (AI)
  - Speaker identification (Diarization)
  - Диаризация
  - Разделение Спикеров (ASR)
  - Diarization (Speaker identification)
up:
  - [[AI-concept]]
---
up: [[AI-concept]]  up: [[ASR|ASR - Automatic Speech Recognition]]
# Diarization
Aliases: Диаризация, разделение спикеров, speaker identification
Transcription and diarization (speaker identification)

https://en.wikipedia.org/wiki/Speaker_diarisation
https://ru.wikipedia.org/wiki/Диаризация 

Диаризация — разделение спикеров. Понадобится при необходимости вычленить из аудиопотока определенного человека или добавить имя говорящего к субтитрам.  ( [link](https://habr.com/ru/companies/ods/articles/692246/)

> The term voice recognition or speaker identification refers to identifying the speaker, rather than what they are saying. [wiki.../Speech_recognition](https://en.wikipedia.org/wiki/Speech_recognition)


> **voice recognition** can refer to speaker recognition or speech recognition.  (https://en.wikipedia.org/wiki/Speaker_recognition)

Из википедии:
pyAudioAnalysis (апдейт хотя бы в 2022)

## Diarization using whisper + x 
> Whisper не был на это натренирован, но вот здесь этот вопрос обсуждают и делятся наработками (colab).  (from: https://habr.com/ru/companies/ods/articles/692246/)

#### Whisper's transcription plus Pyannote's Diarization
https://github.com/openai/whisper/discussions/264

**Update** - [@johnwyles](https://github.com/johnwyles) added HTML output for audio/video files from Google Drive, along with some fixes.

Using the new word-level timestamping of Whisper, the transcription words are highlighted as the video plays, with optional autoscroll. And the display on small displays is improved.
Moreover, the model is loaded just once, thus the whole thing runs much faster now. You can also hardcode your Huggingface token.

xxxx

Andrej Karpathy [suggested](https://twitter.com/karpathy/status/1574476200801538048?s=20&t=s5IMMXOYjBI6-91dib6w8g) training a classifier on top of [**openai/whisper**](https://github.com/openai/whisper) model features to identify the speaker, so we can visualize the speaker in the transcript. But, as [pointed out](https://twitter.com/tarantulae/status/1574493613362388992?s=20&t=s5IMMXOYjBI6-91dib6w8g) by Christian Perone, it seems that features from whisper wouldn't be that great for speaker recognition as its main objective is basically to ignore speaker differences.

In [**`Majdoddin/nlp`**](https://github.com/Majdoddin/nlp), I use [**`pyannote-audio`**](https://github.com/pyannote/pyannote-audio), a speaker diarization toolkit by Hervé Bredin, to identify the speakers, and then match it with the transcriptions of Whispr. Check the result [**here**](https://majdoddin.github.io/dyson.html).

**Edit:** To make it easier to match the transcriptions to diarizations by speaker change, Sarah Kaiser [suggested](https://github.com/openai/whisper/discussions/264#discussioncomment-3825375) runnnig the pyannote.audio first and then just running whisper on the split-by-speaker chunks.  
For sake of performance (and transcription quality?), we attach the audio segements into a single audio file with a silent spacer as a seperator, and run whisper on it. Enjoy it!

(For sake of performance , I also tried attaching the audio segements into a single audio file with a silent -or beep- spacer as a seperator, and run whisper on it see it on [colab](https://colab.research.google.com/drive/1HuvcY4tkTHPDzcwyVH77LCh_m8tP-Qet?usp=sharing). It [works](https://majdoddin.github.io/lexicap.html) on some audio, and fails on some -e.g. Dyson's Interview. The problem is, whisper does not reliably make a timestap on a spacer. See the discussions [#139](https://github.com/openai/whisper/discussions/139) and [#29](https://github.com/openai/whisper/discussions/29))



