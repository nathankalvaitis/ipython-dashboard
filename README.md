# Nathan Kalvaitis Case Study
Goal: Predict future day electricity usage (as measured in kWh) based on historical data utilizing analysis and Holt-Winters forecasting. Holt-Winters was chosen as it incorporates seasonality. Additional ARIMA models were tested but ultimately thrown out for proof of concept. 

Method: Explore data through python and Tableau, develop dynamic dashboard to update model parameters using ipython widgets. Dynamically update aggregates and retrain model based on dynamic user selections

Output: 

Quick EDA.ipynb - initial loading and review of data. Developed dataset to do more discovery in Tableau (ease/familiarity of use)

Dynamic Modeling.ipynb - Dynamic ipy Proof of Concept to recalculate aggregate metrics, regraph metrics, and dynamically predict future 

# Files
Quick EDA.ipynb - initial loading and review of data. Developed dataset to do more discovery in Tableau (ease/familiarity of use)
Dynamic Modeling.ipynb - Dynamic ipy Proof of Concept to recalculate aggregate metrics, regraph metrics, and dynamically predict future 
Data Preparation:

The data is loaded from a CSV file downloaded from https://www.kaggle.com/datasets/csafrit2/steel-industry-energy-consumption/data

Widgets:

Various widgets are created for selecting the training and test periods, days of the week, hours of the day, and load types.
Filtering and Plotting Function:

The filter_and_plot function filters the data based on the widget selections.
The Holt-Winters model is fitted to the training data and predictions are made for the test period.
Predictions are filtered similarly to the test data.
Error metrics and overall statistics are calculated and printed.
The results are visualized in a 2x2 grid of plots, including:
Training, Actual, and Predicted Usage.
Zoomed-in view of Actual vs Predicted Usage.
Mean Forecast Error by Hour.
Sum of Usage by Day of the Week and Hour of the Day.
Interactive Interface:

The interactive_output function is used to create an interactive interface for the widgets and the filtering/plotting function.
The widgets and interactive output are displayed.
Example Output
After running the script and interacting with the widgets, you will see various plots and statistics, including:

Training, Actual, and Predicted Usage with overall statistics as reference lines.
Zoomed-in view of Actual vs Predicted Usage.
Mean Forecast Error by Hour.
Heatmap showing the sum of Usage by Day of the Week and Hour of the Day.
