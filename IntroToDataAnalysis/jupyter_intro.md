# Intro to Jupyter Notebooks

Here are some of the **awesome** things you can do with [Jupyter](https://jupyter.org/) notebooks!
* Markdown
* Code
* Visualizations
* Math Equations

## Code


```python
import numpy as np
import pandas as pd


# Generate 200 random data points along 3 dimensions
x, y, scale = np.random.randn(3, 200)
```


```python
df = pd.DataFrame({"x": x, "y": y, "scale": np.abs(scale)*400})
df.head()
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
      <th>x</th>
      <th>y</th>
      <th>scale</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-1.103836</td>
      <td>0.504666</td>
      <td>140.479902</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-0.757283</td>
      <td>0.379282</td>
      <td>336.376589</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.362067</td>
      <td>-0.010400</td>
      <td>237.105927</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.277399</td>
      <td>-0.745875</td>
      <td>111.946316</td>
    </tr>
    <tr>
      <th>4</th>
      <td>-0.222829</td>
      <td>-1.057424</td>
      <td>65.148486</td>
    </tr>
  </tbody>
</table>
</div>



## Visualizations


```python
df.plot.scatter(x="x", y="y", s="scale", c="scale", colormap='viridis', figsize=(12, 8));
```


    
![png](jupyter_intro_files/jupyter_intro_6_0.png)
    


## Math Equations

When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are 
$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$
