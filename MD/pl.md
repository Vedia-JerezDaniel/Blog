# Performing Principal Components Regression (PCR) and Partial Least Squares Regression (PLS) in Python



```python

%matplotlib inline
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

from sklearn.preprocessing import scale
from sklearn import model_selection
from sklearn.decomposition import PCA
from sklearn.linear_model import LinearRegression
from sklearn.cross_decomposition import PLSRegression, PLSSVD
from sklearn.metrics import mean_squared_error


df = pd.read_csv("D://Gitrepo//Blog//rus2.csv", sep=",")
```


```python
def clean_dataset(df):
    assert isinstance(df, pd.DataFrame), "df needs to be a pd.DataFrame"
    df.dropna(inplace=True)
    indices_to_keep = ~df.isin([np.nan, np.inf, -np.inf]).any(1)
    return df[indices_to_keep]
```


```python
dt = df.select_dtypes(include=np.number)
clean_dataset(dt)
dt.head(6)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
    
    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>total_time</th>
      <th>wait_time</th>
      <th>surge_multiplier</th>
      <th>driver_gender</th>
      <th>price_usd</th>
      <th>distance_kms</th>
      <th>temperature_value</th>
      <th>humidity</th>
      <th>wind_speed</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>29</td>
      <td>7</td>
      <td>1.0</td>
      <td>1</td>
      <td>5.17</td>
      <td>9.29</td>
      <td>12</td>
      <td>0.69</td>
      <td>4.81</td>
    </tr>
    <tr>
      <th>1</th>
      <td>26</td>
      <td>6</td>
      <td>1.0</td>
      <td>1</td>
      <td>4.97</td>
      <td>9.93</td>
      <td>10</td>
      <td>0.70</td>
      <td>6.53</td>
    </tr>
    <tr>
      <th>2</th>
      <td>83</td>
      <td>16</td>
      <td>1.0</td>
      <td>1</td>
      <td>13.01</td>
      <td>18.01</td>
      <td>14</td>
      <td>0.61</td>
      <td>5.25</td>
    </tr>
    <tr>
      <th>3</th>
      <td>20</td>
      <td>6</td>
      <td>2.9</td>
      <td>1</td>
      <td>25.99</td>
      <td>5.10</td>
      <td>3</td>
      <td>0.84</td>
      <td>0.87</td>
    </tr>
    <tr>
      <th>4</th>
      <td>49</td>
      <td>10</td>
      <td>1.4</td>
      <td>1</td>
      <td>13.43</td>
      <td>21.92</td>
      <td>3</td>
      <td>0.90</td>
      <td>1.61</td>
    </tr>
    <tr>
      <th>5</th>
      <td>34</td>
      <td>17</td>
      <td>1.0</td>
      <td>1</td>
      <td>4.06</td>
      <td>4.88</td>
      <td>7</td>
      <td>0.83</td>
      <td>2.73</td>
    </tr>
  </tbody>
</table>
</div>




```python
df[df["ride_hailing_app"] == "Uber"].shape
df[df["ride_hailing_app"] == "Gett"].shape

print(
    "Uber size: ",
    df[df["ride_hailing_app"] == "Uber"].shape,
    "\n Gett size: ",
    df[df["ride_hailing_app"] == "Gett"].shape,
)
```

    Uber size:  (642, 19) 
     Gett size:  (36, 19)



```python
y = dt["price_usd"].values
x = dt.drop(["price_usd"], axis=1)


```


```python
pca = PCA()
X_reduced = pca.fit_transform(scale(x))
pd.DataFrame(pca.components_.T).loc[:5, :5]

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
    
    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.692667</td>
      <td>-0.112583</td>
      <td>-0.039522</td>
      <td>-0.025766</td>
      <td>0.019017</td>
      <td>-0.047957</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.500662</td>
      <td>-0.041094</td>
      <td>-0.479095</td>
      <td>0.124474</td>
      <td>0.329412</td>
      <td>0.376474</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.008190</td>
      <td>-0.082623</td>
      <td>0.372405</td>
      <td>0.675290</td>
      <td>0.564377</td>
      <td>-0.279762</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.006483</td>
      <td>-0.118291</td>
      <td>0.496058</td>
      <td>-0.566484</td>
      <td>0.523330</td>
      <td>0.371541</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.492186</td>
      <td>-0.090315</td>
      <td>0.469016</td>
      <td>-0.155549</td>
      <td>-0.343554</td>
      <td>-0.375643</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.148509</td>
      <td>0.652022</td>
      <td>0.159145</td>
      <td>0.131533</td>
      <td>-0.059497</td>
      <td>0.124116</td>
    </tr>
  </tbody>
</table>
</div>




```python
# 10-fold CV, with shuffle
n = len(X_reduced)
kf_10 = model_selection.KFold(n_splits=10, shuffle=True, random_state=1)
regr = LinearRegression()
mse = []

# Calculate MSE with only the intercept (no principal components in regression)
score = (
    -1
    * model_selection.cross_val_score(
        regr, np.ones((n, 1)), y.ravel(), cv=kf_10, scoring="neg_mean_squared_error"
    ).mean()
)
mse.append(score)

# Calculate MSE using CV for the 19 principle components, adding one component at the time.
for i in np.arange(1, 20):
    score = (
        -1
        * model_selection.cross_val_score(
            regr,
            X_reduced[:, :i],
            y.ravel(),
            cv=kf_10,
            scoring="neg_mean_squared_error",
        ).mean()
    )
    mse.append(score)

# Plot results
fig = plt.figure()
ax = fig.add_subplot(111)
plt.plot(mse, "-v")
plt.xlabel("Number of principal components in regression")
plt.ylabel("MSE")
plt.title("Price")

ymin = min(mse)
xpos = mse.index(ymin)
xmin = np.arange(1, 20)[xpos]  # min 8

ax.annotate(
    "Min. MSE",
    xy=(xmin, ymin),
    xytext=(xmin, ymin + 2),
    arrowprops=dict(facecolor="red", shrink=0.02),
)

plt.xlim(xmin=-1)

```




    (-1.0, 19.95)




Here's the plot for the best regression model : ![alt]({{ site.url }}{{ site.baseurl }}/images/py/pcr.png)    



```python
np.cumsum(np.round(pca.explained_variance_ratio_, decimals=3) * 100)

# When M= 5 we get an 80.3%

```




    [23.3, 42.4, 55.4, 67.9, 80.3, 91.6, 98. , 99.9]




```python

## Now let's perform PCA on the training data and evaluate its test set performance:

pca2 = PCA()
# Split into training and test sets
x_train, x_test, y_train, y_test = model_selection.train_test_split(
    x, y, test_size=0.3, random_state=1
)
# Scale the data
x_reduc_train = pca2.fit_transform(scale(x_train))
n = len(x_reduc_train)

# 10-fold CV, with shuffle
kf_10 = model_selection.KFold(n_splits=10, shuffle=True, random_state=1)
mse2 = []

# Calculate MSE with only the intercept (no principal components in regression)
score2 = (
    -1
    * model_selection.cross_val_score(
        regr,
        np.ones((n, 1)),
        y_train.ravel(),
        cv=kf_10,
        scoring="neg_mean_squared_error",
    ).mean()
)
mse.append(score2)

# Calculate MSE using CV for the 19 principle components, adding one component at the time.
for i in np.arange(1, 20):
    score2 = (
        -1
        * model_selection.cross_val_score(
            regr,
            x_reduc_train[:, :i],
            y_train.ravel(),
            cv=kf_10,
            scoring="neg_mean_squared_error",
        ).mean()
    )
    mse2.append(score2)
```


```python
# Plot results
fig = plt.figure()
ax = fig.add_subplot(111)
plt.plot(mse2, "-v")
plt.xlabel("Number of principal components in regression")
plt.ylabel("Reduced MSE")
plt.title("Price")

ymin = min(mse2)
xpos = mse2.index(ymin)
xmin = np.arange(1, 20)[xpos]  # min 6

ax.annotate(
    "Min. MSE",
    xy=(xmin, ymin),
    xytext=(xmin, ymin + 1),
    arrowprops=dict(facecolor="red", shrink=0.02),
)

plt.xlim(xmin=-1)
```




    (-1.0, 18.9)




Here's the plot for the best regression model : ![alt]({{ site.url }}{{ site.baseurl }}/images/py/pcr2.png)    
    



```python
np.cumsum(np.round(pca2.explained_variance_ratio_, decimals=3) * 100)
```




    [ 23.4,  42.5,  55.8,  68.3,  80.7,  92. ,  98.3, 100. ]




```python
## We find that the lowest cross-validation error occurs when  M=6  components are used.

x_redu_test = pca2.transform(scale(x_test))[:, :5]

# Train regression model on training data
regr = LinearRegression()
regr.fit(x_reduc_train[:, :5], y_train)

# Prediction with test data
pred = regr.predict(x_redu_test)
mean_squared_error(y_test, pred)

```




    8.909402005123031




```python
from sklearn.pipeline import make_pipeline
from sklearn.preprocessing import StandardScaler

pcr = make_pipeline(StandardScaler(), PCA(n_components=6), LinearRegression())
pcr.fit(x_train, y_train)
pca = pcr.named_steps['pca']
```


```python
# 6.7.2 Partial Least Squares

n = len(x_train)

# 10-fold CV, with shuffle
kf_10 = model_selection.KFold(n_splits=10, shuffle=True, random_state=1)
pls_mse = []

for i in np.arange(1, 9):
    pls = PLSRegression(n_components=i)
    score = model_selection.cross_val_score(
        pls, scale(x_train), y_train, cv=kf_10, scoring="neg_mean_squared_error"
    ).mean()
    pls_mse.append(-score)
    
```


```python
fig = plt.figure()
ax = fig.add_subplot(111)
plt.plot(np.arange(1, 9), np.array(pls_mse), "-v", color="green")
plt.xlabel("Number of principal components in regression")
plt.ylabel("MSE")
plt.title("Price")

ymin = min(pls_mse)
xpos = pls_mse.index(ymin)
xmin = np.arange(1, 9)[xpos]  # min 6

ax.annotate(
    "Min. MSE",
    xy=(xmin, ymin),
    xytext=(xmin, ymin + 0.08),
    arrowprops=dict(facecolor="yellow", shrink=0.02),
)

plt.show()
```


Here's the plot for the best regression model : ![alt]({{ site.url }}{{ site.baseurl }}/images/py/pls.png)    
    

```python
pls = PLSRegression(n_components=2)
pls.fit(scale(x_train), y_train)

mean_squared_error(y_test, pls.predict(scale(x_test)))
```




    9.19707333152056




```python
fig, axes = plt.subplots(1, 2, figsize=(8, 5))
axes[0].scatter(pca.transform(x_test)[:,0], y_test, alpha=.3, label='ground truth')
axes[0].scatter(pca.transform(x_test)[:,0], pcr.predict(x_test), alpha=.3,
                label='predictions')
axes[0].set(xlabel='Projected data onto first PCA component',
            ylabel='y', title='PCR / PCA')
axes[0].legend(loc='upper left')

axes[1].scatter(pls.transform(x_test)[:,0], y_test, alpha=.3, label='ground truth')
axes[1].scatter(pls.transform(x_test)[:,0], pls.predict(x_test), alpha=.3,
                label='predictions')
axes[1].set(xlabel='Projected data onto first PLS component',
            ylabel='y', title='PLS')
axes[1].legend()
plt.tight_layout()
plt.show()

```


Here's the plot for the best regression model : ![alt]({{ site.url }}{{ site.baseurl }}/images/py/pre.png)    
    

