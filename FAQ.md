# Вопросы

## 1. Что такое матрица смежности и матрица инцидентности?

Понятное определение есть в wikipedia:
* [матрица смежности](https://en.wikipedia.org/wiki/Adjacency_matrix)
* [матрица инцидентности](https://en.wikipedia.org/wiki/Incidence_matrix)

## 2. Что такое транспонирование матриц ?

[Транспонирование](https://wiki.loginom.ru/articles/transpose.html) — это операция над матрицами в результате которой матрица поворачивается относительно своей главной диагонали. При этом столбцы исходной матрицы становятся строками результирующей. Например, если мы имели матрицу актеров, снявшихся в различных фильмах, то при транспонировании мы получим матрицу фильмов, в которых играли различные актёры.

## 3. Как работают проекции (projection) ?

Небольшой [гайд по проекциям](https://colab.research.google.com/drive/1kAX9kDvN8fA-SIsIobEWVgzqwzuUZiw2?usp=sharing)

## 4. Как загрузить граф из networkx в gephi ?
При первом запуске можно импортировать gexf. Gephi откроет сохраненный файл через стандартное меню просмотра, главное правильно указать тип файла (.gexf)
```
nx.write_gexf(G, "test.gexf")
```
Иногда нужно измененить атрибуты уже существующего графа. Тогда лучше импортировать только вершины как таблицу и выбирать опцию "объединение" в лаборатории данных Gephi.


## 5. Как выгрузить подписки и подписчиков из VK ?

Для этого можно использовать методы [users.getSubscriptions](https://vk.com/dev/users.getSubscriptions) и [groups.getMembers](https://vk.com/dev/groups.getMembers). Более подробно об авторизации и использовании VK API можно узнать в [статье на хабре](https://habr.com/ru/post/319178/)

## 6. Какой алгоритм укладки используется по умолчанию в networkx ?

Как следует из [документации networkx](https://networkx.org/documentation/networkx-1.11/reference/generated/networkx.drawing.layout.fruchterman_reingold_layout.html), по умолчанию используется `spring_layout`, он же `fruchterman_reingold_layout`.

## 7. Какие форматы графов поддерживает networkx?

Как следует из [документации networkx](https://networkx.org/documentation/stable/reference/readwrite/generated/networkx.readwrite.gml.read_gml.html), поддерживаются следующие форматы:
* Adjacency List
* Multiline Adjacency List
* Edge List
* GEXF
* GML
* Pickle
* GraphML
* JSON
* LEDA
* SparseGraph6
* Pajek
* GIS Shapefile
* Matrix Market
