# DSA_CAPSTON-PROJECT-Amazon-File_Documentation

Excel-based analysis of 1,465 e-commerce products with pivot tables and dashboard visualization with actionable insights for product improvement and marketing strategy derived from customer reviews and pricing data.

## 📖 Project Topic: Amazon Product Review Analysis

### 🔭 Project Overview
This Data analysis project aims to  provides e-commerce analytics solutions to sellers on platforms like Amazon. By analysing the various parameters; product and consumer review data etc in the data received we seek to gather enough information to generate insights that can guide product improvement, marketing strategies, and customer engagement. 

### ✍️ Dataset Description
- **Source**: The primary source of data used for this analysis is from Amazon product pages, including:
   - Product details: name, category, price, discount, and ratings 
   - Customer engagement: user reviews, titles, and content 
   - Each row represents a unique product, with aggregated reviewer data stored as comma-separated values 
     - Total Records: 1,465 
     - TotalFields: 16 columns

 ### 🧰 Tools Used
   1. Data Cleaning (Microsoft Excel Power Query)
       - Handled repeated product id column
       - Standardized product categories (e.g. Computers & Accessories, Home & Kitchen, Health & Personal Care, Care & Motorbike, Toys & Games etc)
       - created caalculated columns
   2. Analysis (Pivot Tables, Conditional Formating & Formulae)
   3. Dashboard Development (Excel Charts, Slicers)
      - Interactive Filters: Category, Price Range, Rating
      - Key Visualizations:
      - Discount impacts on sales volume (Scatter plot)
      - Category Performance heatmap (rating vs discount %)
   4. Documentation: Github Markdown

### 🧑‍🔬 Methodology 
In the initial phase of the data cleaning and preparation, the following actions were performed;
   - ⏳ **Data Acquisition and inspection:** The data was loaded and the total number of records and fields were confirmed to be the same from the source.
   - 🧹 **Data cleaning and formating:** An assumption that no product should have more than a record since its all about reviews and ratings was made and hence all duplicated product_id were were removed. Standardized product categories were created from the main category of product given becuase it is a multi-level category. The filter tool was used to validate each column's values.
   - 🔄 **Data Transformation:** Some Calculated columns were formed (e.g Total Potential Revenue, Discounted price, % Discount bucket, Price Range etc) before the dataset was turned to  table by applying ctrl+T.
   - 📊 **Analysis & Modeling:** Pivot tables and the calculated coulmn formed were used to analyse and answer the business questions.
   - 📉 **Visualization:** Built interactive charts and conditional formatting were used to present the answers.
   - 📑 **Reporting**: Insights were compiled into a dashbord with actionable reccomendation.

### 💹 Exploratory Data Analysis (EDA)
The key business questions were answered through structured analysis pivot table architecture.
- Average Discount % by product category: Pivot Table (Rows `n product category, values `n Avg Discount)
- Products Listed by Category: Pivot Table [ Rows `n category, values `n Product (count)]
- High discount Flag = If([Discount]>=50, "Yes","No"), COUNTIF
- Average actual price vs the discounted price by category: Discounted price % was calculated using =((Actual price-Discount price)/Discount price)*100. Pivot Table (Rows `n product category, values `n Avg Actual price and Avg Discounted price)
- Discount Impact: Line chart with treadline
- Price Sensitivity: Bucketized analysis using formular; =IF(Discounted price<200,"<₹200",IF(OR(Discounted price=200,Discounted price<=500),"₹200 - ₹500",">₹500"))
- Product Rating and Review: Pivot tble with clculated column (Average rating+(Rating count/1000)). A scale factor of 1000 was used to balance the weight.

### 🔑 Key Findings & Insights:
1.  The average discount percentage by product category is **46.7%**

2.  Out of 1351 products, Electronic products has the highest number od products (490), Home & Kitchen products are 448, 375 products were Computer & Accesories, 31 are office products, Home Improvement and Musical Instruments have 2 products each and the Health and Toy Games have only one single product.

3. The total number of reviews per category: Electronics products has the highest reviews with 1998 reviews while the Car and Mobile products has the least rreview of 3.8 as shown in the pivot table below.
![IMG_20250705_103337_438](https://github.com/user-attachments/assets/ce89d8ec-8854-49a3-b00a-e3f8aa2cccc8)

   Pivot table showing the total number of reviews per category.
4. The products with the highest average ratings is Fire-Boltt Ninja Call Pro Plus 1.83" Smart Watch with Bluetooth Calling, AI Voice Assistance, 100 Sports Modes IP67 Rating, 240*280 Pixel High Resolution with 5.0 avearge ratings.

5. The average actual price is ₹5,691.18 while the discounted price is ₹3,304.80 by category as shown in the pivot table below. This implies an average discount of **₹2,386.38** (about 42% across all products.
![IMG_20250705_130558_322](https://github.com/user-attachments/assets/8ee33b0d-68e4-413b-bad4-4130f13091cd)
- Category-wise discount analysis: **Electronics** has the highest absolute discount (₹4,192 savings) despite moderate *percentage discount* (40.2%). This indicates volume-driven startegy.
- Toy & Games shows **no discounts** despite competitive market. The risk here is loosing price-sensitive customers during festive periods.
- Office Products is under-discounted. Only 24.1% discount vs category average of 44.9%

6. **Fire-Boltt Ninja Call Pro Plus 1.83" Smart Watch** with Bluetooth Calling, AI Voice Assistance, 100 Sports Modes IP67 Rating, 240*280 Pixel High Resolution hs the highest number of reviews. The fire-Boltt dominates the top 5 positions with 3 products. The top two products are both fire-boltt smartwtches, suggesting strong market presence in the wearble category.

7. **662** products have a discount of 50% or more. Almost half of all products (49%) are heavily discounted (>=50%), this suggests slow-moving inventory (especially in Electronics) and also there may be a potential overstocking issues.

8. The distribution of product ratings: Most products are rated between 3.8⭐ and 4.5⭐. **74.1% of products** (1,077) have ratings >=4.0⭐. Only **1.9% (28 products)** fall below 3.0⭐. Peak at **4.1**⭐ with 225 products (15.4% of total). Electronics (avg 4.1⭐) maintain better quality despite discounts vs Home & Kitchen (avg 3.7⭐ )

9. The total potential revenue (actual_price × rating_count) by category is shown in the pivot table below.
![IMG_20250705_130742_205](https://github.com/user-attachments/assets/abdc09f0-551a-4833-b702-1b89ba49173b)

   Pivot Table showing the Total Potential revenue

  Electronics category alone contributes 91,323 million (80.3% total potential revenue). This indicates that Electronics is the core revenue driver. Heavy reliance on Electronics poses a significant risk. Any downturn in this category would drastically affect overall revenue.

10. The number of unique products per price range bucket is shown below.
![IMG_20250705_130812_800](https://github.com/user-attachments/assets/151f7fc5-ca53-4165-b2a8-fe577ab1c725)

Pivot Table showing number of unique products per price range bucket.
  - 62.9% of products priced >₹500. This alligns with revenue data where Electronics (avg ₹10,418) drove 80% of revenue. This indicates strategic focus on high-value segments.
  - Only 25.3% in ₹200-₹500 range. There is optimal rating-to-price ratio (4.2⭐ avg vs 3.8⭐ for ₹500)
  - <₹200 products represent just 11.8% despite the high-volume potential.

11. Relationship between ratings and level of discounts:
    Engagement peaks at moderate and high discounts as shown in the line graphs in the dashbord section. The highest number of reviews (27,979) occurs in the 61-70% discount range. The second highest is at 21-30% (24,334) reviews. *Ratings does not linearly increase with discount.* Instaed, we see peaks at 21-30% and 61-70% discount. This shows customers distrust extreme discounts.

12. **310 Products** have fewer thn 1000 reviews while 1041 products have greater than 1000 reviews. This shows significant low-engagement(reviews). Nearly 1 in 4 products (23%) struggle with review generation. Low review is not discount-driven because Toy & Games product category have 0% discounts yet 36% low review. Products with <1,000 reviews show **Lower average ratings** (3.4⭐) vs high-review products (4.3⭐).
   
13. There is extreme discounting in Tech Categories: Computers & Accesories (94%), Electronics (91%), and Home & Kitchen (90%) have the highest discounts, all above 90%. This suggests aggressive discounting strategies in these categories, possibly due to high competition, rapid obsolescence (for electronics), or overstocking.
    
14. The top 5 products in terms of rating and number of reviews combined are:
    ![IMG_20250705_130913_516](https://github.com/user-attachments/assets/1a474398-9242-4581-8070-cb1b695c8c41)

Pivot Table showing the top 5 products in terms of rating and number reviews combined.
  The amazon Basics High-speed HDMI cable are very popular, with three different vriants each having 431 reviews. This suggest strong sales and customer engagement in the HDMI cable category. The Boat Bass Heads earphone come in two colours (red and pink) nd have 368 reviews each, this is also a significant number of ratings and reviews combined. The HDMI cables and Boat Bass Head Earphones from Amazon Basics are  top-selling product line, and the consistency in review counts across variants indicates uniform popularity.

### 💻 DashBoard Development and Visualization
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

4. **Average Actual Price VS Discounted price bt Category Chart**

![Av Actual VS Discount Price](https://github.com/user-attachments/assets/c41be163-7157-408e-9de7-7cbbd9938a45)

*Key Metrics:* **Actual Price and Discounted Price.**

5. **Products with highest number of reviews chart**

![products with highest review](https://github.com/user-attachments/assets/f7269378-509b-46b2-bea8-43c776ddf5a5)

*Key Metrics:* **Number of Review and Product Category.**


### 💡 Strategic Recommendations and Conclusion
     
        
     
