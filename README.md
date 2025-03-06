# 🛒 E-commerce Customer Segmentation

## 📌 Project Overview
This project applies **unsupervised learning (clustering)** techniques to segment e-commerce customers based on their **transactional behavior and demographics**. The goal is to identify customer groups that share similar behaviors and use these insights to optimize **coupon marketing strategies**.

## 🚀 Key Objectives
1. **Data Cleaning & Feature Engineering**  
   - Merge multiple datasets (`customers`, `transactions`, `branches`, etc.).
   - Create meaningful features like `burn_rate`, `claimed_frequency`, etc.
2. **Customer Segmentation using Unsupervised Learning**  
   - Apply **K-Means Clustering** to segment customers.
   - Evaluate model performance using **Silhouette Score & Inertia**.
3. **Business Insights & Recommendations**  
   - Identify **high-value customers** for premium offers.
   - Optimize coupon campaigns to improve engagement.

---

## 📊 Datasets Used
The dataset consists of **five tables**:
- **Customers:** (`customer_id`, `join_date`, `city_id`, `gender_id`)
- **Genders:** (`gender_id`, `gender_name`)
- **Cities:** (`city_id`, `city_name`)
- **Transactions:** (`transaction_id`, `customer_id`, `transaction_status`, `burn_date`, `branch_id`)
- **Branches & Merchants:** (`branch_id`, `merchant_id`, `merchant_name`)

All datasets were cleaned and merged into a single customer-level dataset.

---

## 🏗️ Tech Stack
- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- **Machine Learning:** K-Means Clustering
- **Power BI / Tableau:** Visualizing customer insights

---

## 📌 Methodology

### **1️⃣ Data Preprocessing**
- Merged **customers, transactions, cities, and branches** tables.
- Handled missing values (`burn_date` filled with `"Not Burnt"`).
- Created **new features**:
  - `claimed_frequency`: Total coupons claimed per customer.
  - `burn_frequency`: Total coupons successfully redeemed.
  - `burn_rate`: % of claimed coupons that were burnt.

---

### **2️⃣ Customer Segmentation Using K-Means**
- Standardized the dataset using `StandardScaler`.
- Determined the **optimal number of clusters** using the **Elbow Method**.
- Applied **K-Means Clustering** (`k=4`).
- Evaluated performance using:
  - **Silhouette Score**: Measures how well the clusters are separated.
  - **Inertia**: Measures within-cluster variance.

---

### **3️⃣ Business Insights & Recommendations**
| **Cluster** | **Characteristics** | **Business Strategy** |
|------------|-------------------|-----------------|
| **Cluster 0** | High transactions, high burn rate | Provide premium rewards for retention. |
| **Cluster 1** | Low transactions, rarely burn coupons | Offer discounts to increase engagement. |
| **Cluster 2** | High claimed but low burnt | Send reminders & time-limited offers. |
| **Cluster 3** | Moderate engagement | Maintain customer loyalty programs. |

---

✅ **Final Business Takeaways:**
1. **Boost retention** for loyal users (Cluster 0) through exclusive deals.  
2. **Increase engagement** for inactive users (Cluster 1) via targeted promotions.  
3. **Encourage coupon burning** for customers who claim but don’t use them (Cluster 2).  
4. **Sustain moderate users** (Cluster 3) with occasional incentives.  
