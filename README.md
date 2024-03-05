# <center> Проект 1: Анализ резюме из HeadHunter(SQL)

## Оглавление  
[1. Описание проекта](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Описание-проекта)  
[2. Задача](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Задача)  
[3. Краткая информация о данных](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Краткая-информация-о-данных)  
[4. Этапы работы над проектом](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Этапы-работы-над-проектом)  
[5. Результат](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Результаты)    
[6. Выводы](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Выводы) 

### Описание проекта    
Анализ базы банных HeadHunter с применением sql - запросов.

:arrow_up:[к оглавлению](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Оглавление)


### Задача    
Необходимо провести анализ базы данных HeadHunter, отражающей вакансии, размещенные работодателями, регионы нахождения вакансий, а также самих работодателей и их сферы деятельности.  


**Метрика качества**     
* Решение оформляется только в Jupyter Notebook;
* Решение оформляется в соответствии с ноутбуком-шаблоном;
* Каждое задание выполняется в отдельной ячейке, выделенной под задание (в шаблоне они помечены как ваш код здесь). Не следует создавать много ячеек для решения задачи — это провоцирует неудобства при проверке.
* Текст SQL-запросов и код на Python должны быть читаемыми. Не забывайте про отступы в SQL-коде.
* Выводы по каждому этапу оформляются в формате Markdown в отдельной ячейке (в шаблоне они помечены как ваши выводы здесь).
* Выводы можно дополнительно проиллюстрировать с помощью графиков. Они оформляются в соответствии с теми правилами, которые мы приводили в модуле по визуализации данных.
* Не забудьте удалить ячейку с данными соединения перед фиксацией работы в GitHub.


**Что практикуем**     
* Написание sql - запросов;
* Работу с GitHub.


### Краткая информация о данных
Для анализа были предоставлены 5 таблиц, содержащих следующую информацию:
1. Таблица Vacancies:
* Идентификатор вакансии (тип данных int4);
* Название вакансии (тип данных text);
* Ключевые навыки (тип данных text); 
* Тип рабочего графика (тип данных text);
* Требования к опыту (тип данных text);
* Тип трудоустройства (тип данных text);
* Нижняя граница зарплатной вилки (тип данных int4);
* Верхняя граница зарплатной вилки (тип данных int4);
* Идентификатор региона вакансии (тип данных int4);
* Идентификатор работодателя (тип данных int4).

2. Таблица Areas
* Идентификатор города (тип данных int4);
* Название города (тип данных text).

3. Таблица Employers
* Идентификатор работодателя (тип данных int4);
* Наименование работодателя (тип данных text);                               
* Идентификатор региона работодателя (тип данных int4).

4. Таблица Industries:        
* Идентификатор сферы деятельности (тип данных varchar(10));    
* Название сферы деятельности (тип данных text).                        

5. Таблица Employers_Industries: 
* Идентификатор работодателя (тип данных int4);                           
* Идентификатор сферы деятельности(тип данных varchar(10)).                      

  
:arrow_up:[к оглавлению](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Оглавление)


### Этапы работы над проектом  
**Предварительный анализ данных:**  
Первичное изучение данных: 
* Анализ размерности таблиц.


**Детальный анализ вакансий**
Анализ данных отражающих информацию о количестве вакансий, их месте нахождения и графиках работы, а также данные об необходимом опыте работы и о предлагаемой заработной плате:
* Анализ городов с максимальным количеством вакансий в отношении всего рынка труда;
* Анализ зарплатной вилки;
* Анализ наиболее востребованных рынком труда специалистов. 


**Анализ работодателей**
Анализ данных отражающих информацию о работодателях, их сферах деятельности, а также регионах, в которых работодатели публикуют свои вакансии:
* Анализ популярности регионов среди работодателей;
* Анализ сфер деятельности работодателей.


**Предметный анализ**
Анализ вакансий, в частности, поскольку интерес проекта сосредоточен на вакансиях в сфере IT, бы проведен анализ вакансий на позицию Data scientist (далее - DS).:
* Анализ количества вакансий junior (начинающий специалист) DS;
* Анализ ключевых навыков DS, а также их среднего количества;
* Анализ средних значений зарплатной вилки DS.

:arrow_up:[к оглавлению](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Оглавление)


### Результаты:  
В результате проделанной работы были написаны sql - запросы, позволяющие произвести анализ представленных данных.    

:arrow_up:[к оглавлению](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Оглавление)


### Выводы:  
Настоящая задача наглядно показывает работу специалиста Data Scientist, дает представление о будущей работе, помогает применить и отработать знания полученные на практике и подготавливает к дальнейшей профессиональной карьере.

:arrow_up:[к оглавлению](https://github.com/mrfluffypaws/Project_2.-HeadHunter-SQL-/blob/main/README.md#Оглавление)


Если информация по этому проекту покажется вам интересной или полезной, то я буду очень вам благодарен, если отметите репозиторий и профиль ⭐️⭐️⭐️-дами
