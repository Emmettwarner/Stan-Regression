# Stan Linear Regression


### 1. Installation
a. In your console you will need to install Stan on your device using ```pip install cmdstanpy```

b. Once installed go into Jupyter Lab, start a new notebook and import cmdstanpy which lets you install cmdstan 
```
import cmdstanpy 
cmdstanpy.install_cmdstan()
``` 

### 2. Creating a .stan file
  a. Clone my repisitory to get the .stan file make sure its in the same virtual enviroment as your Jupyter notebook for ease of access.
  
  b. Stan has a lot of different data analysis models which you can explore here [Stan Models](https://mc-stan.org/docs/stan-users-guide/regression.html)

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
  a. The libraries I am using can also be found on my GitHub use ``` pip install -r requirements.txt ```
  
  b. The python library os lets you open the .stan file in python.
  ```
stan_reg = os.path.join('linear_reg.stan')
```
