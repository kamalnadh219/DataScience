# Experiment 1

#### Apply least squares model for the regression of number of units sold on TV advertising budget for the Advertising data, for least squares coefficient estimates for simple linear regression.

**Solution:**

```python
import pandas as pd
import numpy as np
from sklearn.linear_model import LinearRegression
```
```python
data = pd.read_csv('/content/Advertising.csv')
model = LinearRegression().fit(data[['TV']], data['Sales'])
tv_coefficient = model.coef_[0]
print("Least squares coefficient estimate for TV advertising budget:", tv_coefficient)
```
**Output:**
Least squares coefficient estimate for TV advertising budget: 0.04753664043301975



<a href="https://www.youtube.com/watch?v=8jazNUpO3lQ">YouTube Video: Histograms Tutorial</a>
