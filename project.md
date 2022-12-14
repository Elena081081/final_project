# ПРИМЕНЕНИЕ IT-ТЕХНОЛОГИЙ ПРИ ПРОВЕДЕНИИ ФАКТОРНОГО АНАЛИЗА ИЗМЕНЕНИЯ НАЛОГА НА ПРИБЫЛЬ

## Проблема, которую будет решать проект

### Для чего нужен факторный анализ прибыли для самой организаций?
Деятельность любой коммерческой компании направлена на получение прибыли. На общее изменение прибыли в текущем периоде по отношению к предыдущему или изменение фактических показателей прибыли по отношению к плану влияют следующие основные факторы:
* объем продажи продукции;
* ассортимент реализуемой продукции;
* себестоимость реализуемой продукции;
* расходы, связанные с реализацией продукции.

Таким образом, с помощью факторного анализа можно определить основные причины изменения величины прибыли и составить план на следующие периоды по объемам выпуска, ассортимента и реализации продукции, а также спрогнозировать расходы, связанные с ее производством и реализацией. Такие аналитические мероприятия позволяют увеличить доходы и сократить расходы организации, и как следствие увеличить прибыль компании. Основная цель проведения такого анализа для компании - найти способы увеличить доходность фирмы. Данные исследования проводятся на основании данных бухгалтерской отчетности.

### Налоговики тоже проводят факторный анализ прибыли. Для чего?
В современном мире сложно представить деятельность любой, даже самой маленькой организации, без проверок контролирующих органов, в частности налоговых инспекций. Почти ежедневно организации и индивидуальные предприниматели получают требования от налоговых органов о представлении пояснений, информации, документов, о внесении изменений в отчетность. Крупнейшие компании страны уже привыкли ежемесячно предоставлять пояснения об изменениях налога на прибыль в текущем периоде по отношению к аналогичному периоду прошедшего года. Как правило, у бухгалтеров часто не хватает времени на то, чтобы провести и предоставить результаты факторного анализа в том объеме и с той тщательностью, которые хотят видеть налоговики. Это не прихоть и не каприз конкретного инспектора, а требования ведомства, чтобы иметь оперативную информацию о положении финансового состояния компаний и делать максимально точными свои прогнозы о будущих поступлениях в бюджет.

Как показывает практика, ежемесячно проводить такой анализ по каждой компании самим налоговикам достаточно трудоёмко. В начале проведения такого анализа инспектор имеет данные налоговых деклараций и несколько десятков таблиц в формате Excel, каждую из которых нужно проанализировать и выбрать из нее нужную информацию и построить причинно-следственные связи между всеми таблицами. Как правило на анализ одной компании может уходить 1-2 дня. Это катастрофически много. Цель моего проекта с помощью применения технологий Excel, SQL, Python и Power BI максимально автоматизировать процесс проведения факторного анализа прибыли и тем самым сократить временные затраты рабочего времени.

### Факторный анализ через отчёты в 1С:Предприятие. Что не так?
Для проведения факторного анализа требуются аналитические таблицы и расчеты. Их составление и работа с ними – очень трудозатратный по времени процесс, требующий консолидации огромного объема данных. Можно воспользоваться специализированными инструментами, предустановленными в продуктах 1С. Так, например, в отчете «Сравнение продаж аналогичных периодов» можно проанализировать по периодам в натуральном выражении объемы продаж товаров (продукции, работ или реализации услуг), а также их прирост в процентном выражении в сравнении по периодам. В этом же отчете можно провести и анализ в количественном и стоимостном выражении в сравнении по периодам. Из этого отчета мы получим информацию о следующих факторах влияния: количество, выручка, себестоимость, валовая прибыль.
Анализируя его, можно сделать вывод о том, что именно пользуется наибольшим спросом в конкретном периоде. Данные этих отчетов содержат агрегированные показатели по обобщенным аналитическим группировкам и могут быть использованы для принятия обоснованных **управленческих и организационных решений**. Для факторного анализа, проводимого налоговыми органами, такие отчеты не раскрывают необходимой информации. При этом другая часть компаний ведет свой учет в SAP, в котором отсутсвуют унифицированные отчеты как в 1С:Предприятие. 

### Порядок проведения факторного анализа без автоматизации. В чём сложность для налоговиков?
Все компании для целей налогового контроля можно разделить на две большие группы:
* компании, которые находятся на особой форме контроля в виде налогового мониторинга;
* все остальные.

В первую группу компаний входят крупнейшие налогоплательщики страны, как правило, с огромной филиальной сетью. При переходе на налоговый мониторинг они предоставляют в налоговый орган доступ к копии базы данных, с которой инспектор может работать только на просмотр с возможностью выгружать все необходимые регистры налогового и бухгалтерского учета, либо витрину базы данных со связанными файлами в формате Excel. Все остальные компании, естественно, могут предоставить только аналитические регистры. 
Цель факторного анализа для налоговиков - выявить не только изменения объема продаж, себестоимости товаров, расходов, связанных с реализацией по конкретной товарной группе, а определить финансово-хозяйственные отношения с какими контрагентами, какие конкретные сделки и их условия оказали влияние на изменение прибыли.

    Для проведения такого анализа необходимо последовательно пройти ряд шагов:

1) Проанализировать строки налоговых деклараций за аналогичные периоды текущего и предыдущего года, выявить строки с наибольшими расхождениями. Для этого в Excel создаем таблицу, состоящую из нескольких столбцов: в первом столбце указываем названия показателей (строк налоговых деклараций), второй и третий столбец содержат данные по текущему и аналогичному периоду прошлого года, в четвертом и пятом столбцах рассчитываются отклонения каждого из показателей в абсолютных и относительных величинах.
2) По строкам с наибольшими отклонениями следует выбрать соответствующий налоговый (аналитический) регистр, который дает расшифровку строк, установленных в первом пункте. Далее по аналогии с первым пунктом создаем таблицу с пятью столбцами с наименованием строк регистров, показателей двух периодов и отклонениями. Регистр может иметь более глубокие расшифровки, то есть для дальнейшего анализа нам придется "проваливаться" все глубже и продолжать создавать все новые таблицы.
3) Далее в зависимости от настроек базы данных можно дойти сразу до первичного документа (договор/контракт, приложения и модификации к ним, счет-фактура, инвойс, бухгалтерская справка, платежный документ и т.д.), либо через бухгалтерские проводки попасть в карточку бухгалтерского счета и только потом выйти на первичный документ.

Таким образом, необходимо свести данные из нескольких больших таблиц как минимум за два периода (а поскольку, налог на прибыль считается нарастающим итогом, то с каждым новым месяцем или кварталом объемы анализируемых данных увеличиваются в разы), прийти к конкретной сделке и выявить причинно-следственные связи. В результате этих действий мы установим одну сделку по одному контрагенту.
Кроме того, еще одна большая проблема заключается в том, что не только в каждой отрасли, но и в каждой компании перечень регистров сильно отличается (компании разрабатывают их самостоятельно согласно своей учетной политике).

***Основная проблема, которую я хочу решить в дипломном проекте, это максимально упростить и сократить временные затраты на проведение факторного анализа изменения налога на прибыль, сделать этот процесс менее трудоемким и освободить время специалистов, занимающихся этим вопросом, для решения более важных задач.***

### Пример проведения факторного анализа на яблоках

Представим, что есть компания "Овощи - фрукты", которая занимается оптовой торговлей овощей и фруктов. Закуп товара компания производит в южных регионах России, а затем своими силами доставляет товар на свои склады в Москве. У компании в собственности несколько складов, один из них свободен, поэтому руководством принято решение сдавать его в аренду. В компании трудятся директор, его заместители, бухгалтеры, логисты, менеджеры по продажам, водители, грузчики. 

Проведем факторный анализ изменения налога на прибыль компании "Овощи - фрукты". В данном разделе будет представлен максимально упрощенный вариант такого анализа, для понимания что же это такое.

**Первый шаг.** 

Нам нужно взять информацию из итогового листа (лист 02) налоговых деклараций по налогу на прибыль за два сравниваемых периода:

***Таблица 1***

Показатели | 2021, руб.| 2020, руб. | Абсолютное отклонение, руб.| Относительное отклонение, %
:--------:|:-------:|:------:|:------:|:--------:
1 | 2 | 3 | 4 | 5
Доходы от реализации| 120 000 | 160 000 | - 40 000 | - 25
Внереализационные доходы| 30 000 | 70 000 | - 40 000 | - 57
Расходы, уменьшающие сумму доходов от реализации| 80 000 | 60 000 | + 20 000 | + 33
Внереализационные расходы | 50 000 | 20 000 | + 30 000 | + 150
Налоговая база | 20 000 | 150 000 | - 130 000 | - 87
**Налог на прибыль (Налоговая база х 20%)** | **4 000** | **30 000** | **- 26 000** | **- 87**


Проанализируем представленную таблицу. Мы видим, что в 2021 году величина прибыли (налоговая база) уменьшилась на 130 000 руб. или на 87 %, соответствующие изменения произошли и с самим налогом на прибыль. Давайте разберемся, почему это произошло. Первое, что мы можем отметить, это одновременное снижение доходов от реализации и внереализационных доходов. При этом сумма расходов увеличилась, как за счет расходов, уменьшающих сумму доходов от реализации, так и внереализационных расходов.

**Второй шаг.**

Далее нам нужно определить, за счет каких товарных групп произошло снижение доходов, и какие статьи расходов оказали максимальное влияние на их увеличение.

**Доходы от реализации** складываются из доходов от продажи овощей и фруктов. Пусть наша компания торгует тремя видами овощей: помидорами, огурцами и картофелем, и тремя видами фруктов: яблоками, грушами и персиками.

***Таблица 2***

Товары | 2021, руб.| 2020, руб. | Абсолютное отклонение, руб.| Относительное отклонение, %
:--------:|:-------:|:------:|:------:|:--------:
1 | 2 | 3 | 4 | 5
Овощи| 50 000 | 40 000 | + 10 000 | + 25
Фрукты| 70 000 | 120 000 | - 50 000 | - 42
**Доходы от реализации** | **120 000** | **160 000** | **- 40 000** | **- 25**


В этой таблице мы расшифровали строку "Доходы от реализации" из Таблицы 1. Из Таблицы 2 мы видим, что снижение доходов от реализации произошло за счет снижения доходов от продажи фруктов, в то время как доходы от продажи овощей увеличились. Теперь посмотрим как именно изменились доходы от продажи по каждой группе фруктов.

***Таблица 3***

Вид фруктов | 2021, руб.| 2020, руб. | Абсолютное отклонение, руб.| Относительное отклонение, %
:--------:|:-------:|:------:|:------:|:--------:
1 | 2 | 3 | 4 | 5
Яблоки| 10 000 | 30 000 | - 20 000 | - 67
Груши| 20 000 | 50 000 | - 30 000 | - 60
Персики| 40 000 | 40 000 | 0 | 0
**Доходы от реализации фруктов** | **70 000** | **120 000** | **- 50 000** | **- 42**


Из таблицы 3 делаем вывод, что доходы от продажи персиков остались на прежнем уровне, а доходы от продажи яблок и груш упали. Причем в абсолютном выражении большее снижение произошло по товарной группе "Груши", а в относительном - по группе "Яблоки". Теперь посмотрим, как изменилась структура покупателей яблок и груш.

***Таблица 4***

Покупатели яблок | 2021, руб.| 2020, руб. | Абсолютное отклонение, руб.| Относительное отклонение, %
:--------:|:-------:|:------:|:------:|:--------:
1 | 2 | 3 | 4 | 5
Катюша| 0 | 5 000 | - 5 000 | - 100
Ромашка| 3 000 | 15 000 | - 12 000 | - 80
Сказка| 7 000 | 10 000 | - 3 000 | - 30
**Доходы от реализации яблок** | **10 000** | **30 000** | **- 20 000** | **- 67**


***Таблица 5***

Покупатели груш | 2021, руб.| 2020, руб. | Абсолютное отклонение, руб.| Относительное отклонение, %
:--------:|:-------:|:------:|:------:|:--------:
1 | 2 | 3 | 4 | 5
Василек| 0| 30 000 | - 30 000 | - 100
Лукоморье| 5 000 | 5 000 | 0 | 0
Аленушка| 0 | 15 000 | - 15 000 | - 100
Братья Гримм| 15 000 | 0 | + 15 000 | + 100
**Доходы от реализации груш** | **20 000** | **50 000** | **- 30 000** | **- 60**


Из анализа таблицы 4 следует, что за год у нас уменьшилось количество покупателей, полностью прекращены поставки в компанию "Катюша". На 80 процентов снизились доходы от компании "Ромашка" и на 30 процентов от компании "Сказка". Из таблицы 5 мы видим, что полностью прекратились поставки груш в компании "Василек" и "Аленушка", при этом появился новый покупатель - компания "Братья Гримм". 

После того, как мы выяснили хозяйственные отношения с какими контрагентами и по каким товарным позициям привели к наибольшим изменениям, мы можем открыть таблицу с договорами, найти необходимые договоры в базе данных и выяснить, в связи с чем произошло снижение поставок, или другими словами, какой фактор привел к этим изменениям. Например, величина поставок осталась неизменной, но снизилась цена на товар; или же все таки уменьшилась величина поставок; или договор был расторгнут в середине анализируемого года; вариантов может быть много.

Таким образом, идя от самой первой таблицы, мы пошагово анализируем, какой фактор оказал влияние на тот или иной показатель. При этом мы анализируем не только факторы, которые привели к уменьшению доходов (как в примере), но и те, что повлияли на их рост. Аналогично будем поступать и с расходами: определять факторы, которые повлияли как на увеличение расходов, так и на их снижение. Процесс проведения факторного анализа я сравнила бы с веером. Мы начинаем проводить сравнительный анализ данных за два периода, исходя из одной строки декларации - суммы налога на прибыль (соответственно и налоговой базы). Далее переходим к сравнению доходов, которые распадаются на доходы от реализации и внереализционные доходы. Дальнейший анализ доходов представлен на Схеме 1. С каждым новым шагом количество анализируемых данных увеличивается в разы. Можно сказать, что мы спускаемся с вершины горы к подножию. Если перевернуть схему, то мы как раз увидим веер данных. По такой же схеме мы будем анализировать внереализационные доходы, затем расходы, связанные с производством и реализацией продукции, и внереализационные расходы. 

***Схема 1***

Доходы от реализации - Строка декларации    |  
:--------:|
*****************************************************
Товары    | Работы  | Услуги 
:--------:|:-------:|:------:
***********************************
Группы товаров| Группы работ| Группы услуг 
:--------:|:-------:|:------:
***************************************
Группа товаров 1 | ГТ 2 | ГТ 3 | Группа работ 1 | ГР 2 | ГР 3 | Группа услуг 1 | ГУ 2 | ГУ 3
:---:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:
**********************************************
Покупатель № 1 ГТ 1 | ....... | Покупатель № n ГТ n | Заказчик № 1 ГР 1 | ....... | Заказчик № n ГР n | Заказчик № 1 ГУ 1 | ....... | Заказчик № n ГУ n
:---:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:
*************************************************
Договор № 1 | .......... | .......... | .......... | .......... | .......... | .......... | .......... | ..........| ..........|  Договор № n
:---:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:
****************************************************
Фактор № 1 | ....... | ....... | ....... | ....... | ....... | ....... | ....... | .......| .......| .......| .......| .......| Фактор № n
:---:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:


Мы видим, что проведение факторного анализа вручную (пусть даже и с использованием стандартных средств Excel) достаточно трудозатратно. И это мы рассмотрели расшифровку самой простой строки декларации "Доходы от реализации". Анализ расходов сложнее в разы в связи с их делением на прямые и косвенные. Для наглядности приведу таблицу с очень обобщенной группировкой расходов в небольшой организации на примере нашей компании "Овощи-фрукты", для понимания объема анализируемой информации.

***Таблица 6***

Статья расходов | Расшифровка 1 уровня | Расшифровка 2 уровня | Расшифровка 3 уровня | Расшифровка 4 уровня
:--------:|:-------:|:------:|:------:|:--------:
1 | 2 | 3 | 4 | 5
Прямые расходы, связанные с реализацией| Товарные группы | Основные поставщики | Договор | Фактор / Причина
Расшифровываем прямые расходы, связанные с реализацией | Помидоры / Огурцы / Картофель / Яблоки / Груши / Персики | Айвенго / Робин Гуд / Ланселот / ... Компания N | Договор_1 ... Договор_N | Фактор_1 ... Фактор N
Заработная плата работников / Страховые взносы| Разбиваем на прямые и косвенные расходы в зависимости от места возникновения | - | - | -
Транспортные расходы| Товарные группы | Исполнитель | Договор | Фактор / Причина
Коммунальные услуги | Разбиваем на прямые и косвенные расходы в зависимости от места возникновения | - | - | - 
Амортизация | Разбиваем на прямые и косвенные расходы в зависимости от места возникновения | - | - | - 
**Итого расходов, связанных с реализацией** | **-** | **-** | **-** | **-**


## Технологии, используемые в проекте

В своем проекте я буду использовать несколько основных инструментов аналитика: **Excel, Python, SQL, PowerBI**. Моя задача не только оптимизировать процесс проведения факторного анализа по налогу на прибыль, но и подойти к ее решению индивидуально в зависимости от величины компании, ее оборотов и формы контроля. Вне зависимости от перечисленных критериев работа будет начинаться с Excel.

На входе мы имеем несколько таблиц в формате Excel, которые мы будем использовать для создания реляционной модели базы данных. Последовательно будем строить связи между таблицами посредством использования первичных и внешних ключей, и в итоге создадим логическую модель базы данных, с которой будем работать. Логическую модель можно построить, используя онлайн-приложение Draw.io, вкладку "Сущность-Связь". Эта модель поможет нам как при составлении сложных запросов в SQL, так и при написании кодов на языке Python.

Для небольших компаний, количество записей в отдельных таблицах которых не превышает 1 000 000 строк, для оптимизации факторного анализа можно использовать Excel с применением логических формул, сводных таблиц, макросов и построением по результатам проведенного анализа дашбордов.

Для компаний, налоговые регистры которых имеют расшифровки в несколько миллионов строк, будем использовать более сильные инструменты: язык запросов SQL и скриптовый язык программирования Python. Для преобразования полученной информации в наглядные графики и диаграммы воспользуемся одним из самых популярных среди аналитиков инструментом визуализации данных - системой Power BI (business intelligence).

Мой проект основан на регистрах налогового учета одной компании. В регистрах сохранены все строки, но цифровые значения взяты условные, без привязки к финансовым показателям конкретной организации. В моей работе не будет таблиц с несколькими миллионами строк контрагентов и сделок, поэтому я автоматизирую процесс проведения факторного анализа с использованием всех указанных ранее информационных технологий. Все из инструментов хороши по своему, рассмортим краткую характеристику и возможности каждого из них.

***Excel***. Для решения поставленной задачи в Excel я буду использовать макросы, которые позволят переложить на программу большую рутинную работу по обработке данных. Мы будем использовать Excel не только в качестве табличного редактора. Помимо этого, с помощью встроенного языка Visual Basic, мы напишем программу, которая решит поставленную задачу.

***Python***. Как уже отмечалось выше, Excel хорош, когда нужно проанализировать небольшое количество данных, но для масштабных вычислений он не подходит. Язык программирования Python позволяет напрямую подключаться к базе данных и выполнять обновления автоматически. С его помощью можно проводить расчеты, создавать отчеты или динамические дашборды. В Excel многое надо вводить вручную, а обновления нельзя автоматизировать.

***SQL***. В отличие от Excel SQL - это не программа, а язык составления структурированных запросов. Как уже указывалось выше, на входе мы имеем несколько таблиц, данным в этих таблицах мы присвоим идентификаторы (id). В результате вся информация будет структурирована не в одной громоздкой таблице, а в множестве маленьких и «легких», связанных между собой особенными отношениями таблиц. Таким образом, мы уменьшаем объемы файлов с информацией. Они занимают меньше места на диске, время выполнения запросов сокращается, система работает быстрее. На языке SQL пишутся специальные запросы к базе данных с целью получения данных или их корректировки. Задав правильный запрос к базам, мы сможем создать новые таблицы, извлекать данные, удалять, фильтровать и т.п.

***Power BI***. Это мощная платформа для бизнес-аналитики и подготовки интерактивных отчетов. В ней можно анализировать большое количество данных из разных источников, преобразовывать цифры в понятные отчеты. В режиме онлайн отслеживать изменения показателей на динамических дашбордах. Работа в Power BI сводится к трем последовательным действиям: сначала нужно загрузить данные из Excel (или любой другой базы данных); потом сгруппировать их по показателям и обработать и преобразовать расчеты в интерактивные графики.

На выходе сравним, насколько удалось оптимизировать проведение факторного анализа посредством каждого из инструментов, и какой из них для решения поставленной задачи наиболее эффективный.

## Инструкция, как это сделать

### Построение логической модели с помощью онлайн-приложения *Draw.io*

Изначально у нас есть несколько таблиц в формате Excel. На основании этих таблиц мы должны выстроить структуру базы данных, с которой будем работать. Модель нашей базы данных будем строить в онлайн-приложении Draw.io.
Запускаем приложение и открываем вкладку ***"Сущность-связь"*** (находится с левой стороны). Выбираем объект Table, перетаскиваем в рабочую область и начинаем последовательно заполнять все поля. Приложение само предлагает нам заполнить поля ***PK*** и ***FK***.
- На первом шаге для каждой таблицы необходимо создать ***Первичный ключ (Primary Key - PK)***. Первичный ключ используется для идентификации записей в таблице, чтобы каждая запись стала уникальной. Для этого присвоим каждой строке в каждой таблице свой ***id-номер***. Для объединения двух таблиц, помимо первичного ключа, понадобится внешний ключ. ***Внешний ключ (Foreign Key - FK)*** - это столбец-ссылка, каждое значение внешнего ключа одной таблицы обязательно соответствует первичному ключу другой таблицы.
- На втором шаге следует определить связи между таблицами. В реляционных базах данных существуют связи: ***Один к одному, Один ко многим, Многое ко многому***. При выборе связей в Draw.io обращаем внимание на их "хвостики" - две чёрточки обозначают один, "гусиная лапка" - много.
