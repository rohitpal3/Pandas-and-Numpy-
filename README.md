# Pandas-and-Numpy-
Important Function 
1.pd.read_cv
2.df.head()
3.df.shape() or df.info() or df.column
4.df=df.drop(['url','address','phone',],axis=1)
5.df.drop_duplicates(inplace = True) (to drop duplicate value)
6.df.rate.isnull().sum() and df.rate.unique()

#replacing new and - value with null value
def replacerate(value):
    if(value =='NEW' or value =='-'):
        return np.nan
    else:
        value= str(value).split('/')
        value=value[0]
        return float(value)
df['rate']=df['rate'].apply(replacerate)


7.df.rate.fillna(df.rate.mean(), inplace= True) fill null values with mean
8. df.dropna(inplace= True) drop null values
9.  df.rename(columns={'approx_cost(for two people)':'cost2people','listed_in(type)':'type','listed_in(city)':'City'},inplace= True)


def handlecomma(value):
    value1 = str(value)
    if value1 == ',':
        value = value1.replace(',', '')
        return value
    else:
        return value 
    
df['Cost2people'] = df['Cost2people'].apply(handlecomma)


