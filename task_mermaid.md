# Task Mermaid Examples

Полная коллекция примеров диаграмм и графиков Mermaid.

---

## 1. Блок-схема (Flowchart)

### 1.1 Простая блок-схема
```mermaid
flowchart TD
    A[Начало] --> B{Условие}
    B -->|Да| C[Действие 1]
    B -->|Нет| D[Действие 2]
    C --> E[Конец]
    D --> E

flowchart LR
    A([Начало]) --> B[Процесс]
    B --> C{Решение}
    C -->|Да| D[[Подпрограмма]]
    C -->|Нет| E[(База данных)]
    D --> F>Ввод/Вывод]
    E --> F
    F --> G((Конец))

flowchart TB
    Start([Старт]) --> Input[/Ввод данных/]
    Input --> Process[Обработка]
    Process --> Check{Проверка}
    Check -->|OK| Output[/Вывод результата/]
    Check -->|Ошибка| Error[Обработка ошибки]
    Error --> Input
    Output --> End([Финиш]

flowchart TD
    subgraph Frontend[Фронтенд]
        A[Пользователь] --> B[UI]
    end
    subgraph Backend[Бэкенд]
        C[API] --> D[Бизнес-логика]
        D --> E[(БД)]
    end
    B --> C

flowchart LR
    A[Задача] --> B[В работе]
    B --> C[Готово]
    
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#ff9,stroke:#333
    style C fill:#9f9,stroke:#333

## 2. Диаграмма последовательности (Sequence Diagram)
### 2.1 Базовая диаграмма

sequenceDiagram
    participant A as Клиент
    participant B as Сервер
    participant C as База данных
    
    A->>B: Запрос данных
    B->>C: SQL запрос
    C-->>B: Результат
    B-->>A: Ответ
