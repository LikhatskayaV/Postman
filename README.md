![all text](https://blog.postman.com/wp-content/uploads/2020/03/api-clients.png)

**Postman** — это **HTTP-клиент** для тестирования **API**. HTTP-клиенты тестируют отправку запросов с клиента на сервер и получение ответа от сервера. API (Application Programming Interface) — это интерфейс для обмена данными с сервера между двумя приложениями или компонентами ПО.

**API** — сокращение от **A**pplication **P**rogramming **I**nterface (программный интерфейс приложения). API — набор правил, протоколов и инструментов для взаимодействия между приложениями. Говоря простым языком, API — интерфейс, который определяет, как одна программа должна взаимодействовать с другой программой. Как правило, представляет собой набор функций, которые могут быть вызваны другой программой.

Как тестировщики, с помощью Postman мы можем отсылать HTTP/s запросы к сервисам и получать от них ответы. С помощью такого подхода можно протестировать бэкенд сервисы и убедиться, что они корректно работают.

Сегодня Postman — супер-популярный инструмент. И вот почему:

- **Бесплатный.** Postman — бесплатный инструмент.
- **Простой в использовании.** Очень просто начать пользоваться — Postman интуитивно понятный. Уже через несколько минут после скачивания и установки вы сможете отправить ваш первый запрос.
- **Поддерживает разные API.** С помощью Postman можно выполнять разные типы запросов к любым API (REST, SOAP, GraphQL (по тестированию GraphQL c помощью Postman у нас есть отдельная статья)
- **Расширяемый.** Postman можно настроить под ваши конкретные нужды с помощью Postman API.
- **Интегрируемый.** Можно легко интегрировать наборы тестов в ваш любимый CI/CD инструмент с помощью Newman (CLI collection runner — позволяет запускать Postman-коллекции в командной строке)
- **Имеет большое комьюнити.** Postman очень популярный и, как следствие, имеет большое комьюнити, которое подскажет ответы на большинство вопросов.

**Некоторые из особенностей Postman:**
- Простой в использовании API клиент.
- Функциональный и приятный UI.
- Может использоваться как для ручного, так и для автоматизированного тестирования API.
- Поддерживает интеграции с другими инструментами (например, поддерживает Swagger и RAML)
- Может быть запущен в Windows, Linux, MacOS.Не требует знания языков программирования.
- Предоставляет возможность легко экспортировать коллекции запросов, наборы тестов. Можно легко обмениваться этими данными с коллегами.
- Интегрируется с CI/CD инструментами (например, с Jenkins, TeamCity и т.п.)
- API Posman-a подробно документирован.
- Позволяет выполнять API автотесты.

Как пользоваться Postman
Для начала, давайте подробно рассмотрим интерфейс. Мы сознательно будем рассматривать английскую версию (и рекомендуем использовать именно ее):

![Рабочая область Postman](https://i0.wp.com/testengineer.ru/wp-content/uploads/2021/08/gajd-po-testirovaniyu-v-postman-01.webp?resize=696%2C274&ssl=1)

1. **New:** С помощью этой кнопки можно создать новый запрос (Request), коллекцию (Collection) или окружение (Environment).
2. **Import:** С помощью этой кнопки можно импортировать коллекцию или окружение. По нажатию откроется окно, где вы сможете выбрать одну из нескольких опций для импорта: импорт из файла, папки или по ссылке. Также можно просто вставить данные для импорта в текстовое поле.
3. **Runner:** По нажатию на кнопку запускается Collection Runner, который выполняет коллекции запросов.
4. **Open New:** По нажатию открывается новое окно Postman или новое окно запуска коллекций.
5. **My Workspace:** Моя рабочая область. С помощью этой кнопки можно создать новую рабочую область (workspace). Рабочая область предоставляет общий контекст для работы с API. Может использоваться для совместной работы внутри команды (ее можно расшарить с коллегами).
6. **Invite:** С помощью этой кнопки можно пригласить других членов команды для совместной работы внутри рабочей области (workspace-а)
7. **History:** Все запросы и ответы попадают во вкладку «History» (История). Это позволяет вернуться к предыдущим запросам.
8. **Collections:** В этой вкладке хранятся коллекции запросов. Коллекции используются для группировки запросов по каким-либо признакам.
9. **Request Tab:** Вкладка запроса. Название вкладки по умолчанию — Untitled Project. Хорошая практика — называть вкладку по названию запроса.
10. **HTTP Request:** С помощью этого выпадающего списка можно выбрать тип запроса: GET, POST, PUT, PATCH, DELETE и т.п.
11. **Request URL:** URL API запроса.
12. **Save:** По нажатию на кнопку Save можно сохранить запрос (или перезаписать, если запрос уже был сохранен ранее)
13. **Params:** Параметры, необходимые для выполнения запроса.
14. **Authorization:** API используют авторизацию, чтобы убедиться, что клиент имеет доступ к запрашиваемым данным. В этой секции описываются параметры авторизации: например, username, password, bearer-токен и т.п.
15. **Headers:** Для работы с некоторыми API с каждым запросом необходимо отправлять специальные хедеры. Это нужно для того, чтобы добавить дополнительные данные о типе операции, которую вы хотите провести. Хедеры можно указать в этой секции.
16. **Body:** В этой вкладке указываются данные, которые должны быть отправлены вместе с запросом.
17. **Pre-request Script:** Pre-request скрипты пишутся на JavaScript и выполняются перед отправкой запросов. Используются для того, чтобы провести какие-то действия прямо перед тем, как отправить запрос (например, добавить timestamp или какие-то вычисляемые данные в ваши запросы)
18. **Tests:** Во вкладке Tests находятся скрипты, которые выполняются во время запроса. Тесты позволяют проверить API и убедиться, что все работает так, как это было задумано.
