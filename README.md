Родительский репозиторий для автоматизации запуска backend и sender части приложения TelegramForwarder

Приложение предназначено для "вылавливания" сообщений по определенным словам из публичных групп.
Для того чтобы получать сообщения, нужно добавить через backend (через бота) подписку на публичную группу.

Разворачиваем на хостинге:

- git clone https://github.com/lashnag/telegram-forwarder.git
- добавляем свой файл .env с настройками окружения
- git clone https://github.com/lashnag/telegram-client-sender-api.git
- устанавливаем python
- cd SenderApi
- pip install -r requirements.txt
- cd app
- python save_session.py
- Вводим Api Id, Api Hash, телефон и код подтверждения
- Ищем папку mounted и копируем из нее файл session.txt в папку первого репозитория в /mounted/sender_api/
- В папке первого репозитория запускаем docker-compose up