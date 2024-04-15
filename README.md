# Lab4-TensorFlow
*Лабораторная работа №4: Обучению первой модели на TensorFlow для распознавания рукописных цифр на датасете MNIST*

## Шаг 1: Загрузка и предобработка данных
- Импортируйте необходимые библиотеки: tensorflow и tensorflow.keras.datasets.mnist
- Загрузите датасет MNIST с помощью функции mnist.loaddata()
- Предобработайте данные: нормализуйте их, преобразуйте в нужный формат (например, масштабирование от 0 до 1)

## Шаг 2: Создание нейронной сети
- Используйте модель Sequential из библиотеки tensorflow.keras.models
- Добавьте слои к модели: открытый слой Flatten с inputshape=(28, 28), полносвязанный слой Dense с 128 нейронами и функцией активации ReLU, полносвязанный слой Dense с 10 нейронами и функцией активации softmax

## Шаг 3: Компиляция модели
- Компилируйте модель с оптимизатором 'adam', функцией потерь 'sparsecategoricalcrossentropy' и метрикой 'accuracy'

## Шаг 4: Обучение модели
- Используйте метод fit для обучения модели на обучающем наборе данных с указанием числа эпох (например, 5 эпох)

## Шаг 5: Оценка качества модели
- Используйте метод evaluate для оценки качества модели на тестовом наборе данных
- Выведите точность модели на тестовом наборе данных

## Шаг 6: Анализ результатов
- Импортируйте библиотеку matplotlib.pyplot для построения графика
- Постройте график кривой обучения (accuracy) с помощью данных из истории обучения
