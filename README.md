# prophet-challenge
Module 8 Challenge
## Step 1
There is multiple ways to display DataFrames.  But this one reqired "display" instead of print or just typing the DataFrame name .

### *visualizing_time_patterns_solution.ipynb*
sp500_volume.groupby(group_level).mean().plot()
median_monthly_traffic = df_mercado_trends['Search Trends'].groupby(by=[df_mercado_trends.index.year, df_mercado_trends.index.month]).sum().median()

## Step 2
### *visualizing_time_patterns_solution.ipynb*
sp500_volume.groupby(by=[sp500_volume.index.year, pd.DatetimeIndex.isocalendar(sp500_volume.index).week]).mean().plot(
df_mercado_trends.groupby(by=[df_mercado_trends.index.isocalendar().day]).mean().plot()


## Step 3
### *stock_volatility_google_trends_solution.ipynb*
df_apple = pd.concat([df_stock, df_trends], axis=1).dropna()
df_merge = pd.concat([df_mercado_stock, df_mercado_trends], axis=1)

*Visualize the close and Search Trends data*
*Plot each column on a separate axes using the following syntax*
*`plot(subplots=True)`*  (did not work)
print(first_half_2020_df.plot(subplots=True))

## Step 4
### *data-prep-time-series_solution.ipynb*
*Label the columns ds and y so that the syntax is recognized by Prophet*
df_prophet.rename(columns={'Date': 'ds', 'Search Trends': 'y'}, inplace=True)

*Drop an NaN values from the prophet_df DataFrame*
df_prophet = df_prophet.dropna()

*View the first and last five rows of the mercado_prophet_df DataFrame*
display(df_prophet.head())
display(df_prophet.tail())

### *forecasting-bitcoin-prices_solution.ipynb*
Fitting the Prophet model
pro_fun.fit(df_prophet)

### *time-series-forecasting-prophet.ipynb*
Makeing a forescast based on future DataFrame
future_df[['yhat','yhat_lower','yhat_upper']].head()

