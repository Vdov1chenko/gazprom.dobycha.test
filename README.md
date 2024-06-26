# Тестовое задание «Интернет магазин»

## Описание

### Сущности:

- **Категории** – есть только название, должны быть многоуровневыми (условно 6 уровней максимум), имеют порядок на своем уровне вложенности.
- **Товары** – есть только название и цена, может лежать только в одной категории, имеет определенный порядок на своем уровне вложенности, может лежать только в одной категории.

### Необходимо 3 метода API:

1. **Отображение списка всех категорий с товарами**
    - HTTP метод: GET
    - Маршрут: `/categories`
    - Контроллер: `CategoryController@index`
    - Описание: Возвращает список всех категорий с их товарами, чтобы была видна вложенность.

2. **Генерация отчета покупок**
    - HTTP метод: GET
    - Маршрут: `/reports/purchases/{format}`
    - Контроллер: `PurchaseReportController@generateReport`
    - Описание: Генерирует отчет о покупках за последний месяц по дням в указанном формате (JSON или CSV).

3. **Метод перемещения товара в другую категорию**
    - HTTP метод: PUT
    - Маршрут: `/products/{product}/move-to-category/{category}`
    - Контроллер: `ProductController@moveToCategory`
    - Описание: Перемещает товар в другую категорию.

## Установка

1. Склонируйте репозиторий: `git clone <URL репозитория>`
2. Установите зависимости: `npm install`

## Использование

```bash
# Запуск локального сервера для разработки
npm run serve

# Сборка для продакшена
npm run build
