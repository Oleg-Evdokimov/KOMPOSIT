# Прогнозирование конечных свойств новых композиционных материалов
Выпускная квалификационная работа по курсу «Data Science» 

в Образовательном Центре МГТУ им. Н.Э. Баумана по теме: 

"Прогнозирование конечных свойств новых материалов (композиционных материалов)".

Целью данной работы является разработка пользовательского приложения для прогнозирования характеристики конечных свойств новых композиционных материалов.

1).	В процессе исследования изучены теоретические основы и методы решения поставленной задачи: 
Спрогнозировать по входным параметрам ряд конечных свойств получаемых композиционных материалов при следующих используемых признаках: 

    •	Соотношение матрица-наполнитель
    •	Плотность, кг/м3
    •	Модуль упругости, ГПа
    •	Количество отвердителя, м.%
    •	Содержание эпоксидных групп,%_2
    •	Температура вспышки, С_2
    •	Поверхностная плотность, г/м2
    •	Потребление смолы, г/м2
    •	Прочность при растяжении, МПа
    •	Потребление смолы, г/м2
    •	Угол нашивки, град
    •	Шаг нашивки
    •	Плотность нашивки

2).	Ознакомление с элементами, составляющими композитные материалы. 

3).	Проведен разведочный анализ и представлена визуализация предложенных данных. Представлены гистограммы распределения каждой из переменной, диаграммы ящика с усами, попарные графики рассеяния точек. В таблице представлены для каждой колонки среднее, медианное значение, проведен анализ и исключены выбросы, проверена выборка на наличие пропусков.

4).	Проведена предобработка данных (удалены шумы, нормализация и т.д.).

5).	Обучено нескольких моделей для прогноза модуля упругости при растяжении и прочности при растяжении. При построении модели было 30% данных оставлено на тестирование модели, на остальных происходило обучение моделей:

* методом опорных векторов

* методом случайного леса

* методом линейной регрессии

* методом градиентного бустинга

* методом К ближайших соседей

* методом деревья решений

* методом стохастического градиентного спуска

* методом многослойного перцептрона

* методом лассо регрессии


6).	Написаны 2 нейронные сети, которые будет рекомендовать соотношение "матрица-наполнитель".

7).	Разработано пользовательское приложение на Flask, выдаваемое прогноз (Выходные данные (прогнозируемы) - Соотношение "матрица - наполнитель").

8).	Оценена точность модели на тренировочном и тестовом датасете.

9).	Создан репозиторий в GitHub и размещен код исследования.

10). Оформлен данный файл README

Входные и выходные данные представлены в нормализованном виде. 
В ходе исследования было доказано, что взаимосвязь между переменными есть, но из-за маленького начального датасета точность прогноза не высока. Полученный результат является лишь шаблоном для создания реальной модели прогнозирования. Если получить доступ к большему объему информации, есть вероятность, что прототип приложения будет выдавать лучшие результаты. При продложении работы над проектом, на мой взгляд, есть большая вероятность реализовать новые методы и подходы. 

Структура репозитория:

Datasets - папка с 2 входными файлами (X_bp.xlsx - Первый датасет, X_nup.xlsx - Второй датасет (с нашивками))

Itog - папка в 2 "чистыми" данными (без шумов и выбросов), с которыми работаем над исследованием и приложением

App - папка с файлами для корректной работы пользовательского приложения, включая само приложение

Materials basalt - папка с некоторыми материалами в pdf по базальтопластику и композитным материалам

Подробный план работы.docx - файл с последовательностью работы над ВКР

Evdokimov O.G. BKP_final.pdf - код работы, выгруженный в pdf

Итоговый проект МГТУ DS требования.docx - файл с требованиями к оформлению работы и всеми задачами

Evdokimov O.G. BKP_final_1.ipynb - начало кода

Evdokimov O.G. BKP_final_2.ipynb - продолжение кода

Evdokimov O.G. BKP_final_3.ipynb - завершение кода

Evdokimov O.G. BKP_final_1.html - первая часть кода в html

Evdokimov O.G. BKP_final_2.html - вторая часть кода в html

Evdokimov O.G. BKP_final_3.html - третья часть кода в html

Evdokimov O.G. BKP_final_1.pdf - первая часть кода в pdf

Evdokimov O.G. BKP_final_2.pdf - вторая часть кода в pdf

Evdokimov O.G. BKP_final_3.pdf - третья часть кода в pdf

BKP_Evdokimov_presentazia_final.pdf - презентация ВКР  в формате pdf для защиты

BKP_Evdokimov_presentazia_final.pptx - презентация ВКР для защиты в формате pptx

Пояснительная записка Евдокимов О.Г..docx - описание работы на 39 стр в формате docx

Пояснительная записка Евдокимов О.Г..pdf - описание работы на 39 стр а формате pdf


Инструкция использования приложения:

Приложение позволяет решать задачу прогнозирования "Соотношение матрица наполнитель". 
Для получения прогноза необходимо 

а)     •	запустить app.py, 

б)     •	совершить запуск всех ячеек,  

в)     •	в появившейся строке ( * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)) - нажать на ссылку: http://127.0.0.1:5000/. 

г)     •	В новом открывшемся окне (сайте) ввести 12 входных параметров и нажать "Готово".

д)     •	в специальном разделе появится результат в виде числа с плавающей точкой. 


Автор: Евдокимов Олег Геннадьевич 

Выпускная квалификационная работа по программе повышения квалификации «Data Science» в обучающем центре МГТУ им. Н. Э. Баумана
2022 г. 

#UPD. В работе есть неточности. Где-то описки, где-то опечатки. Замечаю и исправляю их со временем. Возможно, в данный момент не запускается приложение, но это не точно. 

<div id ="sch" align="center">
<img src="https://komarev.com/ghpvc/?username==Oleg-Evdokimov&style=flat-square&color=blue" alt = ""/>
&style=flat-square&color=blue" alt = ""/>
</div>

