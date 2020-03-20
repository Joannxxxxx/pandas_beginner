# ROUND ONE - 10 minutes to pandas
## DAY ZERO 
### 20200314 周六

[下载 anaconda](https://www.anaconda.com/distribution/#download-section)

* Hello Python - 在 Anaconda 中打开 Jupyter Notebook，打印出 Hello Python 

## DAY ONE
### 20200315 周日

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)

#### Object creation

* import - 载入 numpy 及 pandas，并命名为 np 与 pd
* Series - 仿照示例创建包含如下元素的 Series 对象：2,4,6,8,10,np.nan
* DataFrame - 按照示例创建 DataFrame 对象（两个）

## DAY TWO
### 20200316 周一

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)

#### Object creation

* dtype - 按照示例查看 DataFrame 的数据类型
* TAB - 延续昨日的操作，在输入 df2. 后按下 tab 键（在键盘上数下第三行左一），会出现可供使用的函数。**请使用此功能查看 df2 的 index**。（提示：完整代码为 df2.index 。你可以输入 df2.in 之后按下 tab 键，在看到选择框后使用键盘上的方向键（在键盘右下区域）选择需要的函数，选中后按回车键）
  
#### Viewing data
* head - 仿照示例查看 df 前 4 行（关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/version/0.23.1/generated/pandas.DataFrame.head.html)）
* tail - 仿照示例查看 df 末 4 行(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/version/0.23.4/generated/pandas.DataFrame.tail.html))

## DAY THREE
### 20200317 周二

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
  
#### Viewing data
* index - 按照示例查看 df 的 index（关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.index.html)）
* columns - 按照示例查看 df 的 columns(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.columns.html))
* to_numpy - 按照示例将 df 转为 numpy 格式。**请注意当列的数据类型不同时，to_numpy 的效率将变得很低**。(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_numpy.html))

## DAY FOUR
### 20200318 周三

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
  
#### Viewing data
* describe - 按照示例查看 df 的描述性统计（关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.describe.html)）
* T - 按照示例查看 df 的转置(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.T.html))
* sort_index - 仿照示例将 df 按照 index （日期）从近到远排列。(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sort_index.html))
* sort_values - 仿照示例将 df 按照 A,B 两列从大到小排列。(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sort_values.html))

## DAY FIVE
### 20200319 周四

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
  
#### Selection
* [] - 仿照示例获取 df 的 B 列（提示：英文单引号和英文双引号效果相同，选择一种使用即可）
* . - 仿照示例获取 df 的 C 列
* [index_rank : index_rank] - 仿照示例查看 df 的 0 至 4 行（不含），也就是数学区间的[0,4)行
* [index_value : index_value] - 仿照示例查看 df 的 20130103 至 20130106（含），也就是数学区间的[20130103,20130106]行

## DAY SIX
### 20200320 周五

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
  
#### Selection
##### Selection by label
* loc - 仿照示例获取 df 的 3 行，即 dates[3] 。(提示：index 的 label 为 date）(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html))
* loc - 仿照示例获取 df 的 A,C 列。(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html))
* loc - 仿照示例获取 df 20130103 至 20130106 行的 A,C 列。(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html))

**用法总结**

一般来说使用 loc 时，需要在方括号里填入行或列的 **label**，通俗地讲，就是行、列的名字。具体在本例中，就是 dates[3],20130103 (行的名字） 以及 A,C （列的名字）。

如果我们把 index label 简写为 $indexl$，下标 $i,j = 0,1,……,N-1$，$N$ 为行数，且 $i < j$

column label 简写为 $columnl$，下标 $k,l = 0,1,……,M-1$，$M$ 为列数，且 $k < l$


那么对于连续的切片：
> $df.loc[indexl_i:indexl_j,columnl_k:columnl_l]$

对于离散的切片：
> $df.loc[[indexl_i,indexl_j],[columnl_k,columnl_l]]$

对于行连续、列离散的切片(行离散、列连续同理）：
> $df.loc[indexl_i:indexl_j,[columnl_k,columnl_l]]$

## DAY SEVEN
### 20200321 周六

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
  
#### Selection
##### Selection by label
* loc - 使用 loc 获取 df 20130103 和 20130106 两日的A,C 列 。(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html))
* at - 仿照示例获取 df 的 3 行 C 列。

##### Selection by position
* iloc - 仿照示例使用 iloc 获取 df 的 3 行(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))


## DAY EIGHT 
### 20200322 周日

[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)

#### RECAP
* 载入 numpy 和 pandas 并以约定俗成的简称命名之
* 创建一个10行8列的随机数矩阵命名为 df，其中列名为 ABCDEFGH
* 打印 df 的前 5 行
* 查看 df 的描述性统计
* 将 df 按照 A 列数值从小到大排序
* 打印 df 的 C,H 列
* 打印 df 的 C 至 H 列
* 打印 df 的 6,9 行
* 打印 df 的 6 至 9 行（不含）
* 打印 df 的 6 至 9 行（不含）的 C 至 H 列
* 打印 df 的 6,9 行的 C,H 列
  
## DAY NINE 
### 20200323 周一
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Selection
##### Selection by position
* iloc - 仿照示例使用 iloc 获取 df 的 1 行至 4 行（不含）的 0 列至 3 列（不含）(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))
* iloc - 仿照示例使用 iloc 获取 df 的 1 行、 4 行的 0 列、 3 列(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))
* iloc - 仿照示例使用 iloc 获取 df 的 1 至 4 行（不含）(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))






