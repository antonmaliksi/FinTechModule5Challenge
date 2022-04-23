# Protoype Financial Anaylsis Application

To the Chief Technology Officer of the Credit Union, I present to you the prototype application that will equip <br> your credit union members with the ability to evaluate their financial health.

This prototype application will provide two financial analysis tools:
1. A financial planner for emergencies that will determine if the member has enough <br> reserves for an emergency fund; includes visuals for friendly interpretation of data.
2. A financial planner for retirement that will forecast the performance of their <br> retirement portfolio in ten and thirty years; includes visuals for friendly interpretaion of data.

These tools have been streamlined for ease of use and, more prominently, to allow <br> your members to assess vital data like their monthly budgets and forecast a reasonably effective <br> retirement plan that considers their current holdings of cryptocurrencies, stocks, and bonds.

---

## Technologies

To create this application, we have used Python 3 and the following packages:
1. Pandas
2. Numpy
3. Matplotlib
4. OS
5. JSON
6. Dotenv
7. Alpaca Trade API
8. Monte Carlo Forecast Tools

---

## User Guide

To begin using the notebook in Jupyter Labs:

### Part 1
1. Open "financial_planning_tools.ipynb"
2. Look for the following:
    '''python
    load_dotenv("api.env")
    '''
This line is vital to the entire application. ##__ATTENTION: Please ensure that the <br> ".env" located within the parent folder has your own API keys. Without the API key and Secret Key, <br> this notebook will be unable to extract the necessary market data essential for <br> the systemic processes in this application.

###__For help with obtaining an Alpaca API key and Secret key, [click here](https://alpaca.markets/learn/connect-to-alpaca-api/).

3. Look for the following:
    '''python
    btc_coins = 1.2
    eth_coins = 5.3
    '''
The value "1.2" is assigned to the "btc_coins" simply means that the current portfolio has 1.2 BTC. Adjust the amount of coins as necessary or add new variables. <br> For example, if the member has 68.3 ALGO, your new code will appear as:

    '''python
    algo_coins = 68.3
    '''
### Part 2
1. Look for the following:
    '''python
    start_date = pd.Timestamp("2020-08-07", tz="America/New_York").isoformat()
    end_date = pd.Timestamp("2020-08-07", tz="America/New_York").isoformat()
    '''
These lines of code enable the user to find the current prices of the relevant markets previously set. <br> ##__NOTE: You will see this syntax throughout the application, and the start/end date <br> will be used for previous dates to aquire historical data. Please be mindful of your start and end date when attempting to gather data.

### Part 3
1. Look for the following:
    '''python
    MC_60_40 = MCSimulation(
        portfolio_data = historical_data_df,
        weights = [.60,.40],
        num_simulation = 500,
        num_trading_days = 252 * 30
    )
    '''
What we have created here is a set of parameters for our Monte Carlo simulation. "weights" references the <br> split (or allocation) of funds within the portfolio. "num_simulation" is how many simulations you would <br> like to run; ##__Warning: A higher value will tax your computer and may, in some instances, cause your computer to crash.__## <br> "num_trading_days" is the number of trading days in a year, multiplied by <br> the number of years you want to forecast. For example, if the member wants to <br> forecast the next twenty years, your new code will appear as:

    '''python
    num_trading_days = 252 * 20
    '''

For further assistance, please contact me directly via email or Slack.

---

## Documentation
Please reference the following screenshots for guidance with any changes within the code:

Crypto Holdings                       |  New Crypto Holdings
:------------------------------------:|:------------------------:
![Alt text](url)                      |  ![Alt text](url)

Monte Carlo Simulation                |  New Simulation
:------------------------------------:|:------------------------:
![Alt text](url)                      |  ![Alt text](url)

---

## Contributors
Coding and data analysis was completed by Anton Maliksi from Maliksi FinTech Consulting Firm LLC.

---

## License
No licenses were used for this application.