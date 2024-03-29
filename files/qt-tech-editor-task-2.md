## Отправка и прием сообщений 1-1 чат-ботом

## Участники

Пользователь Б - пользователь домашнего оператора мобильной связи, здесь и далее, пользователь А отождествляется с авторизованным оператором связи клиентом этого пользователя. При этом множественные регистрации пользователя не поддерживаются самими клиентом чата.
Чат-бот - программная сущность, инициирующая отправку сообщений клиенту и выполняющая получение ответов клиента с использованием различных технологий. В данное статье чат-бот отождествляется с функционалом сервера, формирующего сигнальные и медиасообщения от имени чат-бота.

## Сценарий

1. *Чат-бот получил подтверждение возможности использования чата с клиентом Б*.
    При получении функциональных возможностей клиента Б по поддержке режима сессий чата с чат-ботом в заголовке Contact положительного ответа 200OK на инициированный в сценарии обмена функциональными возможностями чат-бота запрос **OPTIONS**, чат-бот продолжает сценарий.
    В противном случае чат с клиентом B невозможен, в логику отправки сообщений передается негативный ответ на запрос передачи сообщения конкретному пользователю, и прикладная логика выбирает альтернативный канал доставки сообщения.
2. *Сервер выступающий от имени чат-бота инициирует новую сессию чата 1-1 чат-бота с клиентом*
    Server по запросу чат-бота инициирует запрос INVITE адресату чата – пользователю Б. При этом заполняются следующие заголовки описанным далее способом, уточняя заполнение заголовков, описанных на шаге 1 системного кейса чата 1-1. Заголовки, заполнение которых не уточнено, заполняются как на шаге 1 системного кейса чата 1-1.