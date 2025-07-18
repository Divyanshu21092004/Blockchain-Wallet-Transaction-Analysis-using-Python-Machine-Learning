# Blockchain-Wallet-Transaction-Analysis-using-Python-Machine-Learning

This project analyzes DeFi wallet transactions from raw JSON data to extract behavioral insights and compute a custom user score using machine learning. The aim is to identify meaningful wallet activity patterns such as frequency, volume, and diversity of actions.


 Objective

To process raw on-chain wallet transaction data, extract relevant features from nested JSON (`actionData`), and generate a user scoring system using clustering techniques (like KMeans).

---

Project Features

-  Parses complex JSON files containing wallet transaction history
-  Extracts and cleans relevant fields such as `amount`, `timestamp`, `action`, `protocol`
-  Normalizes and aggregates user transaction behavior
-  Applies unsupervised learning (KMeans Clustering) to group users
-  Assigns behavior-based scores to wallets
-  Visualizes wallet behavior trends

Features Extracted

From each wallet's transaction history, the following features were engineered:

- Total number of transactions
- Total transaction volume (`amount`)
- Number of unique protocols used
- Diversity in actions (`Deposit`, `Withdraw`, etc.)
- Time-based behavior (e.g., avg time between txns)

 🤖 ML Approach
 
- Unsupervised Learning (KMeans Clustering)** was chosen due to the absence of labeled data. It enables natural grouping of users based on behavior without predefined categories.
- Used **KMeans Clustering** to segment wallets based on transactional behavior.
- Assigned wallet scores based on cluster centroids (e.g., Cluster 0 = low activity, Cluster 2 = high-value user).
