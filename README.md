# Nathan Kalvaitis Case Study
Goal: Predict future day electricity usage (as measured in kWh) based on historical data utilizing analysis and Holt-Winters forecasting. Holt-Winters was chosen as it incorporates seasonality. Additional ARIMA models were tested but ultimately thrown out for proof of concept. 

Method: Explore data through python and Tableau, develop dynamic dashboard to update model parameters using ipython widgets. Dynamically update aggregates and retrain model based on dynamic user selections

Output: 

Quick EDA.ipynb - initial loading and review of data. Developed dataset to do more discovery in Tableau (ease/familiarity of use)


[Tableau Dashboard](https://public.tableau.com/app/profile/nathan.kalvaitis/viz/CaseStudy-TableauDashboardPowerUsageTrends/CaseStudy-ActualvsForecastedPowerUsage?publish=yes) - Dashboard utilized to understand data structure and trends at high level. Included dynamic comparisons vs prior week average, prior six week median, min, and max. Included placeholder for vs forecast.

![image](https://github.com/nathankalvaitis/ipython-dashboard/assets/31044210/7eb8b525-72a7-4ce5-a1ce-cb1c332604ad)

Proof of Concept.ipynb [View on Google Colab](https://colab.research.google.com/drive/1SnF-YWW2PN27cgo8dkEtYHFfp_2kWdMa) - Dynamic Proof of Concept to retrain model and update metrics based on user selections. Bugs exist related to filtering on day of week - hour - load type. The bugs are related to breaking the date indices when training the model.

![image](https://github.com/nathankalvaitis/ipython-dashboard/assets/31044210/60b49fa0-3a34-40da-801a-5f468a6df754)


# Utilizing Proof of Concept

Various widgets are created for selecting the training and test periods, days of the week, hours of the day, and load types to include. Currently, the model is only refit based on the different selections for the training and test period. Additional debugging would be required to refit Holt-Winters prediction model after removal of certain days or hours of the day.

Interactive Interface:

The interactive_output function is used to create an interactive interface for the widgets and the filtering/plotting function.
The widgets and interactive output are displayed. The displays should update any time that selections are changed - added a dummy button for now as placehold for what could be

