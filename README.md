# Financial_Planning
Objective: Create two financial analysis tools: financial planner for emergencies and for retirement 

## Instructions 
### Part 1: Build the Financial Planner for Emergencies 
In this section, you’ll create a personal financial planner for emergencies. To develop the prototype, assume the following:
* The average monthly household income for each credit union member is $12,000.
* Each credit union member has a savings portfolio that consists of a cryptocurrency wallet, stocks, and bonds.

#### Evaluate the Cryptocurrency Wallet by Using the Requests Libary 
In this section, you’ll determine the current value of a member’s cryptocurrency wallet. You’ll collect the current prices for the Bitcoin and Ethereum cryptocurrencies by using the Python Requests library. For the prototype, you’ll assume that the member holds the 1.2 Bitcoins (BTC) and 5.3 Ethereum coins (ETH). To do all this, complete the following steps:
1. Create a variable named monthly_income, and set its value to 12000.
2. Use the Requests library to get the current price (in US dollars) of Bitcoin (BTC) and Ethereum (ETH) by using the API endpoints that the starter code supplied.
3. Navigate the JSON response object to access the current price of each coin, and store each in a variable.
4. Calculate the value, in US dollars, of the current amount of each cryptocurrency and of the entire cryptocurrency wallet.

#### Evaluate the Stock and Bond Holdings by Using the Alpaca SDK 
In this section, you’ll determine the current value of a member’s stock and bond holdings. You’ll make an API call to Alpaca via the Alpaca SDK to get the current closing prices of the SPDR S&P 500 ETF Trust (ticker: SPY) and of the iShares Core US Aggregate Bond ETF (ticker: AGG). For the prototype, assume that the member holds 110 shares of SPY, which represents the stock portion of their portfolio, and 200 shares of AGG, which represents the bond portion.  

#### Evaluate the Emergency Fund 
In this section, you’ll use the valuations for the cryptocurrency wallet and for the stock and bond portions of the portfolio to determine if the credit union member has enough savings to build an emergency fund into their financial plan. 

### Part 2: Create a Financial Planner for Retirement 
In this section, you’ll use the Alpaca API to get historical closing prices for a retirement portfolio. You’ll then run Monte Carlo simulations to forecast the portfolio performance 30 years from now. You’ll use the simulated data to answer questions in your Jupyter notebook about the portfolio.

#### Create the Monte Carlo Simulation 
Use the MCForecastTools library to create a Monte Carlo simulation for the member's savings portfolio 

#### Analyze the Retirement Portfolio Forecasts 
Using the current value of only the stock and bond portion of the member's portfolio and the summary statistics that you generated from the Monte Carlo simulation, answer the following question: 
* What are the lower and upper bounds for the expected value of the portfolio with a 95% confidence interval?

#### Forecast Cumulative Returns in 10 Years 
The CTO of the credit union is impressed with your work on these planning tools but wonders if 30 years is a long time to wait until retirement. So, your next task is to adjust the retirement portfolio and run a new Monte Carlo simulation to find out if the changes will allow members to retire earlier. 
For this new Monte Carlo simulation, do the following: 
* Forecast the cumulative returns for 10 years from now. Because of the shortened investment horizon (30 years to 10 years), the portfolio needs to invest more heavily in the riskier asset—that is, stock—to help accumulate wealth for retirement.
* Adjust the weights of the retirement portfolio so that the composition for the Monte Carlo simulation consists of 20% bonds and 80% stocks.
* Run the simulation over 500 samples, and use the same data that the API call to Alpaca generated.
* Based on the new Monte Carlo simulation, answer the following questions in your Jupyter notebook:
  * Using the current value of only the stock and bond portion of the member's portfolio and the summary statistics that you generated from the new Monte Carlo simulation, what are the lower and upper bounds for the expected value of the portfolio (with the new weights) with a 95% confidence interval?
  * Will weighting the portfolio more heavily toward stocks allow the credit union members to retire after only 10 years?
