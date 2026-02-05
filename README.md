# mini-project-3

# Problem Description
This business problem we are solving is segmenting customers shopping in a mall. We are trying to target marketing campains to different segments of customers. We believe unsupervised learning is appropriate for this project because unsupervised learning splits data into easily identifiable groups.

# Dataset Description
Source: [Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

Size: 200 samples

Features:
- CustomerID: Unique ID assigned to customer
- Gender: Gender of the customer
- Age: Age of the customer
- Annual Income (k$): Annual Income of the customer
- Spending Score (1-100): Score assigned by the mall based on customer behavior and spending nature.

Preprocessing
- Numeric features scaled using sklearn's StandardScaler.
- Gender encoded to numeric

# Setup

## Prerequesties
- Python 3.8+
- pip package manager

## Installation
1. Clone the repository
```
git clone https://github.com/<your-username>/mini-project-3.git
cd mini-project-3
```

2. Install dependencies:
```
pip install -r requirements.txt
```

3. Download the dataset
    - From the `\data` folder
    - Download from Kaggle and import to `\data` folder

## Running the notebook
```
jupyter notebook notebooks\analysis.ipynb
```

# Results Summary

## Optimal K

We choose K=6 because the elbow method indicated a significant change, this K had the highest silhouette score, and we want to identify as many significant customer segmentations as possible.


## Cluster Description

Cluster 0 (Moderate Shopper): Slightly female, late middle age, middle income, middle spending score

Cluster 1 (Trendy Customer): Slightly female, early middle age, high income, high spending score

Cluster 2 (Budget Female Spender): Mostly Female, middle age, low income, low spending score

Cluster 3 (Stingy Buyer): Slightly Male, middle age, high income, low spending score

Cluster 4 (Young Consumer): Slightly Female, young adult, low income, high spending score

Cluster 5 (Young Female Customer): Mostly Female, young adult, middle income, middle spending score

## Anomalies

6 anomalies found
- 1 VIP customer (high spending score and high income)
- 3 low spenders (low income and low spending score)
- 2 potential errors (income and spending score correlates negatively)

## Key Business Insights
The biggest business insight is that Cluster 3 is not spending as much in the mall as they should be. This is especially true considering the lack of anomalies within cluster 3 with only 1.

The second big business insight is that age could potentially indicate what specific products would get a cluster to spend more in the mall. For example, the younger clusters could be marketed to spend more on trendy products.

# Key Contributors
Nicky Cheng: Parts 1 and 4 + README + Report

Vibhor Malik: Parts 2 and 3 + Report