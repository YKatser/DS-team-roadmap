# DS-team-roadmap

![roadmap](files/roadmap.png)

## Table of Contents
- [1. Типы команд](#types)
- [2. Зрелость команд](#maturity)
- [3. Организация кода](#code)
    - [3.1 Типовая структура git репозитория](#code-git)
    - [3.2 Git Workflow](#code-git-workflow)
    - [3.3 Environment Managing](#code-environment)
    - [3.4 Pep8](#code-pep8)
    - [3.5 Code review](#code-review)
    - [3.6 Internal reporting (automized in Python)](#code-internal-reporting)
    - [3.7 External reporting (semi-automized)](#code-external-reporting)
- [4. Роли в команде](#team)
    - [4.1 Дизайн команды](#team-design)
    - [4.2 AI Product owner](#product-owner)
    - [4.3 Project manager](#project-manager)
    - [4.4 Team lead](#team-lead)
    - [4.5 Data scientist](#data-scientist)
    - [4.6 Developer](#developer)
- [5. Управление проектом](#project)
    - [5.1 Проработка проекта в начале](#project-start)
    - [5.2 Взаимодействие членов команды](#project-team)
    - [5.3 Организация проекта](#project-organizing)
    - [5.4 Организация канбан доски](#project-kanban)
- [6. Оценка продуктивности](#productivity-assesment)
    - [6.1 Individual](#productivity-assesment-ind)
    - [6.2 Team](#productivity-assesment-team)

#### Как мы проверяем и оцениваем гипотезы в YouDo, Адам Елдаров, Head of Product and Data Science
https://www.youtube.com/watch?v=jmjzSor1WDU
>Как организовать DS в компании, какие варианты построения команд есть, как фокусировать команду на самом важном, проверять гипотезы и как оценивать их эффективность для бизнеса.

<a name="types"></a>
## 1. Типы команд
<img src="files/teams.png" alt="teams" width="600" height="300">

- Ad-hoc
- Product
- Support

<a name="maturity"></a>
## 2. Зрелость команд
4 уровня зрелости:
- Oblivious
- Emerging 
- Managed
- Optimizing

<img src="files/DS-maturity.png" alt="maturity" width="600" height="300">

#### Ссылки
>[Модель зрелости процессов LeanDS](https://www.youtube.com/watch?v=xlw8vgee5bU)

<a name="code"></a>
## 3. Организация кода
Система организации кода и связанной с ним технической части проекта.  

<a name="code-git"></a>
### 3.1 Типовая структура git репозитория
#### Описание
Структура репозитория для унификации, прозрачности работы и упрощения переключения между проектами для всех участников команды и сотрудников компании.

#### Ссылки
>https://github.com/YKatser/ml-project-template

<a name="code-git-workflow"></a>
### 3.2 Git Workflow
#### Описание
1. Для каждого изменения в мастер или при проверке очередной гипотезы создается отдельная ветка, в которой эти изменения вносятся и гипотезы проверяются. В случае успеха отправляется pull request для дальнейшего рассмотрения и возможного мерджа с мастером.
2. Code review и hypothesis check review проводятся на этапе отправки pull request, и при успешном review ветка мерджится с мастером.
3. Каждая ветка предназначена для одной гипотезы, небольших (не более 3х человекодней работы) изменений и соответствует тикету в jira. Поэтому название ветки рекомендуется брать из названия карточки в jira.
4. При подготовке pull request НЕОБХОДИМО писать комментарий с кратким описанием изменений, при проверке гипотез можно дополнительно добавлять ридми, где отображать метрики/графики ([пример](https://www.youtube.com/watch?v=9BgIDqAzfuA)).

<img src="files/git workflow1.png" alt="git workflow1" width="600" height="140">

<img src="files/git workflow.jpg" alt="git workflow" width="600" height="350">

#### Ссылки
>https://github.com/dslp/dslp/blob/main/branching/branch-types.md#experiment-branches  
>[Курс MLRepa](https://ml-repa.ru/reproducibility-pipelines-automation-mlops)

<a name="code-environment"></a>
### 3.3 Environment Managing
#### Описание
Для обеспечения воспроизводимости важно использовать requirements.txt, инициализируя файл в самом начале проекта.
Управление зависимостями помогает управлять всеми библиотеками, необходимыми для работы приложения.
Можно как использовать виртуальное окружение (приоритетный вариант), так и работать с ноутбуками в контейнере.

#### Ссылки
>[Creating Virtual Environments and Managing Packages with pip](https://docs.python.org/3/tutorial/venv.html)  
>[Add Virtual Environment to Jupyter Notebook/Juplab](https://janakiev.com/blog/jupyter-virtual-envs/)

<a name="code-pep8"></a>
### 3.4 Pep8
#### Описание
Единый стандарт написания кода для унификации стиля написания кода и упрощения чтения кода.
    
#### Ссылки
>https://pep8.org  
>https://gist.github.com/RichardBronosky/454964087739a449da04 - pep8 cheat sheet (short)

<a name="code-review"></a>
### 3.5 Code review
#### Описание
Проверка исходного кода на ошибки, проблемы постановки эксперимента.

#### Ссылки
>https://tlroadmap.io/roles/technical-lead/product-quality/code-review.html  
>https://mtlynch.io/human-code-reviews-1/  
>https://mtlynch.io/human-code-reviews-2/  
>https://youtu.be/2F6J82-Ch88

<a name="code-internal-reporting"></a>
### 3.6 Internal reporting (automized in Python)
#### Описание
Заполнение документов о результатах проверки гипотез, а также внутренние отчеты (по работе моделей и тд).
Процесс должен быть унифицирован и автоматизирован в начале или до начала очередного проекта.
    
#### Ссылки
>[Пример отчета](https://drive.google.com/file/d/1jahPaEie6T4hBrun4HkysXqibxntjkV_/view?usp=drivesdk)

<a name="code-external-reporting"></a>
### 3.7 External reporting (semi-automized)
#### Описание
Внешний отчеты для заказчика/клиента/контролирующих органов. Могут составляться по гостам, по форме, согласованной до начала/в процессе проекта, в свободной форме.

#### Ссылки
>Пример отчета

<a name="team"></a>
## 4. Роли в команде
Система организации команды.

<img src="files/team-customer-connection.png" alt="team-customer-connection" width="400" height="250">

<a name="team-design"></a>
### 4.1 Дизайн команды
#### Описание
Актуально и для единой структурной единицы (лаборатории, отдела), и для проектной команды, работающей над одним бэклогом.
У каждой роли свой список обязанностей (должностная инструкция) и свой круг ответственности. 
Обязанности и ответственность могут меняться в зависимости от проекта и этапа проекта.

- Responsibility assignment matrix:
<img src="files/RACI.png" alt="RACI" width="700" height="300">
    
#### Ссылки
>https://tlroadmap.io/roles/people-manager/team-management/team-design.html

<a name="product-owner"></a>
### 4.2 AI Product owner
#### Описание
- Мост между бизнесом и DS.
- Понимание возможностей и ограничений DS.
- Полномочия принятия решений.
- Ответственность за результат с точки зрения бизнеса и потребителя.

#### Ссылки
    todo

<a name="project-manager"></a>
### 4.3 Project manager
    todo
    
<a name="team-lead"></a>
### 4.4 Team lead
#### Описание
Team lead - связь между продукт менеджером/продукт овнером и членами DS команды/команды разработки. 
Может совмещать роли продукт менеджера, проджект менеджера.
    
#### Ссылки
>[Team lead roadmap](https://github.com/tlbootcamp/tlroadmap) – это карта навыков и компетенций тимлидов, которую можно адаптировать для любой компании и команды:  
>[Конспекты лекций о тимлидстве](https://github.com/YKatser/DS-links/blob/master/TeamLeadLectures.md)

<a name="data-scientist"></a>
### 4.5 Data scientist
#### Описание
Процесс работы DS выглядит следующим образом:

<img src="files/ds-process.png" alt="ds-process" width="800" height="400">

<a name="developer"></a>
### 4.6 Developer
    todo
   
<a name="project"></a> 
## 5. Управление проектом
Система организации проектной деятельности.

<a name="project-start"></a>
### 5.1 Проработка проекта в начале
- AI canvas
>[Как мы используем AI Канвас в БигДате МТС, Мария Ракитина, менеджер продуктов МТС](https://www.youtube.com/watch?v=frtCsg8tPp4)  
>[The Ultimate AI Canvas](https://www.youtube.com/watch?v=hTR66u0i1Qo)

<img src="files/ai canvas.png" alt="ai canvas" width="600" height="300">

- Check list

<img src="files/check list.png" alt="check list" width="600" height="300">

- User story map
>[Story mapping. Как спроектировать продукт с AI-состовляющей](https://youtu.be/GAZ6EDjEDF0?t=872)

- Dataset Card (Паспорт датасета, карточка с различной информацией о датасете)
    - Объем данных, баланс классов, Примеры данных, источник данных и лицензия, тип разметки, иные особенности
    - Помогает не сойти с ума при работе с данными, онбордить новичков, оперативно снабжать другие отделы информацией, принимать решения по данным
    - Формат - Google Doc, Markdown, интерактивная витрина (Streamlit-приложение)
>Источник - [MLOps: жизненный цикл ML-моделей от идеи до продакшна](https://youtu.be/uQ--wxaxzSk?t=1035)

<a name="project-team"></a>
### 5.2 Взаимодействие членов команды
#### Описание
Планируемые встречи (взаимодействие команды): 
- Брейнстормы - для наполнения бэклога и определения архитектуры решения (раз в 2 недели)
- Стендапы ([Kanban meeting](https://systemskill.ru/tpost/eacanrfh51-kak-provesti-kanban-miting-kanban-meetin)) - для обеспечения прозрачности и выявления рисков/проблем (ежедневно, через день)
- Ретроспективы (ретро) - для настройки процесса и понимания слабых мест (раз в 2 недели)

Для сложных гипотез/проектов "Парный Data Science"

#### Ссылки
>[Парный Data Science](https://www.youtube.com/watch?v=n1aurzZajJk)  

<a name="project-organizing"></a>
### 5.3 Организация проекта
#### Описание
Система (фреймворк), описывающая все процессы взаимодействия с внешними и внутренними лицами и исполнителями и тд.
    
#### Ссылки
>[Team Data Science Process (TDSP)](https://docs.microsoft.com/ru-ru/azure/machine-learning/team-data-science-process/lifecycle-data)  
>[CRISP-DM](https://www.the-modeling-agency.com/crisp-dm.pdf)  
>[Lean Data Science 1.0 (SOTA)](https://www.youtube.com/watch?v=GAZ6EDjEDF0)
>[LeanDS](https://leands.ai/ru)
>[QUEST framework](https://www.youtube.com/watch?v=rPisw2KNsC0)

<a name="project-kanban"></a>
### 5.4 Организация канбан доски
#### Описание
Канбан доска создаётся на основе болей и проблем команды, чтобы она была вспомогательным инструментом в работе и в обеспечении качества проекта.
    
#### Ссылки
>https://www.youtube.com/watch?v=QYkuv2zuCFk

<a name="productivity-assesment"></a>
## 6. Оценка продуктивности
Оценка личной и командной продуктивности. 
Процесс может быть выстроен как регулярный анализ и разбор метрик продуктивности (пример команды) или как регулярные performance review (пример члена команды).

<a name="productivity-assesment-ind"></a>
### 6.1 Individual
#### Описание
Оценка эффективности членов команды чаще всего проходит с помощью регулярных performance review. 
Performance review - это инструмент измерения эффективности члена команды.

Как часто:
- По времени (раз в квартал)
- По проектам (после каждого крупного проекта)

Дополнительно использовать one-on-one Тим Лида с каждым членом команды, чтобы рассказать результаты ревью, собрать обратную связь, а также обсудить вопросы, которые лучше не выносить на публику.

#### Ссылки
>[Performance review](https://youtu.be/HKXJ_AWPVBA)  
>[One-on-One 1](https://github.com/YKatser/DS-links/blob/master/TeamLeadLectures.md#георгий-могелашвили-bookingcom-эффективные-1-на-1)  
>[One-on-One 2](https://github.com/YKatser/DS-links/blob/master/TeamLeadLectures.md#встречи-one-on-one-инструмент-эффективного-управления-сотрудниками-никита-бакунин)

<a name="productivity-assesment-team"></a>
### 6.2 Team
#### Описание
Оценка эффективности команды/отдельных исполнителей.
- Время проверки гипотез
- Можно через TTM (Time-To-Market) и другие продуктовые метрики
- выполнение плана
    
#### Ссылки
>https://youtu.be/c0CRiCeJ99s  
>https://www.datascience-pm.com/9-ways-to-measure-data-science-project-performance/
