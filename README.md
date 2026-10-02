# Interactive Terminology Cards

Сервис интерактивного изучения терминологии и карточек для запоминания
с использованием алгоритма интервального повторения (Spaced Repetition).

## Концепция

Система решает проблему забывания профессиональных терминов.
Пользователь создаёт колоды карточек, а сервис по алгоритму SM-2
(как в Anki) определяет, когда показать карточку снова — для
максимально эффективного запоминания.

## Технологический стек

| Слой       | Технология                          |
|------------|-------------------------------------|
| Frontend   | React + TypeScript + Vite           |
| Backend    | Python 3.11 + FastAPI               |
| СУБД       | PostgreSQL 15                       |
| Кэш        | Redis 7                             |
| Развёртывание | Docker + Docker Compose          |

## Инструкция по развёртыванию (в будущем)

```bash
# 1. Клонировать репозиторий
git clone https://github.com/<ваш-логин>/interactive-vocab-cards.git
cd interactive-vocab-cards

# 2. Скопировать переменные окружения
cp .env.example .env
# отредактировать .env

# 3. Запустить контейнеры
docker-compose up -d

# 4. Применить миграции БД
docker-compose exec backend alembic upgrade head
