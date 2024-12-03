# Веб-приложение для управления киберспортивными соревнованиями

## Описание проекта
Данный проект представляет собой веб-приложение для управления киберспортивными турнирами. Система позволяет регистрировать пользователей, организовывать турниры, управлять матчами, прогнозировать результаты и предоставлять отчеты.  
Технологический стек: **Spring Boot** для серверной части и **React** для фронтенда.

---

## Диаграммы

### 1. Диаграмма структуры функциональных возможностей (Mind Map)

Эта диаграмма отображает основные функции системы, включая регистрацию пользователей, управление матчами, прогнозирование результатов, матчмейкинг и отчеты. Также указаны ключевые технологии, используемые в проекте.

```mermaid
mindmap
  root((Киберспортивный Менеджер))
    Регистрация
      Пользователей
      Команд
      Турниров
    Управление матчами
      Расписание
      Результаты
      Статистика
    Прогнозирование
      Анализ данных
      Рекомендации
    Матчмейкинг
      Связь с игровым сервером
      Балансировка команд
    Отчеты
      Индивидуальные
      Командные
      Турнирные
    Технологии
      Backend(Spring Boot)
      Frontend(React)
      База данных(MySQL)
      Кэширование(Redis)
      Сообщения(Kafka)
```

### 2. Диаграмма путешествия пользователя (User Journey)

Эта диаграмма иллюстрирует путь пользователя в системе — от регистрации до получения результатов турнира.

```journey
  title Пользовательский путь: Участие в турнире
  section Регистрация
    Пользователь: Заполняет форму регистрации: 5: Пользователь
    Система: Создает учетную запись: 4: Система
  section Вход в систему
    Пользователь: Авторизуется: 4: Пользователь
    Система: Проверяет учетные данные: 4: Система
  section Участие в турнире
    Пользователь: Выбирает турнир: 5: Пользователь
    Система: Подтверждает участие: 4: Система
    Пользователь: Участвует в матчах: 5: Пользователь
  section Получение результатов
    Система: Сохраняет статистику: 5: Система
    Пользователь: Смотрит результаты и отчеты: 4: Пользователь
```

### 3. Квадрантная диаграмма (Quadrant Chart)

Эта диаграмма показывает распределение функциональных возможностей системы по важности и сложности.

```quadrantChart
  title Приоритеты функционала
  "Высокая важность/Высокая сложность" : "Матчмейкинг, Прогнозирование"
  "Высокая важность/Низкая сложность" : "Регистрация пользователей, Управление матчами"
  "Низкая важность/Высокая сложность" : "Расширенная аналитика"
  "Низкая важность/Низкая сложность" : "Элементы UI, Дополнительные отчеты"
```
### 4. Диаграмма истории разработки (Git Graph)

Эта диаграмма демонстрирует этапы разработки приложения, включая реализацию микросервисов: user-service, tournament-service, matchmaking-service и analytic-service

```gitGraph
  commit id: "Создание структуры проекта"
  branch feature/user-service
  commit id: "Реализован сервис пользователей"
  branch feature/tournament-service
  checkout feature/tournament-service
  commit id: "Добавлен функционал управления турнирами"
  branch feature/matchmaking-service
  checkout feature/matchmaking-service
  commit id: "Реализован матчмейкинг"
  merge main
  checkout feature/user-service
  commit id: "Реализована регистрация команд"
  merge main
  branch feature/analytic-service
  checkout feature/analytic-service
  commit id: "Добавлен модуль аналитики"
  merge main
```
