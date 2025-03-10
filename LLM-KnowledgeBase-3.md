# База знаний по AI, NLP и LLM

Эта база знаний создана для исследовательской команды, чтобы обеспечить удобный доступ к ресурсам по искусственному интеллекту (AI), обработке естественного языка (NLP) и большим языковым моделям (LLM). Ссылки организованы иерархически: от базовых концепций до практических приложений и дополнительных ресурсов. Каждый раздел сопровождается кратким описанием, а каждая ссылка — аннотацией из 1-5 предложений для быстрого понимания содержания.

---

## 1. Основные концепции
Этот раздел включает вводные материалы о больших языковых моделях, их архитектурах и ключевых механизмах, таких как внимание и Transformer. Он предназначен для тех, кто только начинает изучать LLM или хочет освежить базовые знания.

### 1.1. Введение в LLM
- **[Введение в большие языковые модели (LLM)](https://www.youtube.com/watch?v=HEgoPEppu7A)**  
  Вводное видео объясняет, что такое большие языковые модели, как они работают и где применяются. Подходит для новичков, желающих понять основы LLM без глубокого погружения в технические детали.
- **[Введение в большие языковые модели от Andrej Karpathy](https://www.youtube.com/watch?v=NhPHi2Uw9e8)**  
  Лекция от известного эксперта Андрея Карпатого, где он доступно объясняет принципы работы LLM. Отличный ресурс для понимания технической основы и истории развития языковых моделей.
- **[Введение в большие языковые модели (Google Cloud Skills Boost)](https://cloudskillsboost.google/course_templates/539)**  
  Курс от Google Cloud, который охватывает основы LLM и их применение в реальных задачах. Идеально для тех, кто хочет начать с теоретической базы и практических примеров.
- **[Языковые модели для чайников: просто и полезно про BERT и GPT](https://www.youtube.com/watch?v=KRiUvBEwmmU)**  
  Видео-вебинар 2021 года, объясняющий основы BERT и GPT простым языком. Отличный старт для начинающих, с акцентом на интуитивное понимание ключевых концепций.

### 1.2. Ключевые архитектуры и механизмы
- **[Архитектура Encoder-Decoder (Google Cloud Skills Boost)](https://cloudskillsboost.google/course_templates/543)**  
  Курс подробно разбирает архитектуру Encoder-Decoder, лежащую в основе многих современных LLM. Подходит для понимания, как модели обрабатывают входные и выходные данные.
- **[Механизм внимания (Google Cloud Skills Boost)](https://cloudskillsboost.google/course_templates/537)**  
  Курс объясняет механизм внимания, ключевой элемент Transformer-моделей, обеспечивающий их эффективность. Полезен для тех, кто хочет углубиться в технические детали работы LLM.
- **[Модели Transformer и модель BERT (Google Cloud Skills Boost)](https://cloudskillsboost.google/course_templates/538)**  
  Курс охватывает архитектуру Transformer и её реализацию в модели BERT, с примерами применения. Отличный ресурс для изучения основ современных языковых моделей.
- **[Информация о технологии MoE – Mixture of Experts](https://huggingface.co/blog/moe)**  
  Статья на блоге Hugging Face объясняет концепцию Mixture of Experts (MoE), используемую в некоторых передовых LLM. Полезна для понимания новых подходов к масштабированию моделей.
- **[What is Mamba?](https://medium.com/@jelkhoury880/what-is-mamba-845987734ffc)**  
  Статья на Medium описывает модель Mamba, её особенности и отличия от традиционных архитектур. Интересный обзор для тех, кто следит за новыми разработками в области LLM.

---

## 2. Обучение и дообучение LLM
Раздел посвящен созданию, обучению и тонкой настройке языковых моделей. Здесь собраны руководства, инструменты и методы, такие как fine-tuning и RLHF, для адаптации моделей под конкретные задачи.

- **[How to Train a Custom LLM Embedding Model](https://dagshub.com/blog/how-to-train-a-custom-llm-embedding-model/)**  
  Руководство по обучению пользовательской модели эмбеддингов для LLM, полезное для настройки моделей под конкретные задачи. Статья объясняет процесс шаг за шагом, включая выбор данных и инструментов.
- **[Training LLaMa3-8B for Any Language](https://github.com/AI-Commandos/LLaMa2lang)**  
  Репозиторий с удобными скриптами для дообучения LLaMa3-8B на любой язык, кроме английского. Подходит для разработчиков, желающих адаптировать модель под свои языковые нужды.
- **[Официальная документация OpenAI по fine-tuning моделей](https://platform.openai.com/docs/guides/fine-tuning)**  
  Подробная документация от OpenAI о процессе дообучения их моделей для улучшения производительности. Идеальный стартовый ресурс для работы с API OpenAI и fine-tuning.
- **[Fine-Tuning in Deep Learning](https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning))**  
  Статья Википедии объясняет концепцию fine-tuning в контексте глубокого обучения. Хороший теоретический обзор для понимания различий между обучением с нуля и дообучением.
- **[Инструмент для дообучения AI моделей с помощью промптов](https://ai.sber.ru/post/predstavlen-instrument,-pozvolyaushchij-doobuchat-ai-modeli-pro-promptu)**  
  Статья от Сбера описывает инструмент для дообучения моделей через промпты, упрощающий процесс адаптации. Полезна для исследователей, ищущих практичные решения.
- **[GPT LLM Trainer](https://github.com/mshumer/gpt-llm-trainer)**  
  Репозиторий с инструментом для тренировки GPT и других LLM, упрощающим процесс обучения. Подходит для разработчиков, желающих быстро протестировать свои идеи.
- **[Документация по дообучению модели Mistral 7B](https://docs.mistral.ai/capabilities/finetuning/)**  
  Официальная документация Mistral AI описывает, как дообучать модель Mistral 7B для конкретных задач. Полезный ресурс для работы с этой популярной моделью.
- **[Настройка и обучение языковой модели с LoRA и PEFT](https://cloud.ru/docs/aicloud/mlspace/concepts/tutorials/llm/tutorials__guides__llm_install.html)**  
  Руководство от Cloud.ru по настройке и дообучению LLM с использованием методов LoRA и PEFT. Отлично подходит для оптимизации обучения на ограниченных ресурсах.
- **[StackLLaMA: практическое руководство по обучению LLaMA с RLHF](https://habr.com/ru/companies/wunderfund/articles/731128/)**  
  Статья на Хабре объясняет, как дообучать LLaMA с использованием RLHF для улучшения поведения модели. Практическое руководство с примерами и пояснениями.

---

## 3. Эмбеддинги и RAG
Этот раздел охватывает работу с векторными представлениями текста (эмбеддингами) и технологию Retrieval-Augmented Generation (RAG), которая улучшает LLM за счет внешних данных.

### 3.1. Эмбеддинги
- **[Документация об Embeddings (OpenAI)](https://openai-docs.ru/docs/guides/embeddings)**  
  Русскоязычная документация OpenAI объясняет, как использовать эмбеддинги для представления текста. Полезна для понимания основ работы с векторами в задачах NLP.

### 3.2. Retrieval-Augmented Generation (RAG)
- **[Добавление собственных данных в LLM с помощью RAG](https://habr.com/ru/companies/wunderfund/articles/779748/)**  
  Статья на Хабре объясняет, как технология RAG позволяет интегрировать внешние данные в LLM. Практическое руководство для улучшения моделей с помощью баз знаний.
- **[Архитектура RAG: полный гайд](https://habr.com/ru/companies/raft/articles/791034/)**  
  Полное руководство по архитектуре RAG, описывающее её принципы и применение. Отличный старт для тех, кто хочет глубоко понять эту технологию.
- **[Архитектура RAG: часть вторая — Advanced RAG](https://habr.com/ru/companies/raft/articles/818781/)**  
  Продолжение гайда по RAG с углубленными техниками и примерами. Полезно для исследователей, уже знакомых с основами RAG.
- **[RAG from Scratch](https://github.com/langchain-ai/rag-from-scratch)**  
  Репозиторий с руководством и красивыми схемами по созданию RAG-системы с нуля. Отлично подходит для разработчиков, желающих понять внутреннюю работу RAG.
- **[Полное руководство по оценке компонентов системы RAG](https://habr.com/ru/articles/860390/)**  
  Статья на Хабре о методах оценки эффективности RAG-систем. Полезна для анализа качества интеграции внешних данных в LLM.
- **[Построение базы знаний компании и поиска документов на LLM и RAG](https://habr.com/ru/companies/raft/articles/863888/)**  
  Практическая статья о создании корпоративной базы знаний с использованием LLM и RAG. Хороший пример реального применения технологии.
- **[Нам нужен RAG, вам нужен RAG](https://habr.com/ru/articles/864776/)**  
  Статья на Хабре объясняет, зачем и как интегрировать RAG в системы с LLM. Подходит для понимания практической ценности технологии.
- **[Local Agentic RAG with Llama3](https://www.youtube.com/watch?v=u5Vcrwpzoz8)**  
  Видео демонстрирует, как использовать RAG с Llama3 для работы с локальными знаниями. Полезно для практического освоения технологии.
- **[Реализация RAG на основе GigaChat](https://www.youtube.com/watch?v=kxQ3qfryEHE)**  
  Видео-руководство по реализации RAG с GigaChat для поиска и генерации ответов. Практический пример с российской моделью.

---

## 4. Развертывание LLM
Раздел посвящен инструментам и платформам для развертывания языковых моделей — как в облаке, так и локально. Здесь вы найдете решения для инференса и управления моделями.

### 4.1. Облачные решения
- **[Paperspace](https://paperspace.com)**  
  Облачный сервис, предоставляющий доступ к мощным GPU для задач машинного обучения, включая работу с LLM. Подходит для тех, кто ищет вычислительные ресурсы без локального оборудования.
- **[Nebius Platform](https://studio.nebius.ai/)**  
  Платформа для работы с ИИ-моделями, совместимая с API OpenAI, для инференса популярных моделей. Удобна для разработчиков, работающих с облачным доступом.
- **[Платформа OpenAI](https://platform.openai.com/)**  
  Веб-сайт OpenAI предоставляет доступ к API и инструментам для интеграции их моделей в проекты. Базовый ресурс для работы с облачными LLM.

### 4.2. Локальные решения
- **[Ollama](https://ollama.ai/)**  
  Проект для локального запуска языковых моделей с простым интерфейсом и настройкой. Идеально для тех, кто хочет работать с LLM без интернета.
- **[llama.cpp](https://github.com/ggerganov/llama.cpp)**  
  Высокоэффективная реализация моделей LLaMA на C++ для локального использования. Подходит для разработчиков, желающих оптимизировать производительность на своих устройствах.
- **[Text-Generation-WebUI](https://github.com/oobabooga/text-generation-webui)**  
  Веб-интерфейс на базе Gradio для генерации текста с LLM, работающий локально. Удобен для тестирования моделей без сложной настройки.
- **[GPT4All](https://github.com/nomic-ai/gpt4all)**  
  Локальная платформа для работы с GPT-подобными моделями, ориентированная на приватность и простоту. Отличный выбор для оффлайн-применений.
- **[Jan.ai](https://jan.ai/)**  
  Открытый проект, альтернатива ChatGPT, работающий оффлайн с поддержкой популярных моделей. Подчеркивает приватность и локальное хранение данных.
- **[vLLM](https://vllm.ai/)**  
  Открытая библиотека для ускорения инференса LLM, улучшающая эффективность использования памяти. Полезна для оптимизации локального развертывания.

---

## 5. Приложения
Этот раздел охватывает практическое применение LLM в реальных задачах, таких как создание чат-ботов и распознавание речи. Здесь собраны платформы, инструменты и примеры.

### 5.1. Чат-боты и виртуальные ассистенты
- **[Dialogflow](https://cloud.google.com/dialogflow)**  
  Платформа от Google для разработки чат-ботов и виртуальных ассистентов с NLP-технологиями. Подходит для создания контекстных диалоговых систем.
- **[Rasa Platform](https://rasa.com/product/rasa-platform/)**  
  Открытая платформа Rasa для создания контекстных AI-ассистентов и чат-ботов. Идеальна для разработчиков, желающих полный контроль над системой.
- **[Документация Rasa по подготовке данных для NLU](https://rasa.com/docs/rasa/nlu-training-data/)**  
  Руководство по созданию обучающих данных для обработки естественного языка в Rasa. Полезно для настройки точности распознавания намерений.
- **[Just AI Conversational Platform](https://just-ai.com/platforma-jaicp)**  
  Платформа JAICP для создания чат-ботов и голосовых помощников с акцентом на диалоговые системы. Подходит для бизнеса и разработчиков.
- **[SaluteBot от Сбера](https://developers.sber.ru/docs/ru/salutebot/overview)**  
  Платформа от Сбербанка для создания чат-ботов с интеграцией LLM. Хороший пример отечественного решения для диалоговых систем.
- **[Разработка Telegram-бота для доступа к ChatGPT](https://habr.com/ru/articles/860572/)**  
  Статья на Хабре о создании Telegram-бота как интерфейса к LLM, включая ChatGPT. Практический пример с открытым кодом.

### 5.2. Распознавание речи
- **[Whisper Model](https://github.com/openai/whisper)**  
  Модель Whisper от OpenAI для автоматического распознавания речи с высокой точностью. Отличный инструмент для обработки аудиоданных.
- **[Whisper's Transcription + Pyannote's Diarization](https://github.com/openai/whisper/discussions/264)**  
  Обсуждение на GitHub о комбинации Whisper с Pyannote для распознавания речи и разделения спикеров. Полезно для сложных аудиоаналитических задач.
- **[Shopot.ai](https://shopot.ai)**  
  Российский сервис для обработки аудио и распознавания речи, альтернативный Whisper. Подходит для локальных решений с акцентом на рынок СНГ.

### 5.3. Фреймворки для приложений
- **[LangChain](https://github.com/langchain-ai/langchain)**  
  Фреймворк для разработки приложений с LLM, упрощающий интеграцию моделей с данными. Широко используется для создания контекстных систем.

---

## 6. Ресурсы
Этот большой раздел включает дополнительные материалы: туториалы, курсы, статьи, видео и проекты. Здесь вы найдете всё для углубленного изучения и практической работы с LLM.

### 6.1. Туториалы и документация
- **[Mistral 7B Tutorial on DataCamp](https://www.datacamp.com/tutorial/mistral-7b-tutorial)**  
  Туториал по использованию и дообучению модели Mistral 7B, с практическими примерами. Подходит для начинающих и опытных пользователей.
- **[Документация по API OpenAI](https://platform.openai.com/docs/api-reference)**  
  Полная документация по API OpenAI для интеграции их моделей в проекты. Незаменимый ресурс для разработчиков.
- **[Руководство по промпт-инжинирингу](https://www.promptingguide.ai/ru)**  
  Подробное руководство по созданию эффективных промптов для LLM. Полезно для улучшения качества генерации текста.
- **[Все, что нужно знать для разработки с использованием LLM](https://habr.com/ru/articles/775842/)**  
  Обзорная статья на Хабре с основами разработки приложений на базе LLM. Хороший старт для практического применения.

### 6.2. Курсы и образовательные материалы
- **[Введение в Generative AI Studio (Google Cloud Skills Boost)](https://cloudskillsboost.google/course_templates/544)**  
  Курс по использованию Generative AI Studio для работы с генеративными моделями. Подходит для изучения облачных инструментов Google.
- **[AI Hub Koss](https://aihubkoss.com)**  
  Крупнейшее сообщество по ИИ в СНГ, предлагающее курсы по нейросетям и LLM. Отличный ресурс для русскоязычных исследователей.
- **[Large Language Models — Курс от DeepSchool](https://deepschool.ru/llm)**  
  Курс по большим языковым моделям с акцентом на теорию и практику. Подходит для углубленного изучения LLM.

### 6.3. Видео и лекции
- **[Developing an LLM: Building, Training, Finetuning](https://www.youtube.com/watch?v=kPGTx4wcm_w)**  
  Видео о создании, обучении и дообучении LLM с практическими примерами. Полезно для полного цикла разработки моделей.
- **[Делаем GPT ассистента за 3 минуты!](https://www.youtube.com/watch?v=iHtWFGWkpzg)**  
  Видео показывает, как быстро создать GPT-ассистента через API OpenAI и платформу. Отличный пример для быстрого старта.
- **[Fine-Tuning, RAG, Llama, Prompt-Engineering, LLM-Arenas](https://www.youtube.com/watch?v=sbMzUOXcyWw)**  
  Обзор актуальных тем в LLM: дообучение, RAG, Llama и промпт-инжиниринг. Хорошее видео для общего понимания трендов.
- **[Новый генератор промптов от Anthropic](https://www.youtube.com/watch?v=6VlQHdF8gz0)**  
  Видео о новом инструменте Anthropic для автоматизации промптов, упрощающем работу с LLM. Интересно для оптимизации взаимодействия с моделями.
- **[Мастерство LLM: Развертывание и использование локально](https://www.youtube.com/watch?v=zliq9vEz4Dw)**  
  Лекция Игоря Акимова о локальном развертывании LLM, с практическими советами. Полезна для оффлайн-применений.
- **[Create a LOCAL Python AI Chatbot In Minutes Using Ollama](https://www.youtube.com/watch?v=d0o89z134CQ)**  
  Видео-туториал по созданию локального чат-бота на Python с Ollama. Простой и быстрый старт для разработчиков.
- **[Как работает команда NLP Research после GPT-4](https://www.youtube.com/watch?v=-PXV3Nq6YVw)**  
  Лекция Даниила Гаврилова из Тинькофф о работе с NLP после появления GPT-4. Интересный взгляд на эволюцию исследований.

### 6.4. Статьи и обзоры
- **[OpenAI о новых моделях ИИ, которые умеют рассуждать](https://habr.com/ru/companies/bothub/articles/843236/)**  
  Статья на Хабре о последних моделях OpenAI с улучшенными возможностями рассуждения. Полезна для отслеживания новинок.
- **[Лучшие крупные языковые модели в ноябре 2024](https://habr.com/ru/articles/866932/)**  
  Обзор самых эффективных LLM по состоянию на ноябрь 2024 года. Хороший способ узнать о текущих лидерах.
- **[Возможности LLM и RAG на примере бота поддержки](https://habr.com/ru/companies/vk/articles/866906/)**  
  Статья от VK о создании бота поддержки с использованием LLM и RAG. Практический кейс с реальным применением.
- **[Ускорение LLM: универсальные методы](https://habr.com/ru/companies/yandex/articles/878230/)**  
  Статья от Яндекса о методах оптимизации скорости работы LLM. Полезна для повышения производительности моделей.
- **[DeepSeek R1: модель с производительностью o1](https://habr.com/ru/articles/877090/)**  
  Обзор модели DeepSeek R1, её сравнение с o1 от OpenAI и инструкции по использованию API. Интересно для анализа новых игроков на рынке.
- **[LLM Field Landscape](https://habr.com/ru/articles/814665/)**  
  Обзор актуальных концепций, задач и исследований в области LLM на 2024 год. Отличный ресурс для понимания текущего состояния отрасли.
- **[Как сделать контекстное окно на 100K](https://habr.com/ru/articles/752062/)**  
  Статья на Хабре о расширении контекстного окна LLM до 100 тысяч токенов. Полезна для работы с длинными текстами.
- **[Кто такие LLM-агенты и что они умеют?](https://habr.com/ru/companies/ods/articles/776478/)**  
  Объяснение концепции LLM-агентов и их возможностей в задачах автоматизации. Хороший старт для изучения агентных систем.
- **[Распознавание речи и генерация субтитров с Whisper](https://habr.com/ru/companies/ods/articles/692246/)**  
  Статья о применении Whisper для распознавания речи и создания субтитров. Практическое руководство с примерами.

### 6.5. Инструменты и проекты
- **[Справочник по выбору GPU для работы с Llama](https://vc.ru/ai/881777-spravochnik-po-vyboru-gpu-dlya-raboty-s-bolshimi-yazykovymi-modelyami-llama)**  
  Статья на vc.ru с рекомендациями по выбору GPU для LLM, таких как Llama. Полезна для планирования аппаратного обеспечения.
- **[Token Count Utility](https://github.com/felvin-search/token-count)**  
  Утилита на GitHub для подсчета токенов в тексте, важная при работе с LLM. Простой инструмент для оптимизации ввода.
- **[Awesome LLM Agents](https://github.com/kaushikb11/awesome-llm-agents)**  
  Подборка лучших фреймворков и инструментов для разработки LLM-агентов. Отличный ресурс для создания автономных систем.
- **[Awesome LLM JSON List](https://github.com/imaurer/awesome-llm-json)**  
  Список ресурсов для генерации структурированных данных (JSON) с помощью LLM. Полезен для задач парсинга и обработки данных.
- **[Hugging Face Models](https://huggingface.co/models)**  
  Каталог доступных моделей на Hugging Face для скачивания и использования. База для экспериментов с различными LLM.
- **[Together.ai](https://www.together.ai/)**  
  Облачная платформа для оптимизированного запуска LLM, удобная для разработчиков. Подходит для масштабируемых решений.
- **[Google Colab](https://colab.google/)**  
  Бесплатный облачный сервис от Google с доступом к GPU и TPU для работы с LLM. Идеален для прототипирования и обучения моделей.
- **[Groq](https://groq.com)**  
  Сервис для инференса открытых моделей по протоколу OpenAI, существующий давно и проверенный временем. Хороший выбор для облачного доступа.
- **[LLM Pricing](https://llm-price.com/)**  
  Сайт, сравнивающий стоимость использования различных LLM от официальных провайдеров. Полезен для планирования бюджета проектов.
- **[Open WebUI](https://openwebui.com)**  
  Веб-интерфейс для взаимодействия с языковыми моделями, упрощающий их использование. Подходит для тестирования и демонстраций.

---

Эта база знаний охватывает все предоставленные ссылки, обеспечивая структурированный доступ к информации и помогая исследовательской команде эффективно работать с темами AI, NLP и LLM.