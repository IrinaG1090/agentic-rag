# 🤖 Agentic RAG — AI-агент с инструментами

[![Python](https://img.shields.io/badge/python-3.12-blue)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/langchain-1.2.10-green)](https://langchain.com/)
[![Ollama](https://img.shields.io/badge/ollama-phi4--mini-purple)](https://ollama.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📝 О проекте

**Agentic RAG** — это интеллектуальный агент, который умеет не только отвечать на вопросы по документам, но и выполнять действия с помощью инструментов. Проект является четвёртым этапом большого плана по созданию единой мультиагентной системы, объединяющей Agentic RAG, GraphRAG и Multimodal RAG.

### ✨ Текущие возможности
- 🔢 **Калькулятор** — вычисление математических выражений
- 📄 **Поиск по документам** (заглушка, готовится интеграция с реальной векторной базой)
- 🧠 **ReAct-агент** — самостоятельно решает, когда и какой инструмент вызвать
- 🐳 **Локальный запуск** через Ollama (модель phi4-mini)

## 🛠️ Технологический стек

| Компонент | Технология |
|:---|:---|
| **Язык** | Python 3.12 |
| **Агентный фреймворк** | LangGraph (prebuilt React агент) |
| **Модель** | phi4-mini:3.8b-q4_K_M (локально через Ollama) |
| **Инструменты** | LangChain tools |
| **Оркестрация** | LangChain 1.2.10 |

## 📋 Предварительные требования

- Python 3.12+
- [Ollama](https://ollama.com) с установленной моделью `phi4-mini:3.8b-q4_K_M`
- Git (для клонирования)

## 🚀 Быстрый старт

### 1. Клонировать репозиторий
```bash
git clone https://github.com/IrinaG1090/agentic-rag.git
cd agentic-rag

### 2. Создать виртуальное окружение
```bash
python -m venv venv
source venv/bin/activate  # для Linux/Mac
.\venv\Scripts\activate    # для Windows

### 3. Установить зависимости
```bash
pip install langchain==1.2.10 langchain-ollama langgraph python-dotenv

### 4. Запустить Jupyter ноутбук
```bash
jupyter notebook notebooks/01_agent_basics.ipynb

📁 Структура проекта

agentic-rag/
├── notebooks/
│   └── 01_agent_basics.ipynb   # основной ноутбук с агентом
├── tools/
│   ├── __init__.py
│   ├── calculator.py            # инструмент-калькулятор
│   └── search.py                # инструмент поиска (заглушка)
├── .env                          # переменные окружения (опционально)
├── README.md                     # этот файл
└── requirements.txt              # зависимости

🧪 Примеры работы

# Агент автоматически выбирает инструмент
>>> "Сколько будет 25 * 4 + 10?"
✅ Вызывает calculate → результат: 110

>>> "Что такое in-context learning?"
📚 Ищет в документах (пока заглушка)

>>> "Вычисли 2 в 10 степени"
✅ Вызывает calculate → результат: 1024

🤝 Вклад в проект
Буду рада любым предложениям и улучшениям! Создавайте issue или отправляйте pull request.

📄 Лицензия
MIT License
