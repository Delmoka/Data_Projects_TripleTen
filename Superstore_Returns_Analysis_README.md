
# 📦 Superstore Returns Analysis 

This business intelligence project analyzes product returns at Superstore to uncover what is causing high return volumes, when and where they occur most, and which categories and customer segments are most affected. The goal is to support the Superstore's CEO with insights and actionable recommendations to reduce returns and improve profitability.

---

## 🎯 Project Objective

To help Superstore leadership:
- Identify the **root causes** of returned orders
- Understand **when**, **where**, and **why** returns occur
- Recommend **targeted actions** to reduce returns and improve operations

---

## 🗂 Dataset

**Source**: Superstore Dataset  
**Tables Used**: Orders + Returns (LEFT JOIN)  
**Key Fields**:  
- `Order ID`, `Customer ID`, `Product Name`, `Category`,  
- `Sales`, `Order Date`, `State`, `Returned`

---

## 🧪 Methodology

- **Joined** the Returns table to the Orders table using a LEFT JOIN
- Created a calculated field:  
  `Returned_Flag` = IFNULL(IF([Returned]="Yes", 1, 0), 0)
- Calculated:
  - **Return Rate** = AVG([Returned_Flag])
  - **Total Returns** = SUM([Returned_Flag])

---

## 📊 Key Visuals

1. **Sales vs Returns (Scatterplot)**  
   - Showed that **high sales do not always correlate with high returns**
   - Some subcategories with lower sales had disproportionately high return rates

2. **Return Rate by Product Category (Bar Chart)**  
   - Technology and Furniture categories show the highest return rates

3. **Return Rate by Customer**  
   - Customers with more than 1 order were filtered
   - Identified high-return customers for possible follow-up

4. **Return Rate by State (Map)**  
   - California, Utah, and Oregon have high return concentration

5. **Return Rate by Month (Time Series)**  
   - Return rates spike in **August**, **September**, and **December**

6. **Combined Views (Category + State)**  
   - Highlighted Technology as the key driver in high-return states

---

## 🧱 Dashboard

- Interactive dashboard containing all key metrics:
  - Return rate by category, state, and month
  - Filters to explore patterns by product or geography
  - Hover tooltips for detailed insight

---

## 📈 Key Insights

- 📦 **Technology** is the category with the highest return rate across multiple states and months.
- 🗓️ **Returns peak in August, September, and December**, suggesting seasonality.
- 📍 **Utah, California, and Oregon** are high-return states.
- 💡 Customers with multiple orders tend to have higher return rates.
- 🛠️ Operational improvements should focus on:
  - Quality issues in high-return categories (e.g., Technology, Furniture)
  - Return policies in problematic regions

---

## ✅ Recommendations

- **Focus operational improvements** on Technology and Furniture in **California**, **Utah**, and **Oregon**
- Investigate reasons for spikes in **August, September, December**
- **Reinforce product quality checks** before shipment in high-risk categories
- Implement **targeted return-reduction initiatives** in top return states

---

## 🔄 Next Steps

- Deploy dashboard company-wide for return monitoring
- Set automated alerts for return spikes by category or state
- Launch product improvement initiatives based on category-level return trends
- Monitor effectiveness of mitigation strategies using Tableau over time

---

## 📎 How to Use This Dashboard

1. Open the Tableau story or dashboard
2. Hover over charts to view detailed metrics
3. Use tooltips and legends to identify high-risk areas
4. Take action based on insights uncovered

---

## 📍 Tableau Public Link

> [🔗 View the Interactive Dashboard on Tableau Public](#) following the link below 
(https://public.tableau.com/shared/2KRDJYYB9?:display_count=n&:origin=viz_share_link)

## 🛠 Tools Used

- **Tableau Public** for data visualization

