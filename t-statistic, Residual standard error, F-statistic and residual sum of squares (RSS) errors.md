# Experiment 2

#### Compute t-statistic, Residual standard error, F-statistic and residual sum ofsquares (RSS) errors.
**Solution:**

```python
import pandas as pd
import numpy as np
from sklearn.linear_model import LinearRegression
data = pd.read_csv('/content/Advertising.csv')
import statsmodels.api as sm
```
```python
import statsmodels.api as sm
x = data[['TV']].copy()
y =data['Sales']
x['const'] =1
model = sm.OLS(y, x).fit()
t_statistic = model.tvalues[1]
residual_standard_error = model.mse_resid ** 0.5
f_statistic = model.fvalue
rss = model.ssr
print("T-Statistic:", t_statistic)
print("Residual Standard Error:", residual_standard_error)
print("F-Statistic:", f_statistic)
print("Residual Sum of Squares (RSS):", rss)
```
**Output:**


T-Statistic: 15.360275174117547<br>
Residual Standard Error: 3.258656368650463<br>
F-Statistic: 312.1449943727128<br>
Residual Sum of Squares (RSS): 2102.5305831313517<br>




<a href="https://www.youtube.com/watch?v=8jazNUpO3lQ">Data Set Tutorial</a>
