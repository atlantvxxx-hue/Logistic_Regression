# Logistic_Regression
Проект посвящён анализу датасета по заявкам на кредиты и предсказанию их одобрения с использованием методов машинного обучения. Включает этапы предобработки данных, исследовательского анализа и построения базовой модели логистической регрессии.

Данные
Используется датасет "Eligibility Prediction for Loan" с Kaggle, содержащий 614 записей и 13 признаков:
Loan_ID – уникальный ID кредита
Demographic features: Gender, Married, Dependents, Education, Self_Employed
Financial features: ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History
Property_Area – тип местности (городская/сельская)
Target: Loan_Status (Y/N)

Основные этапы проекта
1. Предобработка данных
Удаление записей с пропусками
Отбор числовых признаков (ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History)
Разделение данных на обучающую и тестовую выборки
2. Базовое решение
Построение модели LogisticRegression
Оценка качества:
Accuracy на тесте: 82%
Высокая точность для класса "Y" (одобрено)
Низкая точность для класса "N" (отказ)
3. Исследовательский анализ данных (EDA)
Анализ распределения признаков
Разделение признаков на типы:
Бинарные: Gender, Married, Education, Self_Employed, Credit_History
Категориальные: Dependents, Property_Area
Числовые: финансовые показатели
Визуализация парных распределений (pairplot)

Результаты и выводы
Модель показывает хорошую общую точность, но:
Хуже предсказывает отказы (класс "N")
Признаки Credit_History и финансовые показатели наиболее значимы для предсказания

Технологии
Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn), Jupyter Notebook
Метрики: accuracy, precision, recall, F1-score
