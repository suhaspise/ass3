
In [ ]:
import pandas as pd
In [ ]:
import matplotlib.pyplot as plt
In [ ]:
from google.colab import files
In [ ]:
uploaded=files.upload()
Saving Table_3.6.csv to Table_3.6.csv
In [ ]:
df=pd.read_csv("Table_3.6.csv")
In [ ]:
print(df)
               States  ...  Never (in percent)
0      Andhra Pradesh  ...               75.07
1   Arunachal Pradesh  ...                6.33
2               Bihar  ...               56.25
3             Haryana  ...               14.07
4    Himachal Pradesh  ...               13.43
5     Jammu & Kashmir  ...               38.00
6           Jharkhand  ...               71.29
7           Karnataka  ...               28.27
8              Kerala  ...               30.86
9      Madhya Pradesh  ...               66.00
10        Maharashtra  ...               44.84
11          Meghalaya  ...                0.00
12             Punjab  ...               21.00
13          Rajasthan  ...               18.97
14         Tamil Nadu  ...               31.10
15      Uttar Pradesh  ...               42.82
16        West Bengal  ...               39.39
17     Sample Average  ...               39.98

[18 rows x 5 columns]
In [ ]:
x=df["States"]
In [ ]:
print(x)
0        Andhra Pradesh
1     Arunachal Pradesh
2                 Bihar
3               Haryana
4      Himachal Pradesh
5       Jammu & Kashmir
6             Jharkhand
7             Karnataka
8                Kerala
9        Madhya Pradesh
10          Maharashtra
11            Meghalaya
12               Punjab
13            Rajasthan
14           Tamil Nadu
15        Uttar Pradesh
16          West Bengal
17       Sample Average
Name: States, dtype: object
In [ ]:
y=df["Never (in percent)"]
In [ ]:
print(y)
0     75.07
1      6.33
2     56.25
3     14.07
4     13.43
5     38.00
6     71.29
7     28.27
8     30.86
9     66.00
10    44.84
11     0.00
12    21.00
13    18.97
14    31.10
15    42.82
16    39.39
17    39.98
Name: Never (in percent), dtype: float64
In [ ]:
plt.plot(df["Never (in percent)"])
Out[ ]:
[<matplotlib.lines.Line2D at 0x7fad14f7b908>]

In [ ]:
plt.plot(df["States"])
Out[ ]:
[<matplotlib.lines.Line2D at 0x7fad14a69358>]

In [ ]:
df.plot.bar()
plt.title("bar plot")
Out[ ]:
Text(0.5, 1.0, 'bar plot')

In [ ]:
df.plot.hist()
plt.title("hist plot")
Out[ ]:
Text(0.5, 1.0, 'hist plot')

In [ ]:
df.boxplot()
plt.title("box plot")
Out[ ]:
Text(0.5, 1.0, 'box plot')
