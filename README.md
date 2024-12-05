# Stan Linear Regression


### 1. Installation
a. In your console you will need to install Stan on your device using ```pip install cmdstanpy```

b. Once installed go into Jupyter Lab, start a new notebook and import cmdstanpy which lets you install cmdstan 
```
import cmdstanpy 
cmdstanpy.install_cmdstan()
``` 

### 2. Creating a .stan file
  a. Navigate to [Stan Regression Model](https://mc-stan.org/docs/stan-users-guide/regression.html) and copy the first model on the page or copy from the space below.

  b. In the same folder as you made the notebook create a text file in Jupyter Lab and paste the model in, then rename it as a .stan file.

 ### Stan Linear Regression Model

  ```
data {
  int<lower=0> N;
  vector[N] x;
  vector[N] y;
}
parameters {
  real alpha;
  real beta;
  real<lower=0> sigma;
}
model {
  y ~ normal(alpha + beta * x, sigma);
}
````

### 3. Python Libraries
  a. The libraries I am using are here, make sure yours looks like this:
  ```
import cmdstanpy
cmdstanpy.install_cmdstan()
import os
from cmdstanpy import CmdStanModel
import pandas as pd
import plotnine as pn
import numpy as np
```
  b. The python library os lets you open the .stan file in python.
  ```
stan_reg = os.path.join('linear_reg.stan')
```
