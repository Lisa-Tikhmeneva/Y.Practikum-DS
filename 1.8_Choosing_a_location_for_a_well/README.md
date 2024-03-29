# 1.8_Choosing_a_location_for_a_well

## Закончен 

Выбор места для скважины

## Цель исследования:
Необходимо решить, где бурить новую скважину.

Есть пробы нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов.

Построим модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль. Проанализируем возможную прибыль и риски техникой Bootstrap.

## Информация о датасетах
Три таблицы по трем регионам. Предобработка данных не потребовалась.

## Исследование моделей
Для трёх выбранных регионов данные были разбиты на обучающие и валидационные выборки. Было проведено обучение моделей с помощью линейной регресии. 

## Расчет прибыли
Рассчитали достаточный объём сырья для безубыточной разработки новой скважины.
Сравнили полученный объём сырья со средним запасом в каждом регионе.

Применили технику Bootstrap с 1000 выборок, чтобы найти распределение прибыли. Найдём среднюю прибыль, 95%-й доверительный интервал и риск убытков. Убыток — это отрицательная прибыль.

## Итоги исследования
 При начальном построении модели и предсказаний:
   - В регионах 0 и 2 достаточно высокий средний показатель запаса предсказанного сырья. Однако RMSE для данных регионов также высок (37.6 и 40 соответственно). Это свидетельствует о неоднозначности показателя, неточности модели регрессии.
   - В регионе 1 средний показатель запаса предсказанного сырья ниже остальных регионов. Однако RMSE в данном регионе мал (0.9). Это говорит о точности предсказаний и качестве построенной модели.
   - Средние показатели предсказанного сырья для одной скважины для всех регионов ниже теоретически необходимых.

При расчёте показателей для 200 наилучших скважин из выборочных 500:
   - Средний запас сырья с одной скважины среди всех регионов превосходит минимально необходимый объём.

При применении техники bootstrap:
   - Оценка средней прибыли максимальна для региона 1 (780 млн.р.).
   - Только регион 1 прогнозирует прибыльную разработку по 95%.доверительному интервалу.
   - Риск убытков для региона 1 (1.5%) Рекомендуем регион 1 для разработки.

