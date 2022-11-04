# API сервис

Обязательный модуль для работы панели

Перейдите в папку shoppify-api `cd ~/shoppify-api`

```bash
yarn
yarn db:setup
```

После этих команд в папке shoppify-api появится файл базы данных database.sqlite
Вы можете его скачать по желанию и открыть программой DB Browser (SQLite) 

Теперь запустите сервис `yarn start:dev`
И перейдите по адресу 'api.ваш_домен' 

Если вы верно настроили сервер и домены, то открыв 'api.ваш_домен' - вы увидите сообщение о доступности сервиса.

Теперь создайте админ юзера 

```bash
curl --request POST \
  --url {api.ваш_домен}/auth/registration \
  --header 'Content-Type: application/json' \
  --data '{
    "login": "admin",
    "password": "admin"
  }'
```
В ответ должен прийти token


Остановите сервис `ctrl+C` и переходите к настройке модуля "Бот"