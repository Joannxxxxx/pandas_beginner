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

