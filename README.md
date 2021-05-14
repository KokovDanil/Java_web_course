# web-service
Сервис из курса "Разработка веб сервиса на Java" на stepic.org

# сервлеты на signUp/signIn
При получении POST запроса на signup сервлет SignUpServlet должн запомнить логин и пароль в AccountService.
После этого польователь с таким логином считается зарегистрированным и остается запись в бд.
При получении POST запроса на signin, после регистрации, SignInServlet проверяет,
логин/пароль пользователя. Если пользователь уже зарегистрирован, север отвечает

Status code (200)
и текст страницы:
Authorized: login

если нет:
Status code (401)
текст страницы:
Unauthorized

# сервлет /admin
Сервлет, который обрабатываеи запросы на /admin
При получении GET запроса возвращать значение usersLimit.
По умолчанию 10

Выводит значение usersLimit в JMX с именем:
Admin:type=AccountServerController.usersLimit

# сервлет /resources

Выводит ResourceServer в JMX с именем:
Admin:type=ResourceServerController
Переменные "name" и "age" доступны для чтения из jmx клиента.

Сервлет, который обрабатывает запросы на /resources
При получении POST запроса с параметром path=path_to_resource читает ресурс TestResource из указанного в параметре файла, сохранит ссылку в ResourceService и выведет путь.

После чтения, значения name и age должны быть доступны по JMX.