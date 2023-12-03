# HSE_ML_HW1

Домашнее задание 1. 

Курс: Машинное обучение. 

Автор: Куроедов Виктор


## Задача:
В ходе задание необходимо было построить линейные модели машинного обучения для набора данных о стоимости автомобилей, в зависимости от заданных атрибутов. Также для лучшей из полученных моделей необходимо реализовать API сервис, который "оборачивает" лучшую из моделей в доступный для пользователя интерфейс

## Описание файлов:

`HW1_Regression_with_inference` - ноутбук с аналитикой и процессом построения моделей
`cars_train.csv` - данные для тренировки моделей
`cars_test.csv` - данные для оценки качества получаемых моделей
`ridge_model.pikle` - коэффициенты для модели
`scaler.pikle` - коэффициенты скэйлинга для модели

## Ход работы и основные выводы

1. Был проведен простейший EDA, в ходе которого были проанализированы и заполненны пропуски в данных, визуализированы попарные распределения признаков для трейновой и тестововй выборок, а также проанализировано распределение целевой переменной
2. Были построены основные модели с использованием количественных признаков (в т.ч. Lasso и Ridge регрессии). Для подбора оптимальных параметров использовался `GridSearch`. Для оценка качества использовались метрики MSE и $R^2$.
4. Далее были добавлены категориальные признаки, закодированные методом OneHotEncode. Они дали существенный прирост качества модели и в качетсве финальной версии модели была выбрана Ridge-регрессия.
