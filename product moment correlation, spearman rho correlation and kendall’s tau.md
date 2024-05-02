# Experiment 8

#### Carry out the pearson product moment correlation, spearman rho correlation and kendall’s tau

**Solution:**

```python
import pandas as pd
import matplotlib.pyplot as plt
import pandas as pd
from scipy.stats import pearsonr, spearmanr, kendalltau
college_data = pd.read_csv('/content/College.csv')


pearson_corr_coefficient, _ = pearsonr(college_data['Outstate'], college_data['Room.Board'])
print("Pearson correlation coefficient between 'Outstate' and 'Room.Board':", pearson_corr_coefficient)
 
# Calculate Spearman's rank correlation coefficient
spearman_corr_coefficient, _ = spearmanr(college_data['Outstate'], college_data['Room.Board'])
print("Spearman's rank correlation coefficient between 'Outstate' and 'Room.Board':", spearman_corr_coefficient)
 
# Calculate Kendall's tau
kendall_tau, _ = kendalltau(college_data['Outstate'], college_data['Room.Board'])
print("Kendall's tau between 'Outstate' and 'Room.Board':", kendall_tau)

```

<a href="https://github.com/kamalnadh219/DataScience/blob/main/College.csv">Data Set</a>
