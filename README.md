# Project: In-Vehicle Coupon Acceptance Analysis

## Executive Summary
This project investigates the factors influencing whether a driver will accept a coupon delivered to their vehicle dashboard. By examining driver demographics, contextual factors (like destination and weather), and behavioral habits (like how often they visit bars or coffee houses), I discovered that behavioral frequency and current destination are the strongest indicators of acceptance.

## The Data
The analysis was performed on a dataset containing 12,684 observations, each representing a unique scenario where a coupon was delivered to a driver. We cleaned the data by handling missing values (primarily by dropping the nearly empty 'car' column and imputing other missing values with the most frequent occurrences) to ensure the analysis was based on high-quality information.

## Key Findings: Who Accepts the Coupon?
### 1. Overall Acceptance
Across all coupon types (Bar, Coffee House, Carry Away, Cheap Restaurant, Expensive Restaurant), approximately 56.84% of coupons were accepted. However, this rate varies significantly depending on the coupon category and the driver's profile.

### 2. Bar Coupons: Frequency Matters Most
Drivers were much more likely to accept a bar coupon if they already had a habit of visiting bars.

The Habit Factor: Drivers who visit bars more than 3 times a month accepted coupons at a rate of 76.88%, compared to only 37.06% for those who visit less frequently.

The "No Kids" Advantage: Drivers who were not traveling with children as passengers and were frequent bar-goers showed an acceptance rate of over 71%.

The Age Factor: Drivers over the age of 25 who visit bars at least once a month were significantly more likely to accept coupons (~69.5%) than younger or less frequent visitors (~33.5%).

Hypothesis: The ideal target for bar coupons is an adult (25+) who is already a regular patron of such venues and is currently traveling without familial responsibilities (children).

### 3. Coffee House Coupons: Context is King
Coffee house coupons had an overall acceptance rate of 49.92%. Here, the driver's current intent played a massive role.

The "No Rush" Effect: Drivers headed to "No Urgent Place" were the most likely to stop for coffee (58.08% acceptance).

The Commute Barrier: Drivers headed to "Work" (44.06%) or "Home" (35.79%) were much less likely to accept, suggesting that people on a schedule are less willing to take a detour for coffee.

Directional Indifference: Interestingly, whether the coffee house was in the same direction the driver was already traveling or the opposite direction did not significantly impact their choice to stop.

## Conclusion: Profile of a Likely "Acceptor"
The analysis suggests that the drivers most likely to accept a coupon are those who:

Already frequent the type of business offered in the coupon (Behavioral Loyalty).

Are not under time pressure (Heading to a non-urgent destination).

Are traveling in a social context suitable for the venue (e.g., no children for a bar coupon).

## How to Use This Repository
data/coupons.csv: The raw dataset used for analysis.

coupon_acceptance_eda.ipynb: The Jupyter Notebook containing the full Python code, visualizations, and detailed statistical breakdowns.

## Requirements
To run the analysis, you will need Python with the pandas, seaborn, matplotlib, and plotly libraries installed.
