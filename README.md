# Marketplace-API

## Основная идея

Минимальная версия маркетплейс back-end сервиса, где есть 2 основных актора

- Магазин который продает свою продукцию
- Клиент который выбирает и заказывает товар до пункта выдачи

## Функциональные требования

Магазин должен иметь возможность

- добавить товар
- добавить или выбрать категорию
- отгрузить товар

Клиент маркетплейса

- добавить товар в корзину
- оформить заказ
- выбрать пункт выдачи

## Модели

**PickUpPoints**

- id
- uuid
- name
- address
- close
- open
- created_at
- updated_at

**Users**

- id
- uuid
- login
- password
- email
- is_active
- created_at
- updated_at

**Stores (наследник User)**

- title
- address
- phone

**Store Items**

- id
- uuid
- name
- description
- price
- created_at
- updated_at

**Customers (наследник User)**

- firstname
- lastname
- phone
- card

**Cards**

- id
- uuid
- card_number_last4 unique
- customer_id
- created_at
- updated_at
