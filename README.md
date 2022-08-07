## Customer-Segmentation

#### Clean and Apply RFM technique to rank and group clusters to identify the best customers and perform targeted marketing campaigns, using real online transaction data


### Description

**Apply RFM technique to derive our business goals!** 

#### Marketing Technique: Using RFM (Recency, Frequency, Monetary) Marketing model
* **Recency** : last time customer made a purchase, more likely to repeat than a old customer
* **Frequency** : how many times a customer made a purchase, who purchases often is likely to come back
* **Monetary Value** : amount of money a customer has spent within that timeframe, large purchases likely to return than a customer who spends less

#### Business Benefits:
  1. Personalization: By creating effective customer segments, you can create relevant, personalized offers.
  2. Improve Conversion Rates: Personalized offers will yield higher conversion rates because your customers are engaging with products they care about.

#### Challenges:  

- [x] Working with a skewed Probability distribution 
- [x] Making good sense of Marketing Knowledge


### Install Setup

This project requires **Python 2.7** and the following Python libraries installed:

- [numpy](http://www.numpy.org/)
- [pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [datetime](https://docs.python.org/3/library/datetime.html)
- [seaborn](https://seaborn.pydata.org)
- [squarify](https://pypi.org/project/squarify/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. Make sure that you select the Python 2.7 installer and not the Python 3.x installer.


### Code

Template code is provided in the notebook `retail-customer-data-segmentation.ipynb` 
[Jupyter Notebook](https://github.com/YRohitha/Customer-Segmentation/blob/main/scripts/retail-customer-data-segmentation.ipynb) file.


### Run

In a terminal or command window, navigate to the top-level project directory (that contains this README) and run one of the following commands:

```bash
jupyter notebook retail-customer-data-segmentation.ipynb.ipynb
```
or
```bash
ipython notebook retail-customer-data-segmentation.ipynb.ipynb
```
This will open the Jupyter Notebook software and project file in your web browser.


### Data

The dataset used in this project will be included as `retail_data.csv`. This dataset is sourced from public domain and contains the following attributes:

**Description**

This Online Retail II data set contains all the transactions occurring for a UK-based and registered, non-store online retail between 01/12/2009 and 09/12/2011.The company mainly sells unique all-occasion gift-ware. Many customers of the company are wholesalers.

**Features**
- `Invoice` : A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.
- `StockCode` : Product (item) code. A 5-digit integral number uniquely assigned to each distinct product.
- `Description` : Product (item) name.
- `Quantity` : The quantities of each product (item) per transaction.
- `InvoiceDate` : Invoice date and time. The day and time when a transaction was generated.
- `Price` : Unit price. Product price per unit in sterling (Â£).
- `Customer ID` : Customer number. A 5-digit integral number uniquely assigned to each customer.
- `Country` : Country name. The name of the country where a customer resides.

**Transformed Features**
- `most_recent_txn` : date of their most recent transaction
- `num_orders` : number of transactions they’ve made within a consistent time frame (a year will work best)
- `total_revenue` : total amount they’ve spent during that same timeframe.

**Target Variable**
- `user_segment`: Customer Segment (111, X1X, XX1, X13, X14, 14X, 44X)

* `111`: **Core or Best Customers** : Focus on loyalty programs and new product introductions. Proven to have a higher willingness to pay, so don't use discount pricing to generate incremental sales. Instead, focus on value added offers through product recommendations based on previous purchases

* `X1X`: **Loyal Customers** : Loyalty programs are effective for these repeat visitors. Advocacy programs and reviews are also common X1X strategies. Lastly, consider rewarding these customers with Free Shipping or other like benefits.

* `XX1`: **Whales or Highest Paying Customers** : These customers have demonstrated a high willingness to pay. Consider premium offers, subscription tiers, luxury products, or value add cross/up-sells to increase AOV. Don't waste margin on discounts

* `X13` OR `X14`: **Promising - Faithful customers** : You've already succeeded in creating loyalty. Focus on increasing monetization through product recommendations based on past purchases and incentives tied to spending thresholds (pegged to your store AOV).

* `14X`: **Rookies - Your Newest Customers** : Most customers never graduate to loyal. Having clear strategies in place for first time buyers such as triggered welcome emails will pay dividends.

* `44X`: **Slipping - Once Loyal, Now Gone** : Customers leave for a variety of reasons. Depending on your situation price deals, new product launches, or other retention strategies.
