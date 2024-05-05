# Ex.No:04   FIT ARMA MODEL FOR TIME SERIES
# Date : 23-03-2024

### AIM:
To implement ARMA model in python.
### ALGORITHM:
1. Import necessary libraries.
2. Set up matplotlib settings for figure size.
3. Define an ARMA(1,1) process with coefficients ar1 and ma1, and generate a sample of 1000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

4. Display the autocorrelation and partial autocorrelation plots for the ARMA(1,1) process using
plot_acf and plot_pacf.
5. Define an ARMA(2,2) process with coefficients ar2 and ma2, and generate a sample of 10000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

6. Display the autocorrelation and partial autocorrelation plots for the ARMA(2,2) process using
plot_acf and plot_pacf.
### PROGRAM:
```
NAME : Vikash s
REG NO : 212222240115
```
```
from pandas import read_csv
from pandas import datetime
from matplotlib import pyplot
from pandas.plotting import autocorrelation_plot
from pandas import DataFrame
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.arima_process import ArmaProcess
import matplotlib.pyplot as plt
import numpy as np
import warnings
warnings.filterwarnings('ignore')
import matplotlib.pyplot as plt
import numpy as np

plt.rcParams['figure.figsize'] = [10, 7.5]

ar1 = np.array([1,0.33])
ma1 = np.array([1,0.9])
ARMA_1 = ArmaProcess(ar1,ma1).generate_sample(nsample = 1000)
plt.plot(ARMA_1)
plt.title('Simulated ARMA(1,1) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_1)
plot_pacf(ARMA_1)
ar2 = np.array([1, 0.33, 0.5])
ma2 = np.array([1, 0.9, 0.3])
ARMA_2 = ArmaProcess(ar2, ma2).generate_sample(nsample=10000)
plt.plot(ARMA_2)
plt.title('Simulated ARMA(2,2) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_2)
plot_pacf(ARMA_2)
```

## OUTPUT:
### SIMULATED ARMA(1,1) PROCESS
![316231030-cc32b363-f713-411d-8f3e-54572e825779](https://github.com/vikashsenthil21/TSA_EXP4/assets/119433834/a4ef6d11-85f6-4725-a215-66ee3454711d)



### Partial Autocorrelation
![316231041-2c6c1282-0cd1-4137-a0f9-1900c4debcbb](https://github.com/vikashsenthil21/TSA_EXP4/assets/119433834/eafcb05e-63f0-4c0f-8408-122a9a4623a0)


### Autocorrelation 
![316231050-fcfcef4d-5cd1-46f6-8e77-45d46393a20b](https://github.com/vikashsenthil21/TSA_EXP4/assets/119433834/27d9bd5e-2876-4673-8a77-233837f6debf)



### SIMULATED ARMA(2,2) PROCESS 
![316231084-dfecd07b-ed1f-4be2-861f-564abf2347e6](https://github.com/vikashsenthil21/TSA_EXP4/assets/119433834/e8e2c168-5368-4f0a-a2a0-bdcd4f594733)


### Partial Autocorrelation 
![316231087-238e0f94-83a0-49f8-917c-f9e472480ba5](https://github.com/vikashsenthil21/TSA_EXP4/assets/119433834/eef6e272-0db7-4e54-abe9-8ec9d4019e7c)


### Autocorrelation 
![316231092-54e0825d-6b45-4b0b-a4c5-34a3cc5ddf1a](https://github.com/vikashsenthil21/TSA_EXP4/assets/119433834/4e72b1fe-678f-472b-bc47-94057b4ade4d)


## RESULT:
Thus, a python program is created to fir ARMA Model successfully.
