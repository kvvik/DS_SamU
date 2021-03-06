# Инструменты анализа данных

© Бибиков С.А., к.т.н., доцент

© Евдокимова В.В., ассистент преподавателя 

Кафедра суперкомпьютеров и общей информатики, Самарский университет

## Лекция 1. Да кто такой этот ваш анализ данных?..

Содержание:

0. [Правила игры для группы ПМФ 6306 в 2022 году](https://github.com/kvvik/DS_SamU/blob/main/GAMERULES_6306.md)

1. Что такое анализ данных?
2. Чем data analyst отличается от data scientist?
3. Задачи которые решаются в анализе данных.
4. Практическая часть курса.
5. Порядок лекций и практических занятий.

## 1. Что такое анализ данных?

Большинство определений термина "Анализ данных" сходится к двум основным смысловым определениям:
1. Область математики (информатики, компьютерных наук ...) занимающаяся созданием методов, алгоритмов и инструментов, нацеленных на извлечение знаний из предоставленных данных (экспериментально полученных).
2. Процесс преобразования исходных (экспериментальных, реальных) данных в целях извлечения полезной информации и последующего принятия решений.

Как выглядит работа по анализу данных:
1. У заказчика анализа возникает Вопрос - потребность получить дополнительные неочевидные данные из доступной информации. Вопрос может быть из области бизнеса (где построить новую торговую точку, что влияет на продажи конкретных товаров в магазине, какие тренды покупательского интереса и т.д.), может быть из области техники (при каких условиях механизм выходит на неустойчивые режимы работы или потребляет больше энергии, какие факторы внешней среды не были учтены при проектировании, как скоро образец техники потребует профилактический осмотр и т.д.), могут быть чисто научными (какие процессы происходят при столкновении частиц в ускорителе, что влияет на поведение удаленной звездной системы, как связано изменение интенсивности измеренного освещения и параметры дифракционного отражателя).
2. Специалист по анализу данных изучает вопрос и осуществляет выбор данных, которые ему потребуются для последующей обработки. Какие данные позволят получить ответ на вопрос или найти новую закономерность (для Больших Данных). Если данные еще не собраны, то также нужно описать особенности сбора этих данных для минимизации шума, ошибок и прочих негативных факторов.
3. Специалист готовит данные. Выбирает наиболее значимую их часть, отбрасывает нерелевантные значения или особые случаи, убирает тривиальные случаи, проводит статистическую предобработку, если нужно. Разделяет данные для обучения и для верификации модели, если это необходимо.
4. Специалист обучает модель, если это необходимо для решения поставленной задачи. Для простой задачи вообще может понадобиться только получение определенного среза данных для проведения сравнения с использованием простейших агрегатных функций (суммы, минимума, максимума и т.д.).
5. Специалист проверяет адекватность полученной модели с использованием части данных с предыдущего шага. Если модель не удовлетворяет проверочным данным, то специалист возвращается к шагу 4, 3 или 2. Это зависит от дополнительного анализа получаемых результатов.
6. Модель используется для прогнозирования (в том числе классификации или сегментирования новых данных), определения новых взаимосвязей, получения оценок и т.д.
7. Полученные данные интерпретируются, визуализируются и подготавливаются к презентации для людей, которые будут принимать решения на основе полученной информации. Заказчик получает ответ на Вопрос.

## 2. Чем data analyst отличается от data scientist?

Почитать можно следующие источники: [Интервью ФКН с data scientist из Янедекса](https://cs.hse.ru/news/454940789.html), [Обзор вопроса в рамках стороннего онлайн курса](https://biconsult.ru/services/data-analyst-vs-data-scientist-v-chem-razlichie).

Если обобщить информацию, то помимо _data analyst_ (аналитик данных) и _data scientist_ (пусть будет ученым по данным) есть еще одна схожая профессия _data mining specialist_ (специалист по добыче данных). 

Будем пока использовать английские названия, так проще всего понять, о ком именно идет речь. Итак...

__Data analyst__ - аналитик. Задача аналитика провести анализ, то есть разложение предоставленной информации для получения выводов, необходимых для бизнеса. Чаще всего очень плотно работает с менеджментом в бизнесе. Получает от них запросы на простом человеческом языке; подбирает простые, хорошо известные способы для преобразования имеющейся информации; получает цифры, которые превращает в красочные и понятные презентации для менеджмента, в ходе которых формулируется управляющие решения. Обладает знаниями в области: предмета ведения бизнеса, ведения бизнеса (по крайней мере в курсе используемых бизнес-процессов), презентации, начал статистики, мощных инструментов автоматизированного анализа и презентации (даже тот же Excell), программирования (немного, да и не обязательно).

__Data mining specialist__ - специалист по добыче данных. Этот профессионал нужен, когда самих данных еще нет, и нет даже представления о том, какие данные помогут получить ответ. Он занимается выбором информации, которую нужно собрать, учитывает особенности сбора информации, проводит полноценную подготовку собранной информации перед обработкой, а после обработки способен сделать прогноз развития в выбранной предметной области. Обладает знаниями в области: математики (статистики, к примеру), программирования (несколько рабочих языков программирования, необходимые библиотеки, машинное обучение), подготовки данных (чистые особенности подготовки данных, не обязательно с научной точки зрения), Большие Данные. По моим представлениям это ближе всего к тому, чем должен заниматься студент ПМФ в процессе своего обучения.

__Data scientist__ - обладает навыками двух предыдущих специалистов, при этом обладает фундаментальными теоретическими знаниями в области анализа данных. То есть способен не только модифицировать процесс получения данных, и сами данные, но и инструменты анализа данных. Если кратко, то это в первую очередь ученый. Знания, которыми обладает, те же, что и двое предыдущих специалистов. Кроме этого, уровень знаний хотя бы в одной области должен быть очень высоким. Скорее всего умеет хорошо работать с Большими Данными.

Что такое __Большие Данные__ (_Big Data_) - область анализа данных, отличающаяся большими объемами собранной информации, которая не обязательно обладает высокой релевантностью. Если вы к информации о продажах разных групп товаров добавите информацию о наличии, магазинов конкурентов рядом, погоде, плотности населения, пробках, расстояния до остановок, занятости парковки, возможно вы сможете выделить закономерность продаж спортивной обуви в феврале, что позволит вам скорректировать маркетинговую политику или продумать успешную рекламную акцию.

## 3. Задачи, которые решаются в анализе данных.

В вашем портфолио отсутствуют дисциплины, связанные с анализом данным, поэтому в процессе изучения мы часто будем отвлекаться на сопутствующие знания. 
Какие классы задач будем рассматривать в курсе анализа данных.

1. Введение в Python. 
2. Манипуляции с массивами данных. Способ организации доступа к элементам массивов, хранящих различные данные. Библиотека NumPy. Понятия датафрейма и библиотека Pandas.
3. Визуализация данных. Способ отображения определенных взаимосвязей для данных. Способы интерпретации графической информации. Графические библиотеки, содержащие инструменты визуализации.
4. Машинное обучение. Общие подходы и правила. Библиотеки. Методика обработки данных. Кросс-валидация. Модели машинного обучения.
5. Классификация (и сегментация). Задачи классификации с учителем и без учителя. Различные подходы к построению разделяющих (классивицирующих правил).
6. Линейная регрессия. Простейший инструмент прогнозирования. Реализация в библиотеках.


## 4. Практическая часть курса.

Все обучение будет проходить на примере языка Python. Выбор этого языка обусловлен наличием удобных и популярных библиотек для проведения анализа данных.
Для работы полезно будет использовать для работы следующие инструменты: среда разработки PyCharm - профессиональную версию можно получить бесплатно как студенту с использованием корпоративной почты; среда представления результатов Jupiter Notebook - позволяет совмещать исполняемый код и размеченный текст в одном документе, что существенно упрощает процесс проверки лабораторных работ; опционально git система (система контроля версий) - полезнейший инструмент для личного пользования и для совместной разработки, позволяет контролировать различные версии конечного продукта (документа, программного обеспечения, отчета и т.д.).

___TBD: ссылки на источники ПО. Порядок получения лицензий и т.д.___

__Python:__

[Выбрать версию интерпретатора Python](https://www.python.org/downloads/).

[Бесплатная версия IDE для студентов](https://www.jetbrains.com/ru-ru/community/education/#students) - потребуется получение персональной корпоративной почты в домене ssau.ru.

__Jupiter Notebook:__

[Установка Jupiter Notebook под Python](https://jupyter.org/install) - работает через браузер.

[Онлайн сервис от Google для создания Jupiter Notebook'ов](https://colab.research.google.com/) - можно не ставить среду разработки, все вычисления выполняются в облаке, могут быть особенности работы.

__GitHub:__

[Система контроля версий](https://github.com/) - работает из под PyCharm и отдельно через браузер.

## 5. Порядок лекций и практических занятий.
___TBD: Порядок следующих лекций, объем и их расписание.___
