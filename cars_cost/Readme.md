# Оценка стоимости автомобилей.

**Описание проекта:**
Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение, чтобы привлечь новых клиентов. В нём можно будет узнать рыночную стоимость своего автомобиля.

**Цель проекта:**
Создать модель, которая будет определять рыночную стоимость автомобиля, на основе данных о технических характеристиках, комплектации и ценах других автомобилей и с учетом критериев заказчика:
  - качество предсказания;
  - время обучения модели;
  - время предсказания модели.
    
**Стек инструментов:** Pandas, Matplotlib, Seaborn, Numpy, Phik, Lightgbm

**Выводы:** В ходе исследования была проведена предобработка и подготовка данных для МО. 
Было обучено две простых модели линейной регрессии (LinearRegression, Ridge), DecisionTreeRegressor, а так же модель градиентного бустинга LightGBM.
Из простых моделей наиболее точной оказалась LinearRegression c метрикой RMSE на тренировочной выборке 2684.
Модель LightGBMRegressor показала на тренировочной выборке более высокую скорость обучения и предсказания по сравнению с линейной регрессией и при этом большую точность (RMSE лучшей модели при кросс-валидации - 1678).
Таким образом лучшей моделью в ходе проведенной работы стала модель LightGBM с 90 решающими деревьями. Метрика RMSE лучшей модели на тестовых данных составила 1671.
