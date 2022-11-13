# Backtesting

### Project Motivation:

1. To build a backtesting engine using the Barra dataset that performs portfolio optimization, taking into account transaction costs, and to use performance attribution to identify the major drivers of the portfolio's profit-and-loss (PnL).

### The notebook is separated into three parts:
1. The first part covers data collection and inspection, stock universe construction, alpha factor from Barra model selection, factor returns estimation, risk factor exposure calculation, and transaction cost calculation.
    - This project uses the Barra dataset hosted on Udacity instances for the "AI for Trading" course. The dataset is large and was pre-processed and stored in pickle files on Udacity instances.
2. The second part covers defining and building an objective function, taking its derivative to find the gradient, then minimizing portfolio variance and transaction costs while maximizing returns by optimizing (minimizing) the objective function using it's gradient. The optimized objective function is also used to calculate the portfolio's risk and alpha exposures, as well as total transaction costs.
3. The third part covers putting it all together to form an optimal portfolio, return the risk and alpha exposures, and return total transaction costs by running a backtest and walking through each day, calculating the optimal portfolio holdings and trade list, and then using those "current" optimal holdings as the "previous" optimal holdings in the next day's calculations. Finally, a profit-and-loss (PnL) attribution is calculated.

### File Descriptions:


    project_8.ipynb
    | - Jupyter notebook containing all data collection, cleaning, and data frame construction, alpha and risk factor selection and exposure calculation, objective function definition and construction, gradient calculation, objective function optimization (minimization), backtesting, and PnL attribution calculation.
    helper.py
    |- helper file to abstract some data collection and import statements
    project_helper.py
    |- helper file to abstract graphing functions
    project_test.py
    |- unit tests to flag any major errors
    README.md


### Installations:
- This project uses the Barra dataset hosted on Udacity instances for the "AI for Trading" course. The dataset is large and was pre-processed and stored in pickle files on Udacity instances. You can swap out the code for extracting the dataset with your own custom data access/collection logic.
- You will need a python environment with the following:
    - see the `requirements.txt` file for specific packages and versions
    - python verson 3.7 or higher

### Instructions:
1. Run each cell in 'project_8.ipynb' in sequence. Make sure the Jupyter notebook is in the same level of the directory as 'requirements.txt'.