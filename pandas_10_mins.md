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

#### PRACTICE
* 载入 numpy 和 pandas 并以约定俗成的简称命名之
* 创建一个10行8列的随机数矩阵命名为 df3，其中列名为 ABCDEFGH
* 打印 df3 的前 5 行
* 查看 df3 的描述性统计
* 将 df3 按照 A 列数值从小到大排序（只展示前 5 行）
* 打印 df3 的 C,H 列（只展示前 5 行）
* 打印 df3 的 C 至 H 列（只展示前 5 行）
* 打印 df3 的 6,9 行
* 打印 df3 的 6 至 9 行（不含）
* 打印 df3 的 6 至 9 行（不含）的 C 至 H 列
* 打印 df3 的 6,9 行的 C,H 列
  
## DAY NINE 
### 20200323 周一
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Selection
##### Selection by position
* iloc - 仿照示例使用 iloc 获取 df 的 1 行至 4 行（不含）的 0 列至 3 列（不含）(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))
* iloc - 仿照示例使用 iloc 获取 df 的 1 行、 4 行的 0 列、 3 列(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))
* iloc - 仿照示例使用 iloc 获取 df 的 1 至 4 行（不含）(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))

## DAY TEN 
### 20200324 周二
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Selection
##### Selection by position
* iloc - 仿照示例使用 iloc 获取 df 的 2 行 2 列(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html))
* iat - 仿照示例使用 iat 获取 df 的 2 行 2 列(关于函数更详尽的解释见(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iat.html))

##### Boolean indexing
* 仿照示例选取 df 中 A 列大于 0.5 的部分
* 仿照示例选取 df 中所有小于 0.5 的部分
* 创建 df : 
```python
dates = pd.date_range('20130101', periods=6)
df = pd.DataFrame(np.random.randn(6, 4), index=dates, columns=list('ABCD'))
```
* copy - 按照示例复制 df 并命名为 df2
* 仿照示例创建 df2 的 E 列，值为 ['T', 'O', 'T', 'T', 'D', 'U']
* isin - 仿照示例选取 df2 中 E 列值为 T,D,U 的部分(关于函数更详尽的解释见(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.isin.html))

## DAY ELEVEN
### 20200325 周三
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Setting
* 仿照示例创建 s1，长度为 7，数值任意，其中 index 为 20200206 起的 7 天
* at - 仿照示例将 df 的 0 行 B 列赋值为 0
* iat - 仿照示例将 df 的 0 行 0 列赋值为 0
* 将 df 的 D 列均赋值为 5
* 仿照示例将 df 中数值为 5 的赋值为其相反数

## DAY TWELVE
### 20200326 周四
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Missing data
* 按照示例创建 df1
* 按照示例给 E 列 0,1 行赋值为 1
* dropna - 按照示例对 df1 去除所有含有空值的行(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.dropna.html))
* fillna - 按照示例将 df1 中所有空值用数值 5 填充(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.fillna.html))
* isna - 按照示例判断 df1 中每个值是否为空值[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.isna.html))

## DAY TRIRTEEN
### 20200327 周五
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Operations
##### Stats
* mean - 按照示例计算 df 每一列的平均值(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.mean.html))
* mean - 按照示例计算 df 每一行的平均值(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.mean.html))
* shift - 按照示例创建 s 并后移 2 行(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.shift.html))
* sub - 按照示例将 df 每一列与 s 相减(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sub.html))

## DAY FOURTEEN
### 20200328 周六
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Operations
##### Apply
* apply & cumsum - 按照示例对 df 每一列执行累加(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.apply.html))
* apply & cumsum - 仿照示例对 df 每一行执行累加（提示：使用 axis 参数决定对行操作或对列操作）(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.apply.html))
* apply & lambda - 按照示例对 df 每一列求极差(关于函数更详尽的解释见[链接](https://blog.csdn.net/SeeTheWorld518/article/details/46959593))
##### Histogramming
* 按照示例创建 s
* value_counts - 统计 s 中各个数值出现的频次(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.value_counts.html))

## DAY FIFTEEN
### 20200329 周日
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Operations
##### String Methods
* 按照示例创建 s
* str.lower - 按照示例将 s 中元素的字母都变为小写(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.lower.html))
* str.upper - 仿照示例将 s 中元素的字母都变为大写(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.upper.html))
* str.capitalize - 仿照示例将 s 中元素的首字母变为大写(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.capitalize.html))

## DAY SIXTEEN
### 20200330 周一
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Merge
##### Concat
* 按照示例创建 df
* 按照示例将 df 切成三份
* concat - 按照示例将切割后的 pieces 拼接起来(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.concat.html))
* 仿照示例将 df 按列切成三份，每一份分别拥有1、2、1列
* concat - 仿照示例将按列切割后的拼接起来(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.concat.html))

## DAY SEVENTEEN
### 20200331 周二
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Merge
##### Join
* 按照示例创建数据框 left 和 right
* merge - 按照示例以 key 为主键合并 left 和 right(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.merge.html))
* 按照示例创建数据框 left 和 right
* merge - 按照示例以 key 为主键合并 left 和 right(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.merge.html))

#### Grouping
* 按照示例创建数据框 df
* groupby & sum - 按照示例将 df 按 A 列分组对有数值的列求和(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html))
* groupby & sum - 按照示例将 df 按 A,B 列分组对有数值的列求和(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html))
* groupby & sum - 仿照示例将 df 按 A 列分组对 C 列求和(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html))
* groupby & mean - 仿照示例将 df 按 B 列分组对 D 列求平均(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html))

## DAY EIGHTEEN
### 20200401 周三
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Reshaping
##### Stack
* 按照示例创建 tuples 和 index 并打印显示
* 按照示例创建 df 并打印显示
* 按照示例创建 df2 并打印显示
* stack - 按照示例对 df2 进行堆叠(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.stack.html))
* unstack - 按照示例对数据框 stack 进行去堆叠(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.unstack.html))
* unstack - 按照示例对数据框 stack 按 level = 1 进行去堆叠(**提示：数据框 stack 共有三层 index，分别为 first,second,A/B, 对应 level 0,1,2**)(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.unstack.html))
* unstack - 按照示例对数据框 stack 按 level = 0 进行去堆叠(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.unstack.html))
* unstack - 仿照示例对数据框 stack 按 level = 2进行去堆叠(**提示：数据框 stack A/B 这个 index 的 level 为 2，同时，由于它在 index 中排在最末，也可表示为 level = -1。unstack 默认 level 参数为 -1**) (关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.unstack.html))

## DAY NINETEEN
### 20200402 周四
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Reshaping
##### Pivot tables
* 按照示例创建 df 并打印显示
* pivot_table - 按照示例创建 df 的数据透视表

#### Time series
* date_range - 按照示例创建以时间序列 rng 为 index 的随机数数据框 ts (关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html))
* resample & sum - 仿照示例对 ts 按 30S 进行重采样并求和(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.resample.html))
* date_range - 按照示例创建以时间序列 rng 为 index 的随机数数据框 ts (关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html))
* tz_localize - 按照示例将 ts 索引上的时间序列设定为 UTC 时间(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.tz_localize.html))
* tz_convert - 按照示例将 ts_utc 索引上的时间从 UTC 时间转为美国东部时间(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.tz_localize.html))

## DAY TWENTY
### 20200403 周五
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Time series
* date_range - 按照示例创建以时间序列 rng 为 index 的随机数数据框 ts (关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html))
* to_period - 按照示例将数据框 ts 的时间戳索引转为时期索引(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_period.html))
* to_period - 仿照示例将数据框 ts 的时间戳索引转为以季度为时期的索引(提示：freq='Q')(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_period.html))
* to_period - 仿照示例将数据框 ts 的时间戳索引转为以年为时期的索引(提示：freq='Y')(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_period.html))
* to_timestamp - 按照示例将数据框 ps 的时期索引转为时间戳索引(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_timestamp.html))
* period_range - 按照示例创建以时间序列 prng 为 index 的随机数数据框 ts (关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.period_range.html))
* 打印 prng
* asfreq - 将 prng 转为以月为频率的时间序列，返回值为每个季度的结束月(**提示：比如 Q1 为 1月至3月，则 Q1 的起始月为1月，最末月为3月。参数 how = 'start' 表示选择起始期返回，how = 'end' 表示选择最末期返回，它们可直接缩写为 's', 'e'**) (关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.asfreq.html))
* asfreq - 仿照示例将 prng 转为以月为频率的时间序列，返回值为每个季度的结束月，并在此基础上增加一个月(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.asfreq.html))
* asfreq - 仿照示例将 prng 转为以月为频率的时间序列，返回值为每个季度的结束月，并在此基础上增加一个月，然后将其转换为以小时为频率的时间序列，返回值为每天的起始小时，并在此基础上增加 10 个小时(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.asfreq.html))

## DAY TWENTY ONE
### 20200404 周六
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Categoricals
*  按照示例创建 df
*  astype - 按照示例将 df 的 raw_grade 列数据类型转为 category(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.astype.html))
*  cat.categories - 按照示例给予每一类别更有意义的命名(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.cat.categories.html))
* cat.set_categories - 按照示例为 df 的 grade 列设置标签集(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.cat.set_categories.html))
* 打印 df 的 grade 列
* sort_values - 按照示例将 df 按照 grade 列排序(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sort_values.html))
* groupby - 按照示例将 df 按照 grade 列分组并计算每组个数(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html))

## DAY TWENTY TWO
### 20200405 周日
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Plotting
* 按照示例载入 matplotlib.pyplot 并简称为 plt
* 按照示例创建时间序列 ts
* cumsum - 按照示例对 ts 计算累加(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.cumsum.html))
* plot - 按照示例绘制 ts(关于函数更详尽的解释见[官方文档](https://matplotlib.org/3.2.1/api/_as_gen/matplotlib.pyplot.plot.html))
* 按照示例创建时间序列 df
* cumsum - 按照示例对 df 计算累加(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.cumsum.html))
* plt.figure - 按照示例创建画布(关于函数更详尽的解释见[官方文档](https://matplotlib.org/3.2.1/api/_as_gen/matplotlib.pyplot.figure.html))
* plot - 按照示例绘制 df(关于函数更详尽的解释见[官方文档](https://matplotlib.org/3.2.1/api/_as_gen/matplotlib.pyplot.plot.html)) 
* plt.legend - 按照示例使图例位于最佳位置(关于函数更详尽的解释见[官方文档](https://matplotlib.org/3.2.1/api/_as_gen/matplotlib.pyplot.legend.html)) 


## DAY TWENTY THREE
### 20200406 周一
[10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
#### Getting data in/out
##### CSV
* to_csv - 按照示例将 df 以 csv 文件的格式保存到本地(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_csv.html)) 
* read_csv - 按照示例读取刚刚保存的文件(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html)) 

##### Excel
* to_excel - 按照示例将 df 以 xlsx 文件的格式保存到本地(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_excel.html)) 
* read_excel - 按照示例读取刚刚保存的文件(关于函数更详尽的解释见[官方文档](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_excel.html)) 

****
end
****

