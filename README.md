# dsge_trading

## DSGE Models in Systematic Trading Strategies

Author: Adam Foster

Supervisor: Marcin Chlebus

This repo contains a novel systematic trading strategy setup that employs DSGE models for generating trading signals. DSGE model forecasts relative to observed macroeconomic variables provide the foundation for determining low frequency systematic trading decisions. This framework stands as a candidate investment strategy that could stand the test of time with its grounding in economic theory unlike its high frequency alternatives that typically exploit short-term structural inefficiency. It also serves as a challenge to established strategies, such as buy-and-hold or other long-term macro strategies. There is relatively low dependence on data, making this approach quick to implement without major barriers to entry.

## Tech

The models are coded in Python.

### Running the Code

Please make sure you have all usual dependencies installed on your system. The most important ones include `python`, `pip` and `ipykernel`. If you're using _Visual Studio Code_ for development, you should be prompted to install them automatically. Next, follow this process:

1. Create the virtual environment: `python -m venv venv`
2. Enter `venv`: `source venv/bin/activate` on Linux or `venv\Scripts\activate.bat` on Windows
3. Upgrade your `pip`: `pip install --upgrade pip`
4. Install dependencies from the requirements file: `pip install -r requirements.txt`
5. Navigate to the Model directory and open the Jupyter Notebook IDE of your choice. Select the Python version from inside the `venv` you just created when prompted by `ipykernel` package. Suggested command: `python -m notebook`
