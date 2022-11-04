# Установка панели

Перейдите в папку shoppify-panel `cd ~/shoppify-panel`


```bash
yarn
yarn build
yarn generate
```

После этих команд в папке shoppify-panel появится папка dist.
Ее необходимо скопировать в /var/www

```bash
sudo rm -rf /var/www/ваш_домен/html
sudo cp -r dist /var/www/ваш_домен/html
```

Если вы верно настроили сервер и домены, то открыв ваш_домен - вы увидите форму входа
