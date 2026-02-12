# Search Around The Market - TG Bot

тг-бот для парсинга информации о товарах с wb

##  main functions
- **поиск товаров:** парсинг WB по ключевым словам
- **лимиты:** лимиты на день, 20 запросов в день максимум
- **История:** вся история запросов пользователей хранится в json файле
- **Асинхронность:** использовал aiogram, для высокой скорости обработки

## stack
- **язык:** Python 3.10+
- **библиотека бота:** aiogram 3.x
- **парсинг:** Playwright (Chromium)
- **окружение:** python-dotenv (безопасное хранение токенов)

## peculiarity
на данный момент в файле `services/marketplaces.py` установлено значение:
`headless=False`

**почему эт особенность?:** пока чт (`headless=False`), тк при значение "true", идет banip, тк вб просит капчу, пробуйте пару раз пройти капчу сами и выставлять значение true. p.s в скором времени пофикшу.

## how to launch

**Клонируйте репозиторий:**
   ```bash
   git clone [https://github.com/shixanov/wbparserTGBot.git](https://github.com/shixanov/wbparserTGBot.git)
   cd wbparserTGBot
 ```
**установите зависимости:**
 ```bash
pip install -r requirements.txt
playwright install chromium
 ```
настройте переменные окружения:
 ```
Создайте файл .env на основе .env.example и вставьте ваш BOT_TOKEN.
 ```

запустите бота
 ```
python main.py
