Реализуем функционал приложения, с базовой структурой БД, можно ознакомится в visual paradigm, в ченджлогах и описании каждого микросервиса.

Stack
Java 17 Spring Boot 2 - для более быстрой разработки бэка. Maven - как инструмент сборки. PostgreSQL - как БД. Spring Data - для облегчения работы с БД. Hibernate - как ORM. Lombok - чтобы не писать boilerplate-код, используем на проекте Lombok. Mapstruct - для маппинга, Mapstruct. Liquibase - для миграции БД, Ссылка 1. Ссылка 2. Openfeign - для использования эврика-сервера, и фейн-клиентов для общения между микросервисами. Springdoc-openapi-ui - Swagger. Junit5 - для тестов. Mockito - для тестов. Spring Test - для интеграционных тестов. Spring-security - для аутентификации и авторизации. Docker - для поднятия контейнеров. Postman - тестирования через запросы. Visual paradigm - для проработки базовый структуры БД и генерации ченджлогов.

MVP
MVP - API (полностью описанное в Swagger). Работать с таким API можно будет через веб-интерфейс Swagger и Postman.

Бэкенд
Проект основан на микросерверной архитектуре. А каждый микросервис выстроен по архитектуре REST. Главный принцип следить, чтобы по логике одинаковые классы лежали в одном пакете.

Слои:

config конфигурационные классы
entity сущности базы данных
dto специальные сущности для передачи/получения данных в/с апи
repository dao-слой приложения, реализуем в виде интерфейсов Spring Data, имплементирующих JpaRepository.
service бизнес-логика приложения, реализуем в виде интерфейсов и имплементирующих их классов.
controller обычные и rest-контроллеры приложения.
validator валидаторов.
exception эксепшнов.
handler хэндлеров.
Работа на проекте
С чего начинать
Доступы. Если ты читаешь это, значит доступ к проекту у тебя уже есть

загрузи проект себе в среду разработки
изучи весь проект - начни с pom, properties файлов и конфигурационных классов, так же посмотри visual paradigm
в докере подними БД в командной строке запущенной от имени администратора надо ввести docker run --name postgres -e POSTGRES_PASSWORD=password -e POSTGRES_USER=user -e POSTGRES_DB=postgres -p 5434:5432 -d postgres, где --name имя контейнера, -e POSTGRES_PASSWORD= пароль БД, POSTGRES_USER= логин БД
так же в БД нужно создать 5 схем: account, anti_fraud, auth, history, profile
добейся успешного запуска своего микросервиса
