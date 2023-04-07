# ByPASS SERVER

Сервер для сохранения логов, выдачи паспортов и печати наклеек для ByPASS

Для приложения необходимы библиотеки fastapi, uvicorn, jinja2 и т.д

Полный список зависимостей находится в файле requirements.txt.

Установка всех зависимостей:
```
pip install -r requirements.txt
```
# Структура

static-место для хранения css стилей и постоянных файлов

web-место для хранения сгенерированных html-страниц

templates- место для хранения jinja2-шаблонов, нужных для генерации


# Настройка

Конфигурационный файл - settings.ini

В файле необходимо задать:

    host - ip-адрес сервиса
    port - порт, на котором работает приложение
    path_ocp-папку для хранения логов ocp(создастся автоматически)
    path_tofino-папку для хранения логов TOFINO(создатся автоматически)
    path_ocp_passports=папку, где будет хранится таблица с паспортами
    path_platform-Папку, где будут хранится таблицы и логи платформ(в будущем)

желательно создать папку с паспортами вручную либо при попытке выдать создатся автоматически,

после чего туда надо поместить вручную таблицу. В будущем возможно организую автозагрузку
# Запуск

Запустить скрипт:
    python main.py

Все необходимые команды можно получить по адресу {ip}{port}/docs

Для захода на стартовую страницу нужно прописать в браузере {ip}{port}/

Все папки для хранения создадутся при запуске скрипта(если не было созданы заранее). Не забудьте поместить паспорта в папку

