Python program to calculate the days of the year with the most holidays

You must first install workalendar:

pip install workalendar

Then write and edit the following code with your preferences:

--------

import pandas as pd
from workalendar.america import Colombia
calculate1 = Colombia()
hol=calculate1.holidays(2022)

v1=pd.DataFrame(hol,columns=['date','days'])
v1['date']=pd.to_datetime(v1['date'])
v1['date']=v1['date'].dt.day_name()
v1=v1.groupby('date').count().sort_values('days',ascending = False)
print('Result')
print('\n',v1)

--------

Enjoy it!
