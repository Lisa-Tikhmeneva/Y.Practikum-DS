# 1.7_Customer_leave_research

## Закончен 

Исследование ухода клиентов

## Цель исследования:
Из банка каждый месяц по-немногу стали уходить клиенты. Сохранять текущих клиентов дешевле, чем привлекать новых.

Нужно построить модель для прогноза, уйдёт клиент из банка в ближайшее время или нет. Модель должна быть с предельно большим значением F1-меры (0.59 и выше). Дополнительно измеряем AUC-ROC, сравниваем её значение с F1-мерой.


## Информация о датасее

Исторические данные о поведении клиентов и расторжении договоров с банком из источника данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

## Подготовка данных
Разделим исходные данные на обучающую, валидационную и тестовую выборки. Исследуем качество разных моделей, меняя гиперпараметры. Проверим качество модели на тестовой выборке.

## Исследование моделей
Построили и протестировали следующие модели:
   - Решающее дерево
   - Случайный лес
   - Логистическая регрессия


## Итоги исследования

Метрики логистической регрессии и дерева решений не дотянули до необходимого порога.
