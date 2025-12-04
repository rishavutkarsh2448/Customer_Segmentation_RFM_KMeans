## Customer Segmentation Analysis (RFM + K-Means)

This project performs customer segmentation using RFM (Recency, Frequency, Monetary) features and K-Means clustering. The goal is to group customers into meaningful segments so that marketing teams can target high-value and at-risk customers more effectively.

## Dataset

For this project, a synthetic dataset of 10,000 customers is generated inside the notebook.  
Each customer has the following RFM features:

- **Recency**: Days since the last purchase.  
- **Frequency**: Number of orders in the period.  
- **Monetary**: Total spend in the period.

These three features are commonly used for customer value analysis and segmentation.

## Methodology

1. Generate RFM data for 10,000 customers using NumPy and store it in a pandas DataFrame.  
2. Standardize the Recency, Frequency, and Monetary features using `StandardScaler`.  
3. Apply `KMeans` clustering from scikit-learn with **4 clusters**.  
4. Assign each customer to a cluster and compute the average R, F, and M values per cluster to understand the profile of each segment.  
5. Map clusters to business-friendly segment names:
   - High-Value Loyal  
   - At-Risk High-Value  
   - New/Potential  
   - Low-Value/Churned  

## Results

- The K-Means model divides 10,000 customers into **4 distinct segments** based on their purchasing behaviour.  
- A bar chart of average Recency, Frequency, and Monetary value per cluster is used to compare segments and identify which group contains the most valuable and most at-risk customers.  
- Using these segments, a business can design targeted campaigns, for example:
  - Rewards and exclusive offers for **High-Value Loyal** customers.  
  - Win-back discounts and reminders for **At-Risk High-Value** customers.  
  - Onboarding and cross-sell campaigns for **New/Potential** customers.  

## Technologies Used

- Python  
- pandas, NumPy  
- scikit-learn (StandardScaler, KMeans)  
- Matplotlib  

## How to Run

1. Install Anaconda or Python with the required libraries (pandas, NumPy, scikit-learn, Matplotlib).  
2. Open `customer_segmentation.ipynb` in Jupyter Notebook.  
3. Run all cells from top to bottom to generate the synthetic dataset, train the model, and see the segment profiles and chart.
