# Crypto Pro converter

Утилита конвертирует контейнеры `.reg` формата, полученные путем выгрузки их из системы на Windows в папку с файлами `.key`, пригодными для того чтобы создать локальный контейнер на MacOS и предположительно других UNIX системах. Утилита работает только с входными файлами в `utf-8`.

Протестировано с `CryptoPro CSP 5.0.12997`.

## Usage

Установите зависимости и запустите утилиту:

```bash
npm install
node index.js
```

Для более быстрого запуска была добавлена поддержка аргументов командной строки:

```bash
node index.js -r <путь_к_файлу.reg>
```

Далее уже руками нужно переместить папку с этими файлами в `/var/opt/cprocsp/keys/<имя_пользователя>/`. не забудте установить сертификат в контейнер для работы с электронной подписью, а так же корневой сертификат вашего УЦ. Все это можно сделать через CryptoPro CSP.
