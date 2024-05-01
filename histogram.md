# Experiment 6

#### Produce some histograms with differing numbers of bins for a few of the quantitative variables.

**Solution:**

```python
import matplotlib.pyplot as plt
%matplotlib inline

blood_sugar = [113, 85, 90, 150, 149, 88, 93, 115, 135, 80, 77, 82, 129]
fig, axs = plt.subplots(2, 2, figsize=(12, 12))
axs[0, 0].hist(blood_sugar, bins=4)
axs[0, 1].hist(blood_sugar, bins=6)
axs[1, 1].hist(blood_sugar, bins=2)
axs[1, 0].hist(blood_sugar, bins=8)
plt.show()
```
![53b42c63-becd-4d7a-ac07-724399df77a4](https://github.com/kamalnadh219/DataScience/assets/98703042/771f80c2-1be7-4faa-a28a-c698fac00e48)

<a href="https://www.youtube.com/watch?v=r75BPh1uk38">YouTube Video: Histograms Tutorial</a>

