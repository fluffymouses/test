# Отзывы

Мини-сервис для принятия отзыва и оценки его настроения.
pip install flask
Запустите сервер:
python app.py

Примеры использования:
Добавление отзыва:
Позитивные отзывы:
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Продукт отличный!"}'
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Хороший сервис."}'
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Все супер!"}'
Негативные отзывы:
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Доставка плохая!"}'
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Ремонт ужасный!"}'
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Система отвратительная!"}'
Нейтральные отзывы:
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Сервис можно улучшить."}'
curl -X POST "http://localhost:5000/reviews" -H "Content-Type: application/json" -d '{"text":"Нужно больше функций."}'

Пример ответа на добавление отзыва:
{"id":8,"text":"Нужно больше функций.","sentiment":"neutral","created_at":"2025-07-20T07:40:50.840350"}

Получение всех отзывов:
curl "http://localhost:5000/reviews"

Получение негативных отзывов:
curl "http://localhost:8000/reviews?sentiment=negative"
