# dsge_trading

## DSGE Models in Systematic Trading Strategies

Author: Adam Foster

Supervisor: Marcin Chlebus

This repo contains a novel systematic trading strategy setup that employs DSGE models for generating trading signals. There may exist deviations between model-implied IRF forecasts and realised macro outcomes that contain exploitable information for asset returns. Thus placing such model results relative to observed macroeconomic variables can provide the foundation for determining low frequency systematic trading decisions.

This framework stands as a candidate investment strategy that could stand the test of time with its grounding in economic theory unlike its high frequency alternatives that typically exploit short-term structural inefficiency or microstructure noise. It also serves as a challenge to established strategies, such as buy-and-hold or other long-term macro strategies.

There is relatively low dependence on data, making this approach quick to implement without major barriers to entry.

### Approach

In practice, an RBC model is constructed as a starting point for modelling the US economy. It undergoes the usual interaction between capital, labour and other variables. Responses of macroeconomic variables are dictated by productivity shocks whose underlying series follows an AR(1) process.

The model with its key parameters is calibrated as per the literature with the exception of productivity whose persistence and standard deviation are estimated. After all, changing productivity will be key both to model results and deviation from realised macroeconomic time series.

The estimation is updated per observation in the test period and impulse response functions (IRF) are produced using this data. The next-period forecast from the penultimate period is compared with realised variable values from the ultimate period: any overperformance or underperformance of the economy for the estimated quantity of productivity shock is then interpreted as a signal to go long and short or vice-versa in a related asset, for example a broad stock market index.

This constitutes a novel framework for systematic low frequency trading of macro assets backed by economic theory and data. The approach would be malleable in the sense that various DSGE models can, in principal, be used to model a particular economy, plus the resulting signal can be used as either a momentum or mean-reversion trade.

## Tech

The model has been coded using Python.

### Running the Code

Please make sure you have all usual dependencies installed on your system. The most important ones include `python`, `pip` and `ipykernel`. If you're using _Visual Studio Code_ for development, you should be prompted to install them automatically. Next, follow this process:

1. Create the virtual environment: `python -m venv venv`
2. Enter `venv`: `source venv/bin/activate` on Linux or `venv\Scripts\activate.bat` on Windows
3. Upgrade your `pip`: `pip install --upgrade pip`
4. Install dependencies from the requirements file: `pip install -r requirements.txt`
5. Navigate to the Model directory and open the Jupyter Notebook IDE of your choice. Select the Python version from inside the `venv` you just created when prompted by `ipykernel` package. Suggested command: `python -m notebook`

## Miscellaneous
See prior project attempt in [cmd_forecast](https://github.com/afoster28/cmd_forecast) repo.

## To do
- Relate forecasted economic variables with observed variables
- Make periods dynamic to allow for implementation in systematic trading infrastructure
- Embed DSGE model in systematic trading infrastructure and check initial performance