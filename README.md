### Для работы бота нужно:
1. получить бесплатный API-ключ на OpenWeatherMap
2. Создать бота в Телеграм при помощи Botfather и получить BOT_TOKEN и CHAT_ID

### Пояснения к коду:

1. Подключается к Wi‑Fi и запрашивает данные о погоде из OpenWeatherMap.
2. Полностью парсит JSON‑ответ, извлекая все значения и добавляя пояснения на русском языке.
3. Формирует подробное сообщение с расшифровкой каждого параметра.
4. Отправляет сформированное сообщение в Телеграм-бот через API.

Обратите внимание, что в коде заданы параметры Телеграм:
- telegramBotToken
- telegramChatId

1. **Парсинг JSON:**  
   Код извлекает все ключевые значения из JSON-ответа OpenWeatherMap и формирует понятное сообщение на русском языке с пояснениями.
2. **Время:**  
   Время расчёта (dt), а также время восхода и заката (sys.sunrise, sys.sunset) корректируются с учётом смещения (timezone) и преобразуются в строковый формат.
3. **Формирование сообщения:**  
   Все данные, включая координаты, погодные условия, основные параметры, видимость, ветер, облачность и системную информацию, объединяются в одно сообщение.
4. **Отправка в Телеграм:**  
   Сформированное сообщение отправляется через API Telegram-бота, используя заданные токен и ID чата.

Теперь при каждом обновлении (каждые 60 минут) бот будет отправлять в Телеграм подробное сообщение, содержащее все значения из JSON-ответа с пояснениями на русском языке.


