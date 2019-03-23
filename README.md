# OCBA
An python implementation for Optimal computing budget allocation (OCBA) from [paper](https://deepblue.lib.umich.edu/bitstream/handle/2027.42/45045/10626_2004_Article_264696.pdf?sequence=1&isAllowed=y) 

It's a function for computing budget allocated to each design with addiction budget given in next round.
The first round is not considered in this function, you need to set initional budget for each design and simulate in the calling funcion. When you get the static information after simulation, you can all this function to calculate budget needed for each design in next round.

continue_bool, needed_budget = OCBA(design_mean, design_var, design_used, addiction_budget)

For more information,please see the codes.Comment is enough.
