# Keet Username Checker

**Keet Username Checker** — это Python-скрипт для автоматической генерации и проверки никнеймов в Keet с помощью OCR (Tesseract + OpenCV) и эмуляции действий пользователя.

[🇺🇸 Читать на английском](./README.md)

📹 Демонстрационное видео: [Watch on YouTube](https://www.youtube.com/watch?v=xmpNrbXmt4k)

Он умеет:
- Генерировать никнеймы по правилам (буквы + цифры, минимум 3 символа).
- Исключать дубликаты и повторные проверки.
- Сохранять проверенные, занятые и свободные ники.
- Читать сообщения Keet с помощью OCR.
- Поддерживает мультиязычность (русский и английский).

## ⚡ Возможности
- Автоматическая проверка никнеймов.
- Распознавание текста через OCR (pytesseract + opencv).
- Работа с окнами Windows (pyautogui, pywinauto).
- Продолжение работы после перезапуска.
- Выбор языка интерфейса (--lang en / --lang ru).

## 📦 Установка
Склонируйте репозиторий:
```bash
git clone https://github.com/YOUR_USERNAME/keet-username-checker.git
```
cd keet-username-checker

Установите зависимости:
pip install -r requirements.txt

Установите Tesseract OCR:
Скачать: https://github.com/tesseract-ocr/tesseract
После установки добавьте путь к Tesseract в PATH системы.

## ▶️ Использование
Калибровка:
python keet.py calibrate --lang ru

Запуск:
python keet.py run --lang ru

Options:
- --lang en/ru        Выбор языка
- --min_len N         Минимальная длина ника (по умолчанию 3)
- --max_len N         Максимальная длина ника
- --no-resume         Не продолжать с предыдущего состояния
- --no-require-digit  Разрешить ники без цифр

## Output Files
- free_nicks.txt — свободные ники ✅
- used_nicks.txt — занятые ники ❌
- checked_nicks.txt — все проверенные ники 📝

## Лицензия

Этот проект лицензирован под **MIT license**. Смотрите [`ЛИЦЕНЗИЮ`](./LICENSE) для большей информации.
