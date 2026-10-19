# Ktor Server

Проект REST API на Ktor с поддержкой:
- JSON-сериализации (`ContentNegotiation` + `kotlinx.serialization`)
- Маршрутов `GET`, `POST`, `DELETE`
- Обработки параметров в `query` и `path`
- Корректных HTTP статус-кодов (200, 201, 400, 404, 409)

## Запуск
Запустите `com.example.ApplicationKt` в IntelliJ IDEA или выполните:
```bash
./gradlew run
```
Сервер будет доступен на `http://localhost:8080`.

## Эндпоинты
- `GET /` — приветственное сообщение
- `GET /items` — список всех элементов (поддерживает `?search=текст`)
- `GET /items/{id}` — получение элемента по id (path-параметр)
- `POST /items` — создание нового элемента (принимает JSON: `{"id": 3, "name": "...", "description": "..."}`)
- `DELETE /items/{id}` — удаление элемента по id
