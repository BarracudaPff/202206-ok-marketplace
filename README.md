# 202206-ok-marketplace

Учебный проект
курса [Kotlin Backend Developer](https://otus.ru/lessons/kotlin/?int_source=courses_catalog&int_term=programming).
Marketplace -- это площадка, на которой пользователи выставляют предложения и потребности. Задача площадки --
предоставить наиболее подходящие варианты в обоих случаях: для предложения -- набор вариантов с потребностями, для
потребностей -- набор вариантов с предложениями.

## Что нового в проекте
По сравнению с предыдущим потоком появились следующие изменения:
пока нет.

## Учебный маркетинг приложения

Считаем, что целевая аудитория учебного сервиса -- это средние и крупные предприятия, желающие (а) продать свою
высокотехнологичную продукцию или (б) найти поставщиков для ее производства.

### Гипотетический портрет пользователя для службы Потребностей

1. Высококвалифицированный инженер среднего или высшего звена, который ищет поставщиков компонентов для разрабатываемого
   продукта.
2. Мужчина от 30 до 50 лет
3. С высшим образованием
4. С критическим складом ума, со склонностью сопоставлять цифры, технические характеристики и не ведется на броскую
   рекламу
5. Как правило, женат, имеет детей (как маленьких, так и взрослых), обеспечен, имеет жилье и автомобиль

### Гипотетический портрет пользователя для службы Предложений

Можно выделить несколько сегментов пользователей

1. Высококвалифицированный и опытный сотрудник отдела продаж, знающий как продукт, так и технические детали
    1. Мужчина от 30 до 50 лет
    2. С высшим образованием, знает технологические нюансы продаваемой продукции и как эта продукция используется
    3. Знаком лично с большинством клиентов, большая часть всех продаж через личные контакты
2. Начинающий или низкоквалифицированный продажник
    1. Молодой мужчина до 30-35 лет
    2. Без высшего образование или без опыта работы в соответствующей отрасли
    3. Делает продажи посредством холодных звонков
    4. и т.д.
3. И т.д.

## Описание MVP

![](imgs/design-layout.png)

### Функции (эндпониты)

1. CRUDS (create, read, update, delete, search) для объявлений (ad)
1. ad.offers (опционально)

### Описание сущности ad

1. Info
    1. Title
    2. Description
    3. Owner
    4. Visibility
2. DealSide: Demand/Proposal
3. ProductType (гаечный ключ, ...)
4. ProductId - идентификатор модели товара

# Структура проекта

## Подпроекты для занятий по языку Kotlin

1. [m1l1-hello-world](m1l1-hello-world) - Вводное занятие, создание первой программы на Kotlin
3. [m1l3-oop](m1l3-oop) - Объектно-ориентированное программирование
3. [m1l4-dsl](m1l4-dsl) - Предметно ориентированные языки (DSL)
4. [m1l5-coroutines](m1l5-coroutines) - Асинхронное и многопоточное программирование с корутинами
4. [m1l6-flows-and-channels](m1l6-flows-and-channels) - Асинхронное и многопоточное программирование с Flow и каналами
5. [m1l7-kmp](m1l7-kmp) - Kotlin Multiplatform и интероперабельность с JVM, JS
6. [m2l2-testing](m2l2-testing) - Тестирование проекта, TDD, MDD

## Транспортные модели, API

1. [specs](specs) - описание API в форме OpenAPI-спецификаций
2. [ok-marketplace-api-v1-jackson](ok-marketplace-api-v1-jackson) - Генерация первой версии транспортных модеелй с
   Jackson
3. [ok-marketplace-api-v2-kmp](ok-marketplace-api-v2-kmp) - Генерация второй версии транспортных модеелй с KMP
4. [ok-marketplace-common](ok-marketplace-common) - модуль с общими классами для модулей проекта. В частности, там
   располагаются внутренние модели и контекст.
5. [ok-marketplace-mappers-v1](ok-marketplace-mappers-v1) - Мапер между внутренними моделями и моделями API v1
6. [ok-marketplace-mappers-v2](ok-marketplace-mappers-v2) - Мапер между внутренними моделями и моделями API v1

## Фреймворки и транспорты

[//]: # (1. [ok-marketplace-services]&#40;ok-marketplace-services&#41; - Сервис. Служит оберткой для модуля бизнес-логики. Подключается)

[//]: # (   всеми фреймворками &#40;модулями `*-app-*`&#41;)

[//]: # (1. [ok-marketplace-app-spring]&#40;ok-marketplace-app-spring&#41; - Приложение на Spring Framework)

[//]: # (1. [ok-marketplace-app-ktor]&#40;ok-marketplace-app-ktor&#41; - Приложение на Ktor JVM)

[//]: # (1. [ok-marketplace-app-ktor-native]&#40;ok-marketplace-app-ktor-native&#41; - Приложение на Ktor Native)

[//]: # (1. [ok-marketplace-app-ktor-common]&#40;ok-marketplace-app-ktor-common&#41; - Общая логика для Ktor JVM и Ktor Native)

[//]: # (1. [ok-marketplace-app-knative]&#40;ok-marketplace-app-knative&#41; - Скрипты запуска приложения в KNative)

[//]: # (1. [ok-marketplace-app-rabbit]&#40;ok-marketplace-app-rabbit&#41; - Микросервис на RabbitMQ)

[//]: # (1. [ok-marketplace-app-kafka]&#40;ok-marketplace-app-kafka&#41; - Микросервис на Kafka)

## Модули бизнес-логики

[//]: # (1. [ok-marketplace-stubs]&#40;ok-marketplace-stubs&#41; - Стабы для ответов сервиса)

[//]: # (1. [ok-marketplace-biz]&#40;ok-marketplace-biz&#41; - Модуль бизнес-логики приложения)

## Хранение, репозитории, базы данных

[//]: # (1. [ok-marketplace-repo-test]&#40;ok-marketplace-repo-test&#41; - Базовые тесты для репозиториев всех баз данных)

[//]: # (2. [ok-marketplace-repo-inmemory]&#40;ok-marketplace-repo-inmemory&#41; - Репозиторий на базе кэша в памяти для тестирования)

[//]: # (3. [ok-marketplace-repo-sql]&#40;ok-marketplace-repo-sql&#41; - Репозиторий на базе PostgreSQL)

[//]: # (4. [ok-marketplace-repo-cassandra]&#40;ok-marketplace-repo-cassandra&#41; - Репозиторий на базе Cassandra)

[//]: # (5. [ok-marketplace-repo-gremlin]&#40;ok-marketplace-repo-gremlin&#41; - Репозиторий на базе Apache TinkerPop Gremlin и ArcadeDb)
