# 🧠 Astor Butler — Telegram AI Booking & Loyalty Assistant

Astor Butler is an intelligent assistant designed for HoReCa businesses (restaurants, cafes, clubs) to manage bookings, orders, payments, and customer loyalty — entirely through Telegram and AI.

---

## ✨ Features

- 🤖 AI-powered natural language processing for user interaction
- 📆 Table bookings with slot management and time control
- 🛍️ Merch and service ordering
- ❤️ Charity donations as a part of the ordering system
- 💰 Telegram Stars loyalty system (internal virtual currency)
- 💳 Real-time payments (Tinkoff, Sber, YooKassa integrations)
- 📊 Monitoring & observability: Redis, Kafka, Grafana ready
- 🔒 Secure role-based access: Guest / Manager / Admin
- 🛡️ Phone-based Telegram Login & phone number verification

---

## 🔧 Tech Stack

- Java 17, Spring Boot
- PostgreSQL, Redis
- Docker, docker-compose
- Kafka, Grafana, Prometheus
- Telegram Bot API (via TelegramLongPollingBot)
- Gradle & Maven compatibility

---

## 📄 License

This project is licensed under the **Apache License 2.0** — see [LICENSE](LICENSE) for details.  
By using this bot, you also accept the [Privacy Policy](PRIVACY_POLICY.md).

---

## 🧱 Architecture

Currently monolithic with modular packaging by features (table, merch, charity, etc.).  
Designed to evolve into a **microservice architecture**, with event-driven communication via Kafka.


---

## 🇷🇺 Описание на русском

**Astor Butler** — это умный Telegram-бот-помощник для ресторанов, кафе и клубов.  
Он обрабатывает брони, заказы, оплату и работает как система лояльности. Всё — через Telegram и AI.

---

### ✨ Функциональность:

- 🤖 Естественная обработка запросов с AI
- 📆 Бронирование столов по слотам
- 🛍️ Заказ мерча и дополнительных услуг
- ❤️ Возможность пожертвований прямо через бота
- 💰 Внутренняя валюта — Telegram Stars
- 💳 Онлайн-оплата (Тинькофф, Сбер, ЮKassa)
- 📊 Наблюдаемость через Redis / Kafka / Grafana
- 🔐 Роли пользователей: гость, менеджер, админ
- 📲 Вход по Telegram и привязка номера

---

### 🔧 Технологии:

- Java 21 + Spring Boot
- PostgreSQL, Redis
- Docker / Compose
- Kafka + Grafana / Prometheus
- Telegram Bot API
- Сборка через Gradle

---
