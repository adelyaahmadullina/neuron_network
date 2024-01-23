Создание нейросетевой модели для автоматической обработки естественного языка с использованием методов attention
===========
[Данные, нужные для запуска кода](#title1)

[Запуск кода](#title2)

[Как работает код](#title3)

[Результат работы кода](#title4)

## <a id="title1">Данные, нужные для запуска кода</a>
Нейр_сети_Ахмадуллина.ipynb - основная программа   
Датасет [IMDB Dataset.csv](https://drive.google.com/file/d/1BU5CPG4ksZ9-oO514GIECU5QKUUMkPjX/view?usp=drive_link)

## <a id="title2">Запуск кода</a>
Загрузите  [IMDB Dataset.csv](https://drive.google.com/file/d/1BU5CPG4ksZ9-oO514GIECU5QKUUMkPjX/view?usp=drive_link) в Google Colab.  
<img width="194" alt="image" src="https://github.com/adelyaahmadullina/neuron_network/assets/120652605/5c7fbe61-d1c4-41a6-ba8e-b2a47e18436b">


Или в Kaggle:  
![image](https://github.com/kurrosan/DataAnalysis/assets/120035199/5346a717-48c4-4725-8b34-bce180cf0d7f)

После этого запустите код 
После выполнения всего кода, у нас появится файл с названием submition.csv
![image](https://github.com/kurrosan/DataAnalysis/assets/120035199/81125b73-6254-4bcc-994a-57c5f900b21e)


## <a id="title3">Как работает код</a>
Этот код выполняет задачу анализа данных и построения модели классификации на основе Random Forest для определения мошеннических транзакций с кредитными картами. Загружаются необходимые библиотеки для работы с данными, построения модели и визуализации. Данные о транзакциях считываются из CSV-файла. Выделяются функции (признаки) и целевая переменная из данных. Данные разделяются на обучающий и тестовый наборы для оценки производительности модели. Создается и обучается модель Random Forest на обучающих данных. Модель применяется к тестовым данным для получения предсказаний. Рассчитываются метрики точности, матрица ошибок и отчет о классификации. Проводится поиск оптимальных параметров модели с использованием кросс-валидации. Выводятся лучшие параметры, найденные в результате GridSearchCV. Создается DataFrame с важностью признаков на основе обученной модели. Модель оценивается с использованием кросс-валидации для проверки ее обобщающей способности. Используется RandomOverSampler для балансировки классов в обучающем наборе. Важность признаков визуализируется с использованием столбчатой диаграммы. 


### В представленном коде есть несколько интересных и примечательных моментов:

1. Борьба с несбалансированными данными:
Используется библиотека imbalanced-learn, а именно RandomOverSampler, для увеличения количества экземпляров минорного класса (мошеннические транзакции) и балансировки классов.

2. Настройка параметров модели с помощью GridSearchCV:
Применяется метод кросс-валидации для поиска оптимальных параметров модели Random Forest. Это улучшает обобщающую способность модели и помогает избежать переобучения.

3. Визуализация важности признаков:
После настройки параметров модели строится столбчатая диаграмма важности признаков, что позволяет легко определить, какие функции оказывают наибольшее влияние на предсказания модели.

## <a id="title4">Результат работы кода</a>
Результатом работы является получение файла c предсказанием submition.cs
