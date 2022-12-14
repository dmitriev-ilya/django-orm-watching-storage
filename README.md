# Пульт охраны

Это внутренний репозиторий для сотрудников банка "Сияние". Если вы попали в этот репозиторий случайно, то вы не сможете его запустить, т.к. у вас нет доступа к БД, но можете свободно использовать код вёрстки или посмотреть как реализованы запросы к БД.

Пульт охраны - это сайт, который можно подключить к удалённой базе данных с визитами и карточками пропуска сотрудников нашего банка.
Сайт служит для отслеживания доступа сотрудников банка в хранилище. Сервис позволяет хранить информацию о картах доступа, отслеживать визиты в хранилище, отслеживать активные карты, а также определять подозрительные визиты.
### Интерфейс

**Стартовая страница отображает список активных карт:**


![image](https://user-images.githubusercontent.com/67222917/206236356-9d17df06-be17-43d0-8a2f-44b65754c6d9.png)


**Список пользователей в хранилище:**


![image](https://user-images.githubusercontent.com/67222917/206236457-7593ee84-4b99-4898-be26-b305404ffc41.png)

**Истории визитов пользователей:**


![image](https://user-images.githubusercontent.com/67222917/206236552-2868c379-742c-4385-8ab6-39ba1d0a1116.png)


### Как установить
Python3 должен быть уже установлен. 
Затем используйте `pip` (или `pip3`, есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```

Требует определения переменных окружения в файле `.env`:
```bash
DATABASE_NAME=<DATABASE_NAME>
DATABASE_PASSWORD=<DATABASE_PASSWORD>
DATABASE_HOST=<DATABASE_HOST>
DATABASE_USER=<DATABASE_USER>
DATABASE_PORT=<DATABASE_PORT>
DATABASE_ENGINE=<DATABASE_ENGINE>
SECRET_KEY=<SECRET_KEY>
DEBUG=<bool>
ALLOWED_HOSTS=<list of ALLOWED_HOSTS>
```
Где `DATABASE_NAME`, `DATABASE_PASSWORD`, `DATABASE_HOST`, `DATABASE_USER`, `DATABASE_PORT`, `DATABASE_ENGINE` - данные для подключения к базе данных, `SECRET_KEY` - ключ доступа к сайту, `DEBUG` - включение и отключение дебаггинга на сайте, типа `bool`, `ALLOWED_HOSTS` - список доступных доменов.

### Как запустить

В терминале, командой:
```
python3 manage.py runserver 0.0.0.0:8000
```
