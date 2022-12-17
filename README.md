# Python Telegram Bot MongoDB

![Python](https://img.shields.io/badge/Python-3.8-blue?style=for-the-badge&logo=python)
![motor](https://img.shields.io/badge/motor_pymongo-gray?style=for-the-badge&logo=mongodb)

База данных для ботов python telegram на основе pyTelegramBotApi с MongoDB. Здесь речь идет о базовом функционале, который необходим для комфортной разработки. Библиотека может предоставить вам базовые взаимодействия с базой данных, пользователями и контентом.

## Installation

Просто скачайте папку, вставьте ее в свой проект и импортируйте основной класс `DataBase`. Создайте экземпляр класса и будьте счастливы.

```
pip[in work]
```

## Usage

```
database = DataBase(
    connection_string = f'mongodb+srv://{config.DB_USER}:{config.DB_PASSWORD}@cluster0.gafny.mongodb.net/{config.DB_NAME}?retryWrites=true&w=majority',
    db_name = config.DB_NAME,
)


@bot.message_handler(commands=['start'])
def send_start_message(message):
    database.register_user(message)
    bot.send_message(message.chat.id, 'Start message...')
```
### Присоединяйся к нам
[![Telegram](https://img.shields.io/badge/Telegram-blue?style=for-the-badge&logo=Telegram)](https://t.me/svpgcorporation)
