# Household-Power-Consumption-Analysis

**Project Title: Household Power Consumption Analysis and Forecasting Using LSTM**

**Overview:**
The "Household Power Consumption Analysis and Forecasting Using LSTM" project focuses on analyzing and forecasting the global active power consumption in a household over nearly four years. The dataset includes features such as Date, Time, Global_active_power, Global_reactive_power, Voltage, Global_intensity, Sub_metering_1, Sub_metering_2, and Sub_metering_3. The analysis incorporates data cleaning, statistical tests for normality, and LSTM (Long Short-Term Memory) neural network modelling for accurate power consumption forecasting.

**Key Features:**

1. **Data Cleaning and Statistical Analysis:**
   - Conducted data cleaning to handle missing values and ensure dataset integrity.
   - Utilized statistical tests, including D’Agostino’s K^2 Test, to assess the normality of the data.
   - Examined kurtosis and skewness to understand the distribution of the Global_active_power variable.

2. **Temporal Trends Analysis:**
   - Analyzed temporal trends in power consumption through boxplots, revealing monthly, quarterly, and yearly variations.
   - Identified patterns such as increased power consumption in winter months and lower consumption in summer.

3. **Dickey-Fuller Test for Stationarity:**
   - Employed the Dickey-Fuller test to assess stationarity in the time series data.
   - Differentiate between the null hypothesis (presence of a unit root) and the alternative hypothesis (absence of a unit root) to determine stationarity.

4. **LSTM Model Architecture:**
   - Constructed an LSTM neural network model for time series forecasting.
   - The model architecture includes an LSTM layer with 100 units, a dropout layer to prevent overfitting and a dense layer for output.
   - Compiled the model using mean squared error as the loss function and the Adam optimizer.

5. **Training and Validation:**
   - Trained the LSTM model on the preprocessed data, specifying 20 epochs and a batch size of 70.
   - Incorporated early stopping to monitor and halt training when validation loss ceases to improve.

6. **Model Evaluation:**
   - Evaluated the model's performance using metrics such as mean squared error, assessing the accuracy of power consumption predictions.

7. **Conclusion and Insights:**
   - Analyzed the temporal patterns and trends in household power consumption, revealing seasonality and variations.
   - Confirmed non-Gaussian distribution of the Global_active_power variable through statistical tests.
   - Employed the LSTM model to forecast future power consumption, leveraging the neural network's ability to capture temporal dependencies.

**Model Summary:**
```
Layer (type)                 Output Shape              Param #   
=================================================================
lstm_1 (LSTM)                (None, 100)               52400     
_________________________________________________________________
dropout_1 (Dropout)          (None, 100)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 101       
=================================================================
Total params: 52,501
Trainable params: 52,501
Non-trainable params: 0
_________________________________________________________________
```

The "Household Power Consumption Analysis and Forecasting Using LSTM" project offers valuable insights into power consumption trends, providing a foundation for more accurate forecasting and better resource management in households. The LSTM model's ability to capture temporal dependencies makes it a powerful tool for predicting future power consumption patterns, contributing to efficient energy planning and consumption optimization.
