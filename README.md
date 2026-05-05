# AI Prompt Library

> Библиотека модульных системных промптов для создания AI-ассистентов.

[![Version](https://img.shields.io/badge/version-v1.1-blue)]()

---

## Обзор

`AI Prompt Library` — это коллекция production-ready промптов для разных сценариев:

- Карьерные ассистенты
- Анализаторы резюме
- Коучи
- Обучающие AI-системы

Каждый промпт в библиотеке:

- Модульный (`base` + `modes`)
- Масштабируемый
- Имеет `prompt_card`
- Содержит примеры (`examples`)
- Поддерживает шаблонизацию (`templates`)

---

## Доступные промпты

| Промпт            | Описание                    | Статус                |
|-------------------|-----------------------------|-----------------------|
| `interview-coach` | Подготовка к собеседованиям | Готов к использованию |
| `resume-analyzer` | Анализ резюме               | Базовый каркас        |

---

## Архитектура проекта

```yml
prompt-library/
├── README.md
├── CHANGELOG.md
└── prompts/
    ├── interview-coach/
    │   ├── README.md
    │   ├── prompt_card.md
    │   ├── base/
    │   │   └── system_prompt.md
    │   ├── modes/
    │   │   ├── vacancy_analysis.md
    │   │   ├── questions.md
    │   │   ├── answer_practice.md
    │   │   └── self_presentation.md
    │   ├── templates/
    │   │   └── system_prompt_template.md
    │   └── examples/
    │       ├── vacancy_analysis_example.md
    │       ├── answer_practice_example.md
    │       └── self_presentation_example.md
    └── resume-analyzer/
        ├── README.md
        ├── prompt_card.md
        ├── base/
        │   └── system_prompt.md
        ├── modes/
        │   └── resume_analysis.md
        ├── templates/
        │   └── system_prompt_template.md
        └── examples/
            └── resume_analysis_example.md
```

---

## Контракт использования промпта

Рекомендуемая сборка системного промпта:

1. `BASE_PROMPT` — роль, стиль, ограничения
2. `MODE_BLOCK` — инструкции конкретного режима
3. `RAG_CONTEXT` — контекст из базы знаний (если есть)
4. `USER_INPUT` — запрос пользователя

Минимальный вход:

- `mode`
- `user_input`
- `rag_context` (опционально)

Ожидаемый выход:

- Структурированный ответ по секциям
- Конкретные рекомендации
- Отсутствие выдуманных фактов

---

## Стандарт нового промпта (Definition of Done)

Для каждого нового каталога в `prompts/` обязательно:

- `README.md` с описанием режимов и контракта вход/выход
- `prompt_card.md` (владелец, версия, цель, тэги)
- `base/system_prompt.md`
- минимум 1 файл в `modes/`
- минимум 1 файл в `examples/`
- `templates/system_prompt_template.md`

---

## Добавление нового промпта

1. Создать каталог внутри `prompts/`
2. Добавить обязательные файлы по стандарту выше
3. Проверить консистентность имен файлов и директорий
4. Обновить таблицу в корневом `README.md`
5. Добавить запись в `CHANGELOG.md`
