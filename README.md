# Алгоритм k-means для набора данных open food facts with pyspark

data - https://world.openfoodfacts.org/data

Notebook для очистки данных включен в репо

## Для запуска ноутбука вам нужен pyspark на вашем компьютере. Команда для запуска программы:
- spark-submit k-means.py

После программы появится следующее окно :

![Screenshot from 2023-08-20 10-11-42](https://github.com/stpic270/Big_data_fifth_lab/assets/58371161/7221054a-599f-4f54-921b-bb62a2648d28)

рис 1

Это метод локтя (elbow method) для выбора правильного количества кластеров в зависимости от SSE, лучшие решения - 4 кластерa.

### Алгоритм k-means для набора данных open food facts

K-means — это алгоритм на основе центроида или алгоритм на основе расстояния, в котором мы вычисляем расстояния, чтобы назначить точку кластеру. В K-Means каждый кластер связан с центроидом.

Первое свойство алгоритма кластеризации K-средних

![image](https://github.com/stpic270/Big_data_fifth_lab/assets/58371161/a71828b1-0feb-40cd-a800-34340307fa05)

рис. 2

K-means — это алгоритм на основе центроида или алгоритм на основе расстояния, в котором мы вычисляем расстояния, чтобы назначить точку кластеру. В K-Means каждый кластер связан с центроидом.

#### Первое свойство алгоритма кластеризации K-средних

Все точки данных в кластере должны быть похожи друг на друга (рис. 2)

Если клиенты в конкретном кластере не похожи друг на друга, то их требования могут различаться. Если банк сделает им такое же предложение, оно может им не понравиться, и их интерес к банку может снизиться.

Наличие схожих точек данных в одном кластере помогает банку использовать целевой маркетинг.

#### Второе свойство алгоритма кластеризации K-средних

Точки данных из разных кластеров должны быть максимально разными.

![image](https://github.com/stpic270/Big_data_fifth_lab/assets/58371161/d1625b2b-c5d6-49ed-879a-3e7ccdc3ea13)

рис. 3

Случай 1 (рис. 3)
Покупатели в красном и синем кластерах очень похожи друг на друга. Четыре верхних точки в красном кластере обладают теми же свойствами, что и два основных клиента в синем кластере. У них высокие доходы и высокая стоимость долга.

![image](https://github.com/stpic270/Big_data_fifth_lab/assets/58371161/8ddc5027-9c44-4288-8f8d-a7e6ef7d99e0)

рис. 4

Случай 2 (рис. 4)
Точки в красном кластере полностью отличаются от клиентов в синем кластере. Все клиенты в красном кластере имеют высокий доход и большую задолженность, в то время как клиенты в синем кластере имеют высокий доход и низкую стоимость долга. Очевидно, что в этом случае мы имеем лучшую кластеризацию клиентов.

Следовательно, точки данных из разных кластеров должны максимально отличаться друг от друга, чтобы иметь более значимые кластеры. Алгоритм k-средних использует итеративный подход для поиска оптимальных назначений кластеров путем минимизации суммы квадратов расстояний между точками данных и назначенным им кластерным центроидом.

Links с теорией и git с очисткой датасета:

1) https://www.analyticsvidhya.com/blog/2019/08/comprehensive-guide-k-means-clustering/
2) https://github.com/JadeBlue96/OpenFoodFacts-EDA/tree/master
