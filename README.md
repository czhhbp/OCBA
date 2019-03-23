# OCBA
An python implementation for Optimal computing budget allocation (OCBA) from [paper](https://deepblue.lib.umich.edu/bitstream/handle/2027.42/45045/10626_2004_Article_264696.pdf?sequence=1&isAllowed=y) .

It's a function for computing budget allocated to each design with addiction budget given in next round.
The first round is not considered in this function, 
you need to set initional budget for each design and simulate in the calling funcion. 
When you get the static information after simulation, 
you can call this function to calculate budget needed for each design in next round.
All kinds of situation of statistical information of the designs have been considered, 
so you can use it with confidence.

## How to use
    continue_bool, needed_budget = OCBA(design_mean, design_var, design_used, addiction_budget)

For more information,please see the codes.Comment is enough.

## Simple test：
```python
import numpy as np
from OCBA import OCBA
design_mean = np.arange(1,5)
design_var = np.arange(1,5)
design_used = np.ones(4) * 5
addiction_budget = 10
flag, design_budget = OCBA(design_mean, design_var, design_used, addiction_budget)
```
 output:
```python
flag = True
design_budget = [0. 0. 4. 6.] (numpy.ndarray)
```
