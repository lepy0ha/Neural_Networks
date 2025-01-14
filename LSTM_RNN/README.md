Вот README для вашего нового файла `LSTM_RNN.ipynb`.

---

# Проект: Текстовая Генерация с Использованием LSTM RNN

Этот проект использует рекуррентную нейронную сеть с LSTM для генерации текста на основе входного корпуса. Модель обучается на текстовом файле и может создавать новые текстовые последовательности в стиле исходных данных.

## Содержание

- [Технологии](#технологии)
- [Установка](#установка)
- [Описание модели](#описание-модели)
- [Пример использования](#пример-использования)
- [Результаты](#результаты)

## Технологии

Проект использует следующие технологии и библиотеки:
- Python
- NumPy
- TensorFlow/Keras (для создания и обучения LSTM-модели)
- Matplotlib (для визуализации результатов)

## Установка

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/lepy0ha/NN/LSTM_RNN.git
   ```
2. Установите необходимые зависимости:
   ```bash
   pip install -r requirements.txt
   ```

## Описание модели

Цель проекта — обучить модель на текстовом корпусе и использовать её для генерации текста. Модель принимает начальный текст и прогнозирует следующую последовательность символов, что позволяет ей создавать осмысленный текст, который имитирует стиль и содержание исходных данных.

 - Основные этапы
   - **Предобработка текста**:
Исходный текст преобразуется в последовательности символов, где каждый символ заменяется на индекс, основанный на его частоте.
Это помогает модели лучше понимать структуру текста и частоту использования различных символов.
   - **Создание модели**:
Модель построена с использованием PyTorch и включает LSTM-слой, который позволяет ей "запоминать" последовательности символов.
Обучается модель на фрагментах текста, что позволяет ей улавливать контекст и структуру фраз.
   - **Генерация текста**:
После обучения модель способна принимать начальный текст (или символ) и генерировать следующую последовательность.
Это достигается с помощью функции evaluate, которая добавляет новые символы к начальной последовательности, предсказывая каждый последующий символ.


### Архитектура модели
Модель построена с использованием LSTM-слоёв, которые способны захватывать долгосрочные зависимости в данных. Архитектура включает несколько LSTM-слоёв и полносвязный выходной слой для генерации предсказаний.

## Пример использования

В файле `LSTM_RNN.ipynb` представлен пример, который включает:
1. Подготовку данных временного ряда.
2. Обучение модели LSTM на основе временных данных.
3. Оценку точности модели и визуализацию предсказаний.

### Запуск проекта
1. Подготовьте текстовые данные. Поместите текстовый файл в папку data и укажите его путь в TRAIN_TEXT_FILE_PATH.
2. Запустите обучение модели. Используйте ячейки в LSTM_RNN.ipynb, чтобы обучить модель.
3. Генерация текста. После обучения можно вызвать функцию evaluate для генерации текста


