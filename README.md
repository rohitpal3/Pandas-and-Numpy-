# Pandas-and-Numpy-
Important Function 
1.pd.read_cv</br>
2.df.head()</br>
3.df.shape() or df.info() or df.column</br>
4.df=df.drop(['url','address','phone',],axis=1)</br>
5.df.drop_duplicates(inplace = True) (to drop duplicate value)</br>
6.df.rate.isnull().sum() and df.rate.unique()</br>

#replacing new and - value with null value</br>
def replacerate(value):</br>
    if(value =='NEW' or value =='-'):</br>
        return np.nan</br>
    else:</br>
        value= str(value).split('/')</br>
        value=value[0]</br>
        return float(value)</br>
df['rate']=df['rate'].apply(replacerate)</br>


7.df.rate.fillna(df.rate.mean(), inplace= True) fill null values with mean</br>
8. df.dropna(inplace= True) drop null values</br>
9.  df.rename(columns={'approx_cost(for two people)':'cost2people','listed_in(type)':'type','listed_in(city)':'City'},inplace= True)</br>


def handlecomma(value):</br>
    value1 = str(value)</br>
    if value1 == ',':</br>
        value = value1.replace(',', '')</br>
        return value</br>
    else:</br>
        return value </br>
    
df['Cost2people'] = df['Cost2people'].apply(handlecomma)</br>


