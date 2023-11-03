## Learning Plan
* Jupyter allows you to run python code interactively in a web browser. 
* You can also share your code (called notebooks).
* Install using conda is recommended by Juypter Documentation. Technically venv can work too. 
* See README for installation instructions. 
* ESC takes you to command mode 
* ENTER takes you to edit mode 
* Everything is separated into cells 
* You can add cells above or below
* "!" can be used to run bash commands, like !ls (!dir on windows)
* "%" for magic keywords, use %lsmagic to get the list, example %pwd 
* Use `%matplotlib inline` to show matplot lib data inside jupyter. 
* Notebook files are just json files, that you share. 
* Use file --> export as HTML for posting into a blog etc. 
* Using matplotlib (remember to pip install `matplotlib`, `numpy` and `pandas` first) then try [this](https://matplotlib.org/stable/plot_types/basic/scatter_plot.html#sphx-glr-plot-types-basic-scatter-plot-py).
* Load a sample csv `df = pd.read_csv("./zillow.csv")` then run `df` to see the data, You can also see `df.head(5)` or `df.tail(5)` to see head or tail.
* You can sort the dataframe `top_5 = df.sort_values(by="SF", ascending=False).head()`

## Examples

Getting top rows

```
import pandas as pd
df = pd.read_csv("./zillow.csv")
df.columns
df.sort_values(by="LivingSpace", ascending=False).head()
```
Plotting a scatter plot

```
df.plot(x="Beds", y="ListPrice", kind="scatter")
```

Filtering, averaging, summarizing stuff
```
big_houses = df[(df["Beds"] > 4)]
big_houses['ListPrice'].mean()
big_houses[['LivingSpace', 'ListPrice']].describe()
big_houses[['Beds']].groupby('Beds').value_counts()
```

Iterating over rows (generally not recommended)
```
for i, row in df.iterrows():
    print(i, row['Zip'])
```
