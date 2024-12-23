# Распознавание результатов общего анализа крови

## Введение

Целью этого проекта является диагностика общего анализа крови (нормальный результат / отклонение от нормы) и выдача рекомендаций по поводу "срочности" обращения к врачу, назначившему тот или иной анализ. Он включает анализ данных, предварительную обработку данных и применение моделей машинного обучения для составления прогнозов.


## Описание проекта

Проект состоит из следующих основных этапов:
1) Импорт необходимых библиотек и наборов данных
2) Знакомство с данными
3) Предварительная обработка и очистка данных
4) Обработка мультиколлирнеарности
5) Разделение данных на тренировочную и валидационную выборки
6) Настройка гиперпараметров для моделей машинного обучения
7) Обучение моделей 
8) Сравнение результатов
9) Реализация "срочности"

## Импортированные библиотеки

В данном проекте использовались ключевые библиотеки:
* Pandas
* NumPy
* Seaborn
* Matplotlib
* Scikit-learn
* CatBoost

## Параметры, рассматриваемые в CSV-файле

1) *'ID истории болезни'*: ID пациента;
2) *'Осн. диаг. при выписке МКБ10 (текст)'*: диагноз пациента при выписке из стационара;
3) *'Заголовок документа'*: название анализа из которого был взят тот или иной показатель крови;
4) *'Кол. лаб. показатель'*: название показателя крови;
5) *'Значение кол. показателя'*: числовое значение этого показателя;
6) *'Ед. изм. кол. показателя'*: единицы измерения этого показателя;
7) *'Норма кол. показателя'*: референсный интервал нормы для данного показателя;
8) *'Флаг нормы кол. показателя'*: результат относительно референсного интервала (Пониж/Норм/Повыш);
9) *'Кач. лаб. показатель'*: данный признак содерджит в себе строку "комментарий";
10) *'Значение кач. показателя'*: непосредственно сам комментарий;
11) *'Норма кач. показателя'*: дополнение к комментарию;
12) *'Пол'*: пол пациента (М/Ж);
13) *'Дата рождения пациента'*: дата рождения пациента в формате ГГГГ-ММ-ДД ЧЧ:ММ:СС.

## Короткое описание

Целью данного проекта было:
1) Проанализировать данные;
2) Обучить следующие модели и сравнить результаты:
    * Logistic Regression;
    * Decision Tree;
    * Random Forest;
    * Cat Boost.
3) Дополнить предсказания лучшей модели выводом "срочности" обращения к врачу, назначившему анализ.

## Заключение

Выполняя шаги, описанные в этом репозитории, вы можете получить представление о наборе данных, выбрать наиболее релевантные функции и создать прогностические модели, которые помогут в анализе показателей крови.