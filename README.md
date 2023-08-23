# **GEXXER**
## Reveal the most important GEX levels on the Yahoo Option Chain data

### Example of GEX levels
![](https://github.com/erma0x/gexxer/blob/main/documents/plot%20output/Screenshot%20from%202023-05-30%2002-08-57.png)

### Exammple of calls and puts volumes

![](https://github.com/erma0x/gexxer/blob/main/documents/plot%20output/Screenshot%20from%202023-05-30%2000-18-14.png)


### Market Movement Analysis with
- Gex levels used as supports and resistences.
- Trend following.
- Fibonacci Retreacements
- Elliot Waves
- VIX
- Wychoff Supply and Demand
- Strike Price Delta Neutral
- Yahoo Finance's Option Chain


### Mathematical model of GEX
```
GEX = (open interest calls * calls gamma) - (open interest puts * puts gamma)
```

The code provided implements a trading strategy based on an indicator calculated using data on the strike price, open interest and range of call and put options, together with historical prices of the underlying and the VIX. Below is the documentation for the code:

1. **Importing required libraries:**
    - We use `pandas` for tabular data manipulation.

2. **Data on strike prices, open interest and options range:**
    - `strike_price`: A list containing the strike prices of the options.
    - `open_interest_call`: A list containing the open interest of call options.
    - `open_interest_put`: A list containing the open interest of put options.
    - `gamma_call`: A list containing the range values of the call options.
    - `gamma_put`: A list containing the gamma values of the put options.
    - This data is provided as fictitious examples and should be replaced with real data.

3. **Historical prices of the underlying and the VIX:**
    - `prices_underlying`: A list containing the historical prices of the underlying.
    - `historic_vix`: A list containing the historical values of the VIX.
    - This data is provided as fictitious examples and should be replaced with real data.

4. **Trading Indicator Calculation:**
    - An indicator is calculated using strike price, open interest and option range data.
    - The indicator is calculated for each item in the strike price list and stored in a new list called `indicator`.

5. **Creating a DataFrame for the data:**
    - Data is organized in a DataFrame using the `pandas` library.
    - The DataFrame is created with the following columns: 'Strike Price', 'Open Interest Call', 'Open Interest Put', 'Gamma Call', 'Gamma Put', 'Indicator', 'Underlying Price', 'Historical VIX' .
    - This allows you to easily manipulate and analyze the data.

6. **Calculation of indicator statistics:**
    - The mean and standard deviation of the calculated indicator is calculated.
    - The mean is stored in the `mean_indicator` variable and the standard deviation in the `standard_deviation_indicator` variable.

7. **Trading Strategy Execution:**
    - The trading strategy is executed for each row of the DataFrame, starting from the second row (index 1).
    - If the indicator is above the mean plus the standard deviation and the current historical VIX is greater than the previous historical VIX, a buy transaction is executed.
    - If the indicator is below the mean minus the standard deviation and the current historical VIX is less than the previous historical VIX, a sell transaction is executed.
    - A message with information about the

purchase or sale transaction (strike price and price of the underlying).
    - You need to add logic for the actual execution of buy and sell operations.

This is the documentation for the provided code. Remember that this is just an example trading strategy and may require further adaptation and customization to apply in a real trading environment.
