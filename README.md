# Библиотека промптов

# AI Prompt Library

> Библиотека промптов для создания ассистентов на основе искусственного интеллекта.

[![Version](https://img.shields.io/badge/version-v1.0-blue)]()

---

## Обзор

AI Prompt Library — это коллекция production-ready системных промптов
для создания AI-ассистентов разных направлений:

- Карьерные ассистенты
- Анализаторы резюме
- Коучи
- Обучающие AI-системы

Каждый промпт:
- Модульный
- Масштабируемый
- Имеет prompt card
- Имеет тест-кейсы

---

## Доступные промпты

| Промпт           | Описание                    | Статус.      |
|------------------|-----------------------------|--------------|
| ainterview-coach | Подготовка к собеседованиям | Тест         |
| resume-analyzer  | Анализ резюме               | В разработке |

---

## Архитектура проекта

'''
prompt-library/
│
├── README.md
├── CHANGELOG.md
│
├── prompts/
│   │
│   ├── interview-coach/
│   │   ├── README.md
│   │   ├── prompt_card.md
│   │   │
│   │   ├── base/
│   │   │   └── base_prompt.md
│   │   ├── modes/
│   │   │   └── vacancy_analysis.md
│   │   │   └── questions.md
│   │   │   └── answer_practice.md
│   │   │   └── self_presentation.md
│   │   ├── templates/
│   │   │   └── system_prompt_template.md
│   │   └── examples/
│   │   │   └── vacancy_analysis_example.md
│   │   │   └── answer_practice_example.md
│   │   │   └── self_presentation_example.md
│   │
│   └── resume-analyzer/
'''


## Добавление нового промпта
 
1. Создать каталог внутри prompts/
2. Добавить в этом каталоге необходимые подкаталоги и файлы с описанием в них:
- base
- template
- examples
- modes
3. Обновить главный README.md проекта
