# Seminar 01 - Introduction to network visualization tools

## Prerequisites
* Please install gephi https://gephi.org/users/download/ for today's seminar and set up English Language.

![859bc3d2e4bf09d240115f3f9ec96e19.png](Images/859bc3d2e4bf09d240115f3f9ec96e19.png)

## Materials
* NetworkX [colab](https://colab.research.google.com/drive/1f-j5Zum7M-gjEdpR7AzXZcCDs17294Ei?usp=sharing)
 
 ### Data
* [edges](https://dl.dropboxusercontent.com/s/39k4aj05dbkbz8g/edges.csv) 
* [nodes](https://dl.dropboxusercontent.com/s/jt3fie6aedewirf/nodes.tsv) 

# Форматы файлов и средства работы с графами

## Graph data sources classification

1. Graph Databases
    * Graph Query languages
3. Relational Databases
    * SQL
3. Files
    * Common tables
    * Specific graph formats
    * Domain-oriented formats

## File formats

### Main formats

1. [Description](http://users.cecs.anu.edu.au/~bdm/data/formats.txt) of graph6, sparse6 and digraph6 encodings
2. [DOT](https://en.wikipedia.org/wiki/Dot) (graph-description,language)
3. [GraphML](http://graphml.graphdrawing.org/specification.html)
4. [GXL](http://www.gupro.de/GXL/) (Graph eXchange Language)
5. GML (Graph Modelling Language)
    * [from yFiles](https://docs.yworks.com/yfiles/doc/developers-guide/gml.html) 
    * [from Gephi](https://gephi.org/users/supported-graph-formats/gml-format/)

## Domain specific graph formats

1. [OpenBabel](http://openbabel.org/wiki/Main_Page)
[github](https://github.com/openbabel/openbabel/), [file formats](https://github.com/openbabel/documentation/tree/master/FileFormats)

## Data collection file formats

1. UCI Network [Data Repository Download](http://networkdata.ics.uci.edu/getting_started.php) formats
a.	[Pajek](http://mrvar.fdv.uni-lj.si/pajek/)
b.	[GML](https://networkx.org/documentation/networkx-1.9/reference/readwrite.gml.html)
c.	[GraphML](http://graphml.graphdrawing.org/)
d.	[DyNetML](http://www.casos.cs.cmu.edu/projects/dynetml/)

## Main implementations
1. graph-tool
2. [Snap](https://snap.stanford.edu/snappy/index.html) от Стенфордской группы
3. JGraphT - java библиотека с [питоновской обвязкой](https://medium.com/@dimitrios.michail/announcing-the-python-bindings-of-jgrapht-918d0cf386de).
4. stellargraph для эббеддингов
1. [NetworkX](http://networkx.org/) - a Python package for the creation, manipulation, and study of the structure, dynamics, and functions of complex networks
* *[*Converting to and from other data formats*](http://networkx.org/documentation/stable/reference/convert.html#)
2. [ReGraph](https://cambridge-intelligence.com/regraph/) - a Python package for advanced graph visualisation
* [*ReGraph tutorial*](https://cambridge-intelligence.com/python-graph-visualization-using-jupyter-regraph/)
3. [IGraph](https://igraph.org/) - Network analysis software
* [*Reading and Writing Graphs from and to Files*](https://igraph.org/c/doc/igraph-Foreign.html)
4. [Graphviz](http://graphviz.org/) - Graph Visualization Software
* [*The DOT Language*](http://graphviz.org/doc/info/lang.html)
5. [Gephi](https://gephi.org/) - the leading visualization and exploration software for all kinds of graphs and networks
* [*Supported Graph Formats*](https://gephi.org/users/supported-graph-formats/)
6. [Cytoscape](https://cytoscape.org/) - an open source software platform for visualizing complex networks 
7. [Graphjstry](https://www.graphistry.com/) - has a list of connectors
8. [NodeXL](https://www.smrfoundation.org/nodexl/) - add-in for Microsoft Excel that support social network and content analysis
9. [Socnetv](https://socnetv.org/): social network analysis and visualization software
* [*Supported Formats*](https://socnetv.org/docs/formats.html)
10. [vosviewer](https://www.vosviewer.com/) - a software tool for constructing and visualizing bibliometric networks
11. [CitNetExplorer](https://www.citnetexplorer.nl/) - a software tool for visualizing and analyzing citation networks of scientific publications
12. yworks [yed](https://www.yworks.com/products/yed)
    * [online demo](https://www.yworks.com/products/yfiles/demos)
13. [ogma](https://doc.linkurio.us/ogma/latest/) 
14. d3
15. [ibm i2](https://www.ibm.com/security/resources/demos/i2-analysts-notebook-demo/)
16. CASOS [ORA](http://www.casos.cs.cmu.edu/projects/ora/)

Интересное сравнение бенчмарков есть в статье [Benchmark of popular graph/network packages](https://www.timlrx.com/blog/benchmark-of-popular-graph-network-packages-v2) v2

## Publications and prototypes
1. [LargeViz](https://github.com/lferry007/LargeVis)
[github](https://github.com/elbamos/largeVis), [Visualizing Large-scale and High-dimensional Data](https://arxiv.org/abs/1602.00370)
2. [mars](https://github.com/marckhoury/mars) - a graph drawing tool for large graph visualization
3. [Interactive Graph Layout of a Million Nodes](https://www.mdpi.com/2227-9709/3/4/23/htm)

## Nice visualizations

# Graph Vizualization

* [Network Repository](https://networkrepository.com/)
    * [Cora in Network Repository](https://networkrepository.com/graphvis.php?d=./data/gsm50/labeled/cora.edges)

- julesvernestrilogy.com
- [internet-map.net](http://internet-map.net) / webverse.org

* Статья по визуализации графов от iggisv9t [хабр](https://habr.com/ru/company/ods/blog/464715/), [towardsdatascience](https://towardsdatascience.com/large-graph-visualization-tools-and-approaches-2b8758a1cd59) 
* Еще одна визуализация от Deep Graph Library [блог](https://www.dgl.ai/blog/2019/02/17/gat.html)

* Хороший гайд по [yFiles Automatic Graph Layout](https://www.youtube.com/watch?v=AkR6r1FbRdY)
    * [yEd](https://www.yworks.com/yed-live/) - Live Graph Editor
    * [Layout-Styles Demo](https://live.yworks.com/demos/layout/layoutstyles/index.html) (offers more settings)

## References
* "[A survey of two-dimensional graph layout techniques for information visualisation](https://dl.dropboxusercontent.com/s/p4aoaxpyij0ml7x/1473871612455749.pdf)" [@gibsonSurveyTwodimensionalGraph2013]
* "[What Would a Graph Look Like in This Layout? A Machine Learning Approach to Large Graph Visualization](https://arxiv.org/pdf/1710.04328.pdf)" [@kwonWhatWouldGraph2018]
