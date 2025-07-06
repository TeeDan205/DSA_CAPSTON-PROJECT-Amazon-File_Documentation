# DSA_CAPSTON-PROJECT-Amazon-File_Documentation

Excel-based analysis of 1,465 e-commerce products with pivot tables and dashboard visualization with actionable insights for product improvement and marketing strategy derived from customer reviews and pricing data.

## 📖 Project Topic: Amazon Product Review Analysis

### 🔭 Project Overview
This Data analysis project aims to provides e-commerce analytics solutions to sellers on platforms like Amazon. By analyzing the various parameters; product and consumer review data etc. in the data received we seek to gather enough information to generate insights that can guide product improvement, marketing strategies, and customer engagement. 

### ✍️ Dataset Description
- **Source**: The data was provided by the incubtor hub for the purpose of the hackathon and final Examinations of my data analysis program by the organization. The dataset contains information scraped from Amazon product pages, including: 
   - Product details: name, category, price, discount, and ratings 
   - Customer engagement: user reviews, titles, and content 
   - Each row represents a unique product, with aggregated reviewer data stored as comma-separated values 
     - Total Records: 1,465 
     - Total Fields: 16 columns

 ### 🧰 Tools Used
   1. Microsoft Excel (For Data Cleaning)
       - Handled repeated product_id column
       - Standardized product categories (e.g. Computers & Accessories, Home & Kitchen, Health & Personal Care, Care & Motorbike, Toys & Games etc.)
       - created calculated columns
   2. Pivot Tables, Conditional Formatting & Formulae (For Analysis)
   3. Microsoft Excel Charts, Slicers (Dashboard Development)
      - Interactive Filters: Category, Rating.
      - Key Visualizations:
      - Discount impacts on sales volume (Scatter plot)
      - Category Performance heatmap (rating vs discount %)
   4. Documentation: GitHub Markdown

### 👓Aims and Objectives: Some business questions listed below are to be answered:
   - What is the average discount percentage by product category?
   - How many products are listed under each category?
   - What is the total number of reviews per category?
   - Which products have the highest average ratings?
   - What is the average actual price vs the discounted price by category?
   - Which products have the highest number of reviews?
   - How many products have a discount of 50% or more?
   - What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?
   - What is the total potential revenue (actual_price × rating_count) by category?
   - What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?
   - How does the rating relate to the level of discount?
   - How many products have fewer than 1,000 reviews?
   - Which categories have products with the highest discounts?
   - Identify the top 5 products in terms of rating and number of reviews combined.

### 🧑‍🔬 Methodology 
In the initial phase of the data cleaning and preparation, the following actions were performed;
   - ⏳ **Data Acquisition and inspection:** The data was loaded and the total number of records and fields were confirmed to be the same from the source.
   - 🧹 **Data cleaning and formatting:** No product should have more than a record since it's all about reviews and ratings was made, hence all duplicated product_id were removed. Standardized product categories were created from the main category of product given because it is a multi-level category. The filter tool was used to validate each column's values.
   - 🔄 **Data Transformation:** Some Calculated columns were formed (e.g. Total Potential Revenue, Discounted price, % Discount bucket, Price Range etc.) before the dataset was turned to  table by applying ctrl+T.
   - 📊 **Analysis:** Pivot tables and the calculated column formed were used to analyse and answer the business questions.
   - 📉 **Visualization:** Built interactive charts and conditional formatting were used to present the answers.
   - 📑 **Reporting**: Insights were compiled into a dashboard with actionable recommendation.

### 💹 Exploratory Data Analysis (EDA)
The key business questions were answered through structured analysis pivot table architecture.
- Average Discount % by product category: Pivot Table (Rows `n product category, values `n Avg Discount)
- Products Listed by Category: Pivot Table [ Rows `n category, values `n Product (count)]
- High discount Flag = If([Discount]>=50, "Yes","No"), COUNTIF
- Average actual price vs the discounted price by category: Discounted price % was calculated using =((Actual price-Discount price)/Discount price)*100. Pivot Table (Rows `n product category, values `n Avg Actual price and Avg Discounted price)
- Discount Impact: Line chart with tread line
- Price Sensitivity: Bucketized analysis using formular; =IF(Discounted price<200,"<₹200",IF(OR(Discounted price=200,Discounted price<=500),"₹200 - ₹500",">₹500"))
- Product Rating and Review: Pivot table with calculated column (Average rating+(Rating count/1000)). A scale factor of 1000 was used to balance the weight.

### 🔑 Key Findings & Insights:
1.  The average discount percentage by product category is **46.7%.**

2.  Out of 1351 products, Electronic products has the highest number of products (490), Home & Kitchen products are 448, 375 products were Computer & Accessories, 31 are office products, Home Improvement and Musical Instruments have 2 products each and the Health and Toy Games have only one single product.

3. The total number of reviews per category: Electronics products has the highest reviews with 1998 reviews while the Car and Mobile products has the least review of 3.8 as shown in the pivot table below.

![pivot 3](https://github.com/user-attachments/assets/9393f630-b1ef-4279-ad45-3e5a6efe365a)

   Pivot table showing the total number of reviews per category.
4. The products with the highest average ratings is Fire-Boltt Ninja Call Pro Plus 1.83" Smart Watch with Bluetooth Calling, AI Voice Assistance, 100 Sports Modes IP67 Rating, 240*280 Pixel High Resolution with 5.0 average ratings.

5. The average actual price is ₹5,691.18 while the discounted price is ₹3,304.80 by category as shown in the pivot table below. This implies an average discount of **₹2,386.38** (about 42% across all products).

![pivot 5](https://github.com/user-attachments/assets/c7a49eb5-520a-4d70-a9f4-23e4fffcb832)

- Category-wise discount analysis: **Electronics** has the highest absolute discount (₹4,192 savings) despite moderate *percentage discount* (40.2%). This indicates volume-driven strategy.
- Toy & Games shows **no discounts** despite competitive market. The risk here is losing price-sensitive customers during festive periods.
- Office Products is under-discounted. Only 24.1% discount vs category average of 44.9%

6. **Fire-Boltt Ninja Call Pro Plus 1.83" Smart Watch** with Bluetooth Calling, AI Voice Assistance, 100 Sports Modes IP67 Rating, 240*280 Pixel High Resolution has the highest number of reviews. The fire-Boltt dominates the top 5 positions with 3 products. The top two products are both fire-boltt smartwatches, suggesting strong market presence in the wearable category.

7. **662** products have a discount of 50% or more. Almost half of all products (49%) are heavily discounted (>=50%), this suggests slow-moving inventory (especially in Electronics) and also there may be a potential overstocking issue.

8. The distribution of product ratings: Most products are rated between 3.8⭐ and 4.5⭐. **74.1% of products** (1,077) have ratings >=4.0⭐. Only **1.9% (28 products)** fall below 3.0⭐. Peak at **4.1**⭐ with 225 products (15.4% of total). Electronics (avg 4.1⭐) maintain better quality despite discounts vs Home & Kitchen (avg 3.7⭐ )

9. The total potential revenue (actual_price × rating_count) by category is shown in the pivot table below.

![pivot 9](https://github.com/user-attachments/assets/c8f7cf18-9466-4d30-8648-da7acc5950d3)

   Pivot Table showing the Total Potential revenue

  Electronics category alone contributes 91,323 million (80.3% total potential revenue). This indicates that Electronics is the core revenue driver. Heavy reliance on Electronics poses a significant risk. Any downturn in this category would drastically affect overall revenue.

10. The number of unique products per price range bucket is shown below.

![pivot 10](https://github.com/user-attachments/assets/a8306e62-8263-4a9d-8390-1b44986d31cd)

Pivot Table showing number of unique products per price range bucket.
  - 62.9% of products priced >₹500. This aligns with revenue data where Electronics (avg ₹10,418) drove 80% of revenue. This indicates strategic focus on high-value segments.
  - Only 25.3% in ₹200-₹500 range. There is optimal rating-to-price ratio (4.2⭐ avg vs 3.8⭐ for ₹500)
  - <₹200 products represent just 11.8% despite the high-volume potential.

11. Relationship between ratings and level of discounts:
    Engagement peaks at moderate and high discounts as shown in the line graphs in the dashboard section (no 7). The highest number of reviews (27,979) occurs in the 61-70% discount range. The second highest is at 21-30% (24,334) reviews. *Ratings do not linearly increase with discount.* Instead, we see peaks at 21-30% and 61-70% discount. This shows customers distrust extreme discounts.

12. **310 Products** have fewer than 1000 reviews while 1041 products have greater than 1000 reviews. This shows significant low-engagement(reviews). Nearly 1 in 4 products (23%) struggle with review generation. Low review is not discount-driven because Toy & Games product category have 0% discounts yet 36% low review. Products with <1,000 reviews show **Lower average ratings** (3.4⭐) vs high-review products (4.3⭐).
   
13. There is extreme discounting in Tech Categories: Computers & Accessories (94%), Electronics (91%), and Home & Kitchen (90%) have the highest discounts, all above 90%. This suggests aggressive discounting strategies in these categories, possibly due to high competition, rapid obsolescence (for electronics), or overstocking.
    
14. The top 5 products in terms of rating and number of reviews combined are:

![pivot 14](https://github.com/user-attachments/assets/518c1b84-d4c7-41d5-afb2-b85fd7b5e745)


Pivot Table showing the top 5 products in terms of rating and number reviews combined.
  The amazon Basics High-speed HDMI cable are very popular, with three different variants each having 431 reviews. This suggests strong sales and customer engagement in the HDMI cable category. The Boat Bass Heads earphone come in two colours (red and pink) and have 368 reviews each, this is also a significant number of ratings and reviews combined. The HDMI cables and Boat Bass Head Earphones from Amazon Basics are top-selling product line, and the consistency in review counts across variants indicates uniform popularity.

### 💻 Dashboard Development and Visualization
The interactive Excel dashboard below provides key insights from the product and review analysis.
1. **Average Discount Category Chart**

![Average discount by category](https://github.com/user-attachments/assets/3fc31577-8306-48a4-9f44-d170bead6d2b)


*Key Metrics:* **Average Discount and Product Category.**

2. **Products listed under each category Chart**

![products listed](https://github.com/user-attachments/assets/fd5a2db1-3d83-46b3-bd90-cd4489851b19)


*Key Metrics:* **Product Category.**

3. **Total number of reviews by category Chart**

![Number of reviews per category](https://github.com/user-attachments/assets/eff74654-618e-4742-b89a-c2f2a11ffd87)

*Key Metrics:* **Number of Review and Product Category.**

4. **Average Actual Price VS Discounted price by Category Chart**

![Av Actual VS Discount Price](https://github.com/user-attachments/assets/c41be163-7157-408e-9de7-7cbbd9938a45)

*Key Metrics:* **Actual Price and Discounted Price.**

5. **Products with highest number of reviews chart**

![products with highest review](https://github.com/user-attachments/assets/f7269378-509b-46b2-bea8-43c776ddf5a5)

*Key Metrics:* **Number of Review and Product.**

6. **Distribution of product Ratings chart**

![product distribution](https://github.com/user-attachments/assets/0cb4751d-467a-4493-912e-53a1b37904a9)

*Key Metrics:* **Product rating and Product.**

7. **Relationship between Rating to Discount Scatter-Line graph**

![relationship btw rating to discount](https://github.com/user-attachments/assets/ff0fa064-97cc-450b-ae29-71c91a781082)

*Key Metrics:* **Product rating and Discount.**

8. **Product Categories with highest discounts Charts**

![product with highest discount](https://github.com/user-attachments/assets/7d253db2-6b62-42f8-9330-7dd57c6db959)

*Key Metrics:* **Product Category and Discount.**

9. **Top five(5) Products in terms of ratings and Reviews Pie Charts**

![Top 5 products](https://github.com/user-attachments/assets/0adac127-b600-4288-8708-26a2ccfdeeba)

*Key Metrics:* **Product rating and Product.**

10. **Number of Products with 50% discount (Doughnut Chart)**

![product with 50% discount](https://github.com/user-attachments/assets/a2f7f6be-b711-4f7b-854f-305a61a4439e)


*Key Metrics:* **50% Discount and Product.**

11. **Number of Unique Products per price Range Charts**

![number unique bucket](https://github.com/user-attachments/assets/b6bb3b8c-6d61-4d57-8066-56e8affd24cb)


*Key Metrics:* **Product and Price Range.**

**Dashboard Overview**
Below is the dashboard at a glance:⏬

![dashboard summary](https://github.com/user-attachments/assets/db23e4ad-e8f7-4190-8d74-257e0339e23a)


### 💡 Strategic Recommendations and Conclusion
   1. Cap Discount 40% for Electronics and 30% for Home & kitchen products categories.
   2. Investigate why Toys and Games product category have no discounts. If sales are lagging, consider introducing targeted discounts.
   3. Leverage on Top Products. Since Fire-Boltt smartwatches are popular, consider deeper analysis on what drives their reviews to replicate success in other categories.
   4. Monitor Customer Response and track if high-discount products show increased return rates, lower repeat purchase rates and higher review volumes with declining ratings.
   5. Increase 4.6 rated products from 6.4% to 15% and offer merchandising advantages for premium-rated suppliers.
   6. Diversification Strategy; reduce dependency on Electronics by investing in the Computer and Accessories and Home & Kitchen product category.
   7. Increase ₹200 - ₹500 products from 25% to 35% in few months to expand the mid-tier products.
   8. Focus on 20-30% discounts for new product launches and regular promotions to maximize both reviews and customer satisfaction. Investigate why 81-90% discounts have such low review.
   9. Investigate why the HDMI cables have so many reviews; is it due to high sales volume?
   10. Boost the fewer than 1000 review products by offering ₹100 coupons for verified reviews and implement post-purchase email sequence with review prompts.

## 🗝️ Key Performance Indicator (KPIs)
   - Total Number of purchase: 1351 products were purchased, suggesting strong, quality products, market reliability and customer's satisfactions and demands.
   - Total discount value amounted to ₹4,464,787.17
   - Total Actual Price sum up to ₹7,688,779.62
   - Average Product Rating: 4.1 ⭐
   - Average Rating count on product is 29,236
   - Total Potential Revenue: The business has potential revenue of ₹113,643,36,203.38 with ₹91,323.92 million from Electronics.
     
