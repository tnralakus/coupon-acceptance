# Driver Coupon Acceptance Analysis

## Executive Summary
This project analyzes the factors influencing whether a driver accepts a coupon delivered to their mobile device. Utilizing a dataset from the UCI Machine Learning Repository (collected via Amazon Mechanical Turk), the study examines demographics, contextual variables, and behavioral patterns to distinguish between "acceptors" and "non-acceptors."

**Key Insight:** I discovered that **behavioral frequency** and **current destination** are the strongest indicators of acceptance.

---

## Data Overview
The dataset consists of 12,684 observations, each representing a unique scenario where a coupon was delivered to a driver. It includes diverse attributes categorized into three main areas:
* **User Attributes:** Age, gender, marital status, income, and frequency of visiting bars/restaurants.
* **Contextual Attributes:** Destination, weather, temperature, time, and passenger type.
* **Coupon Attributes:** Type (Bar, Coffee House, Carry Away, etc.) and expiration.

### Data Cleaning Highlights
* **Missing Data:** The `car` column was removed (>90% missing). Categorical missing values (~1% missing volume) were handled via mode imputation.
* **Feature Engineering:** Converted categorical frequency ranges into numeric formats to perform correlation analysis during coffee house coupon anaylsis.
* **Validation:** Outlier detection confirmed numeric stability across the dataset.

---

## Key Findings

### 1. Overall Trends
The average acceptance rate across all coupons is **56.84%**. However, performance varies wildly by category.

### 2. Bar Coupons (41.00% Acceptance)
Targeting for Bar coupons is most effective when:
* **Frequency:** The driver visits bars >3 times/month (76.88% acceptance).
* **The "No Kids" Advantage:** The driver has no children as passengers (71% acceptance).
* **Age:** The driver is over 25 years old (~69.5% acceptance).

### 3. Coffee House Coupons (49.92% Acceptance)
Acceptance is sensitive to time and intent:
* **Top Performers:** Drivers under 30 and frequent coffee house visitors.
* **Contextual Triggers:** Highest acceptance occurs at 80°F, during the morning, and when the driver has "No Urgent Place" to go.
* **Peak Segment:** Specific targeting of the above factors yielded an acceptance rate of **82.08%**.

---

## Conclusion: The "Acceptor" Profile
The most likely candidate to accept a coupon:
1.  **Is a Regular:** Already frequents that type of establishment.
2.  **Is Not Rushed:** Heading to a non-urgent destination.
3.  **Is Contextually Ready:** Traveling without children (for bars) or driving in the morning (for coffee).

---

## Setup and Installation

### Project Structure
* `data/coupons.csv`: The raw dataset containing 12,684 observations.
* `coupon_acceptance_eda.ipynb`: A comprehensive Jupyter Notebook containing data cleaning, exploratory data analysis (EDA), and visualizations.

### Prerequisites
You will need Python 3.x and the following libraries:
* `pandas`
* `seaborn`
* `matplotlib`
* `plotly`

### Running the Analysis
1. Clone the repository:
   `git clone https://github.com/tnralakus/coupon-acceptance.git`
2. Navigate to the directory and launch Jupyter:
   `jupyter notebook coupon_acceptance_eda.ipynb`
