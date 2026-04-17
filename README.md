# 📚 Book Recommender System

Система рекомендации книг на основе **коллаборативной фильтрации** с веб-интерфейсом на Streamlit.

## 🎯 О проекте

Данный проект представляет собой **End-to-End** систему рекомендации книг, которая:

- Загружает и обрабатывает датасет с Kaggle (Book Recommendation Dataset)
- Выполняет очистку и валидацию данных
- Строит матрицу "пользователь-книга"
- Обучает модель коллаборативной фильтрации (Nearest Neighbors)
- Предоставляет веб-интерфейс для получения 5 рекомендаций похожих книг

## 🛠 Технологии

| Категория | Технологии |
|-----------|------------|
| **Язык** | Python 3.7+ |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn (NearestNeighbors) |
| **Веб-интерфейс** | Streamlit |
| **Конфигурация** | PyYAML |
| **Сериализация** | Pickle |

## 🚀 Установка и запуск

### Предварительные требования

- Python 3.7 или выше
- Conda (рекомендуется) или venv

### 1. Клонирование репозитория

```bash
git clone https://github.com/your-username/Book-Recommender-System.git
cd Book-Recommender-System
```

### 2. Создание виртуального окружения (Conda)

```bash
conda create -n books python=3.9 -y
conda activate books
```

### 3. Установка зависимостей

```bash
pip install -r requirements.txt
```

### 4. Настройка конфигурации

Убедитесь, что файл `config/config.yaml` содержит правильные пути и URL для скачивания датасета.

### 5. Запуск обучения модели

```bash
python main.py
```

Это запустит **End-to-End** пайплайн обучения:

* Загрузка данных с Kaggle
* Валидация и очистка данных
* Трансформация (построение сводной таблицы)
* Обучение модели NearestNeighbors

### 6. Запуск веб-приложения

```bash
streamlit run app.py
Приложение откроется в браузере по адресу http://localhost:8501
```

Приложение откроется в браузере по адресу `http://localhost:8501`
