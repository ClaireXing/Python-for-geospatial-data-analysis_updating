# Python-for-geospatial-data-analysis
Python for geospatial data analysis

### Overview:

地学空间分析对应一套融合几何关系和地理特征在内的数据处理方法。与常见的图像/矢量图形不同，地理数据带有投影坐标、几何特征索引、配套属性信息（矢量文件中对应dbf文件保存的属性链接表格，栅格文件对应多波段影像），因此，处理方法与传统数据不同。

配套ArcGIS/QGIS等软件可以实现一大部分基本的空间数据处理与分析功能，但当我们需要处理大量数据时，例如大尺度研究（多城市、全国、全球），用软件设置参数、可视化、批处理等难以一键完成，要调整或者重复的操作很多（我前阵子就是这样，挺费时间）。因此必须上coding啊。这个repository整理并分享用比较多的python空间数据处理和分析方法库，以供参考。

Geospatial analysis corresponds to a set of data processing methods that integrate geometric relations and geographic information. Different from common image/vector graphics, geographic data has its own projection systems, geometric features, and joint attribute information (for vector files, it's the attribute link table saved in the 'dbf' file; for raster files, it's multiple bands of images). Therefore, the processing method is not the same as traditional data. 

Supporting ArcGIS/QGIS and other software can realize most of the basic spatial data processing and analysis functions. Nonetheless, when we need to process a large amount of data, such as in large-scale research (national or even global), parameter adjusting, visualizing, batch processing, etc. can not complete with one click using those softwares, since there are many adjustments or repeated operations (I used software for data processing and visiualization before, which takes a lot of time). All these will be much faster with CODE. This repository organizes and shares a series of python spatial data processing and analysis techniques in python for reference.

### Several useful tools (updating):

1. [Geopandas](https://geopandas.org/)

   对**矢量数据的属性操作、空间运算**非常适合。它沿用了pandas的框架和大部分操作，将相同函数直接扩展到对shp的操作，所以非常好入门。绘制地图也和pandas绘图基本类似。适合于一些初始简单的EDA，还不能提供更多复杂的空间分析功能。

   基于包：pandas——满足基本的空间数据属性操作，shapely——几何图形操作的高级接口，fiona——文件访问与读写，descartesand matplotlib——绘图。

   Suitable for **attribute analysis and spatial operations on vector data**. It follows the Pandas framework, directly extending the same functions on SHP, so it's vary easy to learn. Mapping functions are similar to drawing plots in pandas. It is suitable for initially exploratory data analysis, but can not yet provide much complex spatial analysis. 

   Packages it builts on: Pandas -- for basic spatial data attribute operations, Shapely -- high-level interface for geometric operations, FIONA -- for file access, Descartes and Matplotlib -- drawing maps.

2. [GDAL/OGR](https://gdal.org/)

   GDAL是**栅格处理神器**，适合于各种栅格操作，**但！安装时貌似会覆盖你现有的python版本（它目前自带python3.6版本），一定要小心！养成新建环境的好习惯！（血泪教训）**

   OGR是GDAL项目的分支，是对矢量数据提供支持。目前是在做矢量栅格化的时候用这个比较多，别的功能还没有用到（毕竟有了geopandas满足基本需求），之后碰到了会继续更新。

   GDAL is a raster processing tools suitable for a variety of raster operations. But! It will overwrite your existing Python version (it comes with Python 3.6 now), so beeee careful!! Get in the habit of creating a new environment! (You know why I say this. /(ㄒoㄒ)/)

   OGR, a branch of the GDAL project, supports vector data. It is currently used mostly for vector rasterization, and I have not yet try more other functions (geopandas, after all, satisfies basic requirements). I will updated this part as soon as I found more interesting functions.

3. [Pysal](https://pysal.org/)

   这个包针对地理空间矢量数据，提供了很多**时空分析与建模**的模块，非常丰富，可以满足不少地学经典统计、空间建模及挖掘的需求，是前面两个数据处理为重心的包在空间分析进阶版。

   This package provides a plenty of modules for spatio-temporal analysis, specific for geospatial vector data. The diverse functions can meet the needs of many geospatial statistics, modeling and mining. It is the advanced version of the previous two packages, which mainly focus on data processing in spatial analysis.