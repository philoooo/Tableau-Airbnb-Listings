# Airbnb Listings Dashboard Using Tableau
---
## Use Case
This project helps identify the most profitable areas and property features to start an Airbnb business. By exploring listing prices, seasonal trends, and property characteristics (like bedroom count and location), we gain insight into how to optimize revenue on Airbnb.

---

##  Data Source
**Dataset:** Airbnb Public Listings (2016)

- Imported Excel dataset into Tableau.
- Created a **logical table** called `Listings` by joining the `Listings` and `Calendar` tables.
- Join type: **Inner Join** on `Listings.id = Calendar.listing_id`.
![Data Source](https://github.com/philoooo/Tableau-Airbnb-Listings/blob/main/Capture.PNG)
---

##  Visualizations

### Sheet 1: Average Listing Price by Zipcode
- **Columns:** `Zipcode`
- **Rows:** `AVG(Listings.Price)`
- Used color to represent pricing variation by zip code.
- Sorted zip codes by average price.

 *Insight:* Some zip codes consistently earn more, making them ideal locations to consider for investment.

---

### Sheet 2: Filled Map - Average Price by Zipcode
- **Geographic dimension:** `Zipcode`
- **Measure:** `AVG(Price)`
- Added zip code and average price labels.
- Applied color gradients based on price.

 *Insight:* This map helps visually pinpoint which neighborhoods yield the highest returns.

---

### Sheet 3: Weekly Price Trends (Calendar Table)
- **Columns:** `WEEK(Date)`
- **Rows:** `SUM(Calendar.Price)`
- Filtered to remove final week outlier (incomplete data).
  
 *Insight:* Pricing spikes during peak travel seasons; strategic timing can boost listing profitability.

---

### Sheet 4: Average Price by Bedroom Count
- **Dimension:** `Bedrooms`
- Removed NULL and 0 values.
- **Measure:** `AVG(Price)` on Rows and Labels.

 *Insight:* Listings with more bedrooms charge higher nightly rates and tend to generate more revenue overall.

---

### Sheet 5: Count of Listings by Bedroom Count
- **Dimension:** `Bedrooms`
- Removed NULL and 0 values.
- **Measure:** `COUNT(Listings.id)`

 *Insight:* One- and two-bedroom listings dominate the market, meaning more competition. Multi-bedroom properties are less common and may offer better ROI.

---

##  Final Dashboard
- Combined all five visualizations into a single **Tableau Dashboard**.
- Set layout containers to **automatic sizing** for responsiveness.
- Organized charts for intuitive comparison.

![Dashboard](https://github.com/philoooo/Tableau-Airbnb-Listings/blob/main/Airbnb%20Dashboard.PNG)

---

##  Key Takeaways
- ** More Bedrooms = Higher Earnings**  
  While cheaper to acquire, 1-bedroom properties bring in the least. Larger listings allow for higher nightly rates and better returns.

- ** Location Drives Profitability**  
  Some zip codes consistently show higher prices. Focus on these for better market entry.

- ** Seasonality Matters**  
  People spend the most money on Airbnb in peak summer (June) and leading up to and on Christmas day. There is a sharp decline after Christmas week in January, making it a bad time to post a listing. 

- ** Lower Competition in Larger Listings**  
  Fewer 3+ bedroom listings on the platform could indicate an underserved market segment. For example, there were only 5 6-bedroom listings. A zipcode without a 6-bedroom listing would be an optimal location.

---


---

## 📎 Resources
- Dataset: [Inside Airbnb 2016 Data](https://www.kaggle.com/datasets/alexanderfreberg/airbnb-listings-2016-dataset)
- Tool: [Tableau Public](https://public.tableau.com/)

---


**Author: Rachel Curran**  
