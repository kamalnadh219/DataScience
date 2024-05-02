# Experiment 4

#### Compute the confusion matrix and overall fraction of correct predictions.Explain what the confusion matrix is telling you about the types of mistakes made by KNN.

**Solution:**

```python
import pandas as pd
from sklearn.neighbors import KNeighborsClassifier as K
from sklearn.metrics import *
d=pd.read_csv('/content/smart_data.csv')


d.dropna(inplace=True)
x=d[['open','high','low','close','volume']]
y=d['Name']
m=K(n_neighbors=3).fit(x,y)
print("Confusion Matrix:",confusion_matrix(y,m.predict(x)))
print("Overall Fraction of Correct Predictions:",accuracy_score(y,m.predict(x)))

```
**Out Put:**
```
Confusion Matrix: [[1251    0    0 ...    0    0    0]
 [   4 1240    0 ...    0    0    0]
 [   0    0 1228 ...    0    0    0]
 ...
 [   2    0   16 ...   53    0    0]
 [   7    0    0 ...    0   30    0]
 [  15    7    0 ...    0    0   22]]
Overall Fraction of Correct Predictions: 0.35664241901429494
```
<a href="https://www.youtube.com/watch?v=r75BPh1uk38">YouTube Video: Histograms Tutorial</a>
