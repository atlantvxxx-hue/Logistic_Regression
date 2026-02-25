# Logistic_Regression
Проект посвящён анализу датасета по заявкам на кредиты и предсказанию их одобрения с использованием методов машинного обучения. Включает этапы предобработки данных, исследовательского анализа и построения базовой модели логистической регрессии.

Данные
Используется датасет "Eligibility Prediction for Loan" с Kaggle, содержащий 614 записей и 13 признаков:
Loan_ID – уникальный ID клиента
Demographic features: Gender, Married, Dependents, Education, Self_Employed
Financial features: ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History
Property_Area – тип местности (городская/сельская)
Target: Loan_Status (Y/N)

Основные этапы проекта
1. Предобработка данных
Анализ распределения признаков
Разделение признаков на типы:
Бинарные: Gender, Married, Education, Self_Employed, Credit_History
Категориальные: Dependents, Property_Area
Числовые:ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term
Визуализация
Кодирование пропусков
Стандартизация и OneHotCodding
Разделение данных на обучающую и тестовую выборки
3. Базовое решение
Построение модели LogisticRegression
Оценка качества:
Accuracy на тесте: 82%
Высокая точность для класса "Y" 
Низкая точность для класса "N" по метрике precision

Результаты и выводы:
Модель показывает хорошую общую точность, но:
Хуже предсказывает отказы (класс "N")
Признаки Credit_History и числовые признаки наиболее значимы для предсказания

Технологии
Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn), Jupyter Notebook
Метрики: accuracy, precision, recall, F1-score

P.s Улучшил модель, добавив балансировку с помощью комбинации undersampling и oversampling. Показатель по категории "N" на тестовой выборке увеличились с 0.55 до 0.68 (+=21%).
