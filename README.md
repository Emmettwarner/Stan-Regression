# Stan Regression


### 1. Installation
a. In your console you will need to install Stan on your device use ```pip install cmdstanpy```

b. Once installed go into Jupyter Lab and then import cmdstanpy this lets you install cmdstan 
```
import cmdstanpy 
cmdstanpy.install_cmdstan()
``` 

### 2. Compiling
  a. Navigate to [Stan Regression Model](https://mc-stan.org/docs/stan-users-guide/regression.html) and copy the first model on the page or copy from the space below.
  
  b. In jupyter lab create a text file, paste the model in then rename it so it becomes a .stan file. 

  c. Import the python package os this lets you call the .stan file into python.

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

  
