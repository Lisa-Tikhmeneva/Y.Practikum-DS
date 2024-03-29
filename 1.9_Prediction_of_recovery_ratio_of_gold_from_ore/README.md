# 1.9_Prediction_of_recovery_ratio_of_gold_from_ore

## Закончен 

Предсказание коэффициента восстановление золота из руды

## Цель исследования:
Подготовим прототип модели для «Цифры». Компания создаёт решения для более эффективной работы промышленных предприятий.

Модель будет предсказать коэффициент восстановления золота из золотосодержащей руды. Используем данные с параметрами добычи и очистки. Это поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.
## Информация о датасетах
Данные находятся в трёх файлах:
   - gold_recovery_train_new.csv — обучающая выборка;
   - gold_recovery_test_new.csv — тестовая выборка;
   - gold_recovery_full_new.csv — исходные данные.

Данные индексируются датой и временем получения информации (признак date). Соседние по времени параметры часто похожи.

Некоторые параметры недоступны, потому что замеряются и/или рассчитываются значительно позже. Из-за этого в тестовой выборке отсутствуют некоторые признаки, которые могут быть в обучающей. Также в тестовом наборе нет целевых признаков.

Исходный датасет содержит обучающую и тестовую выборки со всеми признаками.

## Подготовка данных
   - добавили в тестовую выборку целевые признаки
   - убрали из тренировочной выборки лишние столбцы с онлайн признаками
   - убрали пропуски из выборок

## Анализ данных
Посмотрели на:
  - изменение концентрация металлов и соли (Au, Ag, Pb, Sol) на различных этапах очистки
   - распределения размеров гранул сырья на обучающей и тестовой выборках
   - суммарную концентрацию всех веществ на разных стадиях: в сырье, в черновом и финальном концентратах

## Исследование моделей
Чтобы оценивать модели, введём новую метрику sMAPE, опишем её в функциях.
Модели:Решающее дерево, Случайный лес, Линейная регрессия.
Обучим и оценим их качество кросс-валидацией.

## Итоги исследования
Модель случайного леса показала лучшие результаты для тестовой выборки, для неё final sMAPE для обучающей выборки получилась 7.93%, а для тестовой 7.16%.
