
# RAG
Retrieval Augmented Generation (RAG)
see [[Embeddings]]

https://www.promptingguide.ai
https://www.promptingguide.ai/techniques/rag




#### важные доки

##### Типы RAG - Обзор
See: [[Types-RAG-Oview@a|Types of RAG: An Overview (article)]]
TOC: [[Types-RAG-Oview@a#Naive RAG|Naive RAG]]
[[Types-RAG-Oview@a#Advanced RAG|Advanced RAG]] --> [[Types-RAG-Oview@a#Pre-Retrieval Processes|Pre-Retrieval Processes]]  |  [[Types-RAG-Oview@a#Post-Retrieval Processes|Post-Retrieval Processes]]
[[Types-RAG-Oview@a#Modular RAG|Modular RAG]] --> [[Types-RAG-Oview@a#Hybrid Search|Hybrid Search]] | [[Types-RAG-Oview@a#Recursive Retrieval and Query Engine|Recursive Retrieval and Query Engine]] |  [[Types-RAG-Oview@a#StepBack approach|StepBack approach]] | [[Types-RAG-Oview@a#Sub-Queries|Sub-Queries]] | [[Types-RAG-Oview@a#Hypothetical Document Embeddings|Hypothetical Document Embeddings]]


##### \* Архитектура RAG: часть вторая — Advanced RAG
 https://habr.com/ru/companies/raft/articles/818781/
 первое важное изменение - это значительный рост размера контекстного окна и падение стоимости токенов, до инфляции лиры еще не дотягивает, но уже близко. Например, размер окна в самой большой модели Клод от Антропик составляет 200+ тыс токенов, а Gemini, судя по последним новостям до 10млн. В таких условиях для многих задач RAG просто не требуется (или не все его компоненты),
##### \*  Архитектура RAG: полный гайд
https://habr.com/ru/companies/raft/articles/791034/
Архитектура RAG: полный гайд
.... Тут два варианта: доучивать модель вашими данными или использовать RAG.
Доучивать долго, дорого и скорее всего у вас все равно не выйдет (не переживайте, дело не в том что вы плохой родитель, просто это мало кто может и умеет делать).
Второй вариант — это Retrieval-Augmented Generation (известный так же под позывным RAG).
##### \*  Добавление собственных данных в LLM с помощью RAG
https://habr.com/ru/companies/wunderfund/articles/779748/
Добавление собственных данных в LLM с помощью RAG
....

[] Пользователь вводит вопрос.
[] Система ищет подходящие документы, которые могут содержать ответ на этот вопрос. Эти документы часто включают в себя собственные данные компании, которая разработала систему, а хранятся они обычно в некоем каталоге документов.
[] Система создаёт промпт для LLM, в котором скомбинированы данные, введённые пользователем, подходящие документы и инструкции для LLM. Модель должна ответить на вопрос пользователя, применив предоставленные ей документы.
[] Система отправляет промпт LLM.
[] LLM возвращает ответ на вопрос пользователя, основанный на предоставленных контекстных сведениях. Это — выходные данные системы.
Вот диаграмма, отражающая эту общую идею, лежащую в
основе RAG:

![[20240909212011.png]]



