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

## 💡 Как использовать веб-приложение

1. Обучение модели (ещё не обучена)

* Нажмите кнопку *"Train Recommender System"*
* Дождитесь завершения обучения (появится сообщение "Training Completed!")

2. Получение рекомендаций

* Выберите книгу из выпадающего списка
* Нажмите кнопку *"Show Recommendation"*
* Система покажет 5 похожих книг с обложками

### Пример работы

<img width="880" height="386" alt="img1" src="https://github.com/user-attachments/assets/16d10c6c-de90-42a3-adcb-3a7e45210393" />

<img width="884" height="663" alt="img2" src="https://github.com/user-attachments/assets/6a5d1cf3-29b6-4e26-a589-29b22e67ef99" />

<img width="876" height="724" alt="img3" src="https://github.com/user-attachments/assets/7fd5a3b0-17cb-467f-a119-9d83990ee431" />

## 📚 Источник данных
[Book Recommendation Dataset on Kaggle](https://www.kaggle.com/datasets/ra4u12/bookrecommendation?resource=download&select=BX-Books.csv)

Датасет содержит:

+ *BX-Books.csv* — информация о книгах (ISBN, название, автор, год, издатель, URL обложки)
+ *BX-Book-Ratings.csv* — оценки пользователей (User-ID, ISBN, Book-Rating)
+ *BX-Users.csv* — демографические данные пользователей (не используется в текущей версии)
