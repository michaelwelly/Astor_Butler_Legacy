# Astor Butler Legacy

Историческая реализация и источник продуктовых сценариев/тона общения.
Активный FSM-first runtime находится в [Astor Butler MVP](https://github.com/astor-hospitality/Astor_Butler_MVP),
гостевой агент — в [Astor Concierge](https://github.com/astor-hospitality/Astor_Concierge).
Legacy не является текущей целью деплоя Astor; перенос кода и данных требует
отдельного ревью. Список возможностей ниже — историческое описание, не
подтверждение работающих платёжных интеграций или production-приёмки.

## Подготовка к релизу — 06.10.2026

Фактический стек по `pom.xml` и CI: Java 17, Spring Boot 3.2.5, Maven.
Сборка через Gradle в текущем репозитории не подтверждена.

```bash
./mvnw test
./mvnw package
```

Эти команды требуют Java 17; тесты и запуск могут требовать настройки внешних
сервисов. В этой документационной сессии сборка Legacy не запускалась.

- [ ] Точный commit прошёл [CI](https://github.com/michaelwelly/Astor_Butler_Legacy/actions); история CI не заменяет новый прогон.
- [ ] Release notes явно указывают legacy/reference и ограничения, без обещания актуальной функциональности MVP.
- [ ] Проверены права/лицензии переносимых фрагментов; секреты, дампы и гостевые данные не попадают в assets.
- [ ] Не запускать старый бот с production-токеном действующего Butler.
- [ ] Отдельный стенд и отдельное разрешение нужны перед любым развёртыванием.

GitHub tag/release не равен production deployment. Старый workflow на push в
`main` публикует Docker-образ: документацию меняем через PR, без автоматического
мержа и без запуска этого workflow вручную.

Astor Butler is an intelligent assistant designed for HoReCa businesses (restaurants, cafes, clubs) to manage bookings, orders, payments, and customer loyalty — entirely through Telegram and AI.

---

## ✨ Features

- 🤖 AI-powered natural language processing for user interaction
- 📆 Table bookings with slot management and time control
- 🛍️ Merch and service ordering
- ❤️ Charity donations as a part of the ordering system
- 💰 Historical Telegram Stars/payment scenarios (live operation not verified)
- 💳 Payment integration groundwork (provider acceptance must be checked separately)
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
- Maven (`pom.xml`, Maven wrapper)

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
- 💰 Исторические сценарии Telegram Stars; это не собственная внутренняя валюта проекта
- 💳 Платёжные сценарии требуют отдельной проверки провайдера и приёмки
- 📊 Наблюдаемость через Redis / Kafka / Grafana
- 🔐 Роли пользователей: гость, менеджер, админ
- 📲 Вход по Telegram и привязка номера

---

### 🔧 Технологии:

- Java 17 + Spring Boot 3.2.5 (по `pom.xml`)
- PostgreSQL, Redis
- Docker / Compose
- Kafka + Grafana / Prometheus
- Telegram Bot API
- Сборка через Maven

---
