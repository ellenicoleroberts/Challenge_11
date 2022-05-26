<img src= "images/ba.png" width="930" height="300">

# MercadoLibre: Forecasting Net Prophet

 This Jupyter notebook builds a financial database and web application by using SQL, Python, and the Voilà library for the purpose of analyzing the performance of a hypothetical fintech ETF consisting of four stocks: GOST, GS, PYPL, and SQ. Each stock has its own table in the etf.db database (included in this repo).

---

## Technologies

This application leverages python 3.7 with the following packages that require additional installation:

* pandas: an open-source library that offers easy-to-use data analysis tools for Python.
* fbprophet: FbProphet is a powerful time series analysis package released by Core Data Science Team at Facebook.
* hvplot: hvPlot provides a high-level plotting API built on HoloViews that provides a general and consistent API for plotting data.
* holoviews: Python library designed to make data analysis and visualization seamless and simple.
* matplotlib: a comprehensive library for creating static, animated, and interactive visualizations in Python.

---

## Installation Guide

Begin by cloning the GitHub repo (the same repo that this README.md file is contained within) into your terminal. 

Because this code uses [Facebook Prophet library](https://facebook.github.io/prophet/), which can be difficult to install on some machines, we recommend using the Google Colab IDE. Google Colab allows you to run Jupyter Notebooks in the cloud. By installing libraries within Google Colab instead of onto your machine, you are installing them only temporarily, in memory, while using the cloud. 

To configure a [Google Colab](https://colab.research.google.com/) workspace:

* Open Google Colab and upload the notebook contained within this repo.

* Run the provided code in the notebook's install section and import the required libraries and dependencies in the following section.

---

## Usage

The first part of this notebook analyzes PayPal (PYPL). It makes an SQL query to obtain all data from the PYPL table. Using hvPlot, an interactive visualization for the PYPL daily returns is created as well as an interactive visualization for the PYPL cumulative returns. 

The closing prices for PYPL that are greater than 200 are then selected with another SQL query. Further, again using an SQL query, the top 10 daily returns for PYPL are obtained.

Next, using SQL, the notebook builds an ETF portfolio and then evaluates its performance. To do so, an SQL query is used to access each table in the database and joins them into a single DataFrame. The daily returns are then calculated for each stock, followed by the daily returns for the entire ETF by averaging the daily returns of each stock for a given day (assuming an equal-weighted portfolio). These ETF daily returns are then used to calculate the annualized returns and the cumulative returns for the ETF. The cumulative return values of the ETF portfolio are visualized with an interactive line plot using hvPlot.

---

## Contributors

Nicole Roberts,
elle.nicole.roberts@gmail.com

---

## License

[BSD 3](https://choosealicense.com/licenses/bsd-3-clause-clear/): BSD 3-clause is a permissive licence, allowing nearly unlimited freedom with the software as long as BSD copyright and license notice is included.
