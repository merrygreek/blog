---
title: "Pandas"
date: 2021-03-10T21:19:59+08:00
tags:
- python
- 数据处理

---

![](/img/pandas.jpg)

```python
pd.read_csv(,sep='/t',index_col='',header=None,parse_date=[5,6])
df.shape/.shape[0]
df.columns
df.types/s.type
df.info()
df.head()
df.tail()
#索引标签
df.loc[]
df.loc[[0,8,9]]
df.loc[:,['year','pop']]
#索引顺序
df.iloc[[]]
df.iloc[:,3:6]
#分组
df.groupby('year')['lifeExp'].mean()
df.groupby(['year','age'])[['life','god']].mean()
#重新index
df.reset.index()
#值不同的个数
s.nunique()
#不同的值
s.nunique()
#统计,不管相不相同
df1[df1[8]=='停送电操作计划'][2].value_counts()
#建立s
pd.Series([list])
#建立df
pd.DataFrame({key:[list]})
#s的运算
S.mean() / .min() / .max()  / .std()
#df统计简介
df.describe()
#筛选
age[age>age.mean()]
#广播,相同索引标签自动对齐
age+age / age+100
#datetime操作
pd.to_datetime(S, format ='%Y-%m-%d')
s = s.astype('timedelta64[Y]')
#df变化的话一般会复制出副本,在源对象进行修改的话
inplace = true
#删除
df.drop(['age'],axis=1)
#to_excel
.to_excel('',sheet_name = '', index = False)

#连接行
row_concat = pd.concat([df1,df2,df3])
pd.concat([df1,df2,df3],ignore_index=True)
#添加列
pd.concat([df1,df2,df3],axis=1)
pd.concat([df1,df2,df3],join='inner')
#单个
df1.append(df2)
#多个df合并
df.merge(df,left_on='name',right_on='site')
df.merge(df,left_on=[''],right_on=[''])
left_join = pd.merge(df1,df2,on='台区考核户',how='left')

#缺失值
pd.isnull()
pd.notnull()
#加载的时候,不包含默认的缺失值
pd.read_csv('',keep_default_na=False)
S.count()
S.fillna(0)
S.dropna()
df.s.sum(skipna =True)

#数据整理
pd.melt(df,id_vars = 'religion')
pd.melt(df,id_vars = [ ],var_name= '',value_name='')
#拆分
df.s.str.split('_')
#组合
df.s.str.split('_',expand = true)
df.columns = ['','']
pd.concat(['',''],axis =1)
s,s= zip(*df.s.str.split('_'))
s.drop_duplicates()
#表查找
import glob
my = glob.glob('*.csv')

#数据分类,category数据表示分类变量:如性别,占用空间更小
s.astype('category')
pd.to_numeric(s,errors='ignore')
pd.to_numeric(s,errors = 'coerce')

#字符
''.join(list)
str.splitlines()
#正则表达式语法
m = re.match(pattern = '',string='')
m.group()
m = re.findall(pattern = '',string= '') - > list
#替代
re.sub(pattern = '',string = ,repl='')
#编译
p = re.compile()
m = p.match(string)
m = p.findall(string)

#函数应用
def my_exp(x,e):
    return x ** e
df['a'].apply(my_exp,e=2)

#按列应用
df.apply(func,axis=0)

import regex as re
p = re.compile()
df['a'].apply(lambda x: p.match(x).group())

df.groupby('').lifeExp.agg(np.mean)

#自定义函数:
def myfunc:
    pass
df.groupby('').lifeExp.agg(myfunc)
df.groupby('').lifeExp.agg([np.mean,np.std,np.count_nonzero])
#指定列的值
df.groupby('').lifeExp.agg({
    'a':'mean',
    'b':'median',
    'c':'median'
    })
df.rename(columns={'':'','':''})

#agg聚合计算,transform方法不会减少数据量
df.groupby('').lifeExp.transform(myfunc)
df.groupby('').lifeExp.filter(lambda x:func)

#时间
from datetime import datetime
t1 = datetime.now()
t2 = datetime(1970,1,1)
diff = t1-t2
d = pd.to_datetime(s,format='%m/%d/%Y')
d.year
d.month
d.day

#s为datetime类型
s.dt.year
te.loc[(te.Date.dt.year==2010)&(te.Date.dt.month==6)]

date为index
te['2015']
te['2010-10']
#工作日
pd.date_range(start='2010-1-1',end='2010-11-2',freq = 'B')
```

