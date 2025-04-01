Efficiency Frontier Analysis


Introduction

I analyzed the efficiency frontier for this project by selecting a basket of seven individual stocks traded on the New York Stock Exchange (NYSE). The objective was to determine the correlation between these stocks and observe how the efficiency frontier behaves with a randomly selected portfolio. The efficiency frontier is a fundamental concept in portfolio optimization, demonstrating the trade-off between risk and return.


Stock Selection

The stocks selected for this project were:

  - Apple (AAPL)

  - Microsoft (MSFT)

  - Google (GOOGL)

  - Amazon (AMZN)

  - J.P. Morgan (JPM)

  - Bank of America (BAC)

  - Lockheed Martin (LMT)


Data Collection and Processing

To analyze stock price movements, I extracted historical stock price data using Yahoo Finance. The dataset spans three years, with the end date set to the day the script is executed. Only adjusted closing prices were considered to account for corporate actions like stock splits and dividends.

After retrieving the data, I computed the daily returns for each stock and removed any missing values (NaN) to ensure data integrity. The key statistical metrics calculated were the mean (average return) and variance (risk) of the returns, which serve as fundamental inputs for portfolio optimization.


Correlation Analysis

A correlation matrix was generated to examine the relationships between the selected stocks. The correlation coefficient values range between -1 and +1, where:

  - +1 indicates a perfect positive correlation (stocks move in the same direction).

  - -1 indicates a perfect negative correlation (stocks move in opposite directions).

  - 0 indicates no correlation.

From the correlation matrix, it became evident that stocks within the same sector exhibited stronger correlations. For example:

  - Technology sector: AAPL, GOOGL, and MSFT showed a high degree of correlation.

  - Financial sector: BAC and JPM displayed strong positive correlation.



Annual Returns and Volatility

Next, I calculated annual returns and annual standard deviation (volatility). To simplify further computations, these were renamed as "Returns" and "Volatility," respectively.

A second correlation matrix was created, this time illustrating the relationships between the percentage changes in stock returns rather than absolute price movements.


Portfolio Simulation

With the necessary statistical metrics computed, I proceeded to simulate a portfolio using the following framework:

  - Weight Calculation: The sum of all stock weights in the portfolio must equal 1.

  - Portfolio Returns: Computed by multiplying the stock weights by their respective       
  - annual returns.

  - Risk Computation: Further calculations were conducted and stored in a data frame   
    for visualization.


Efficiency Frontier Visualization

The efficiency frontier was plotted as a scatterplot representing all possible portfolio returns and correlations between assets. This graphical representation highlights the trade-off between risk and return. Key observations include:

The efficiency frontier helps identify optimal portfolio allocations that maximize returns for a given level of risk.

Diversification is a crucial factor in risk mitigation.

Each blue dot in the scatterplot represents a unique portfolio allocation. It represents the trade-off between expected returns on and volatility (risk) for different portfolio allocations.

![b9198b56-a98c-4de9-afe1-8867919af500](https://github.com/user-attachments/assets/2b86846d-ead2-4135-9dab-774a036b2f8c)

Each portfolio allocation was assigned a unique color in the scatterplot to enhance clarity. 

![c89b2957-f4ea-4f1f-834f-0b696f309680](https://github.com/user-attachments/assets/3b910121-fc69-4411-9ac3-ed2ac094e3c1)

Here we can see the black x marker. The black "X" marker represents the portfolio with the lowest possible risk. It's located on the far left because that is where volatility is at its minimum. 
The returns for this selection would be moderate, meaning is prioritizes stability over anything. Thus, this portfolio selection would have minimal fluctuations.

![1640d1e3-18de-4443-b648-3cc7f8db1314](https://github.com/user-attachments/assets/7934961a-e431-469a-9d7f-4ab25f33a70b)

The two markers show the:

  - Minimum Volatility Portfolio (Black X):

    This is the portfolio with the lowest possible risk (volatility).

    It is located on the far left of the plot.

    Investors who are highly risk-averse may prefer this portfolio.
    
  - Optimal Risk Portfolio (Blue X):

    This is the portfolio that offers the best risk-return trade-off.

    It is typically chosen based on the Sharpe Ratio, which maximizes return per unit       of risk.

    It lies on the efficient frontier where return is maximized for a given risk level.


![1efb0441-ecec-4460-bbc1-02eebc5b0fb1](https://github.com/user-attachments/assets/d91e30d6-212e-4146-9242-40269378e639)


The most efficient region for diversification and risk mitigation is located between the minimum volatility portfolio and the optimal risk-return point, which is highlighted in gray shading on the plot. Anything outside of the gray shading would not align with our risk level.

![3f170b40-63de-4944-a27a-3c4a5c25a0af](https://github.com/user-attachments/assets/80c6731f-15d6-4dcd-8866-f836f1fb9149)


Conclusion

The Efficiency Frontier is important to visualize the fundamental trade-off between risk and return in portfolio optimization. I simulated thousands of allocations and  calculated how to optimise the portfolio with my chosen assets.

  - Diversification: Highlights how diversity in a portfolio allows for reducing the overall portfolio risk. Stocks within the same sector are heavily correlated, while others aren't.
  - Efficiency Frontier: Provides a visual representation of the best risk-return combinations.

The 'Sweet Spot' is selected within the Minimum Volatility and Optimal Risk area. These two marks highlight the sweet spot of investing.

  - Minimum Volatility Portfolio -> suitable for risk-averse investors prioritizing stability
  - Optimal Risk Portfolio -> ideal for investors seeking a balanced approach to risk and reward

Understanding these two factors in a portfolio will help secure more success than long-lasting failure and loss of money.
