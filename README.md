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
       - Standardized product categories (e.g. Car and mobile , house and office equipment....
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
![IMG_20250705_103337_438](https://github.com/user-attachments/assets/ce89d8ec-8854-49a3-b00a-e3f8aa2cccc8) Pivot table showing the total number of reviews per category.
4. The products with the highest average ratings is Fire-Boltt Ninja Call Pro Plus 1.83" Smart Watch with Bluetooth Calling, AI Voice Assistance, 100 Sports Modes IP67 Rating, 240*280 Pixel High Resolution with 5.0 avearge ratings.
5. The average actual price is ₹5,691.18 while the discounted price is ₹3,304.80 by category as shown in the pivot table below. This implies an average discount of **₹2,386.38** (about 42% across all products.
![IMG_20250705_130558_322](https://github.com/user-attachments/assets/8ee33b0d-68e4-413b-bad4-4130f13091cd)
- Category-wise discount analysis: **Electronics** has the highest absolute discount (₹4,192 savings) despite moderate *percentage discount* (40.2%). This indicates volume-driven startegy.
- Toy & Games shows **no discounts** despite competitive market. The risk here is loosing price-sensitive customers during festive periods.
- Office Products is under-discounted. Only 24.1% discount vs category average of 44.9%
6. 
7. 
8. 

     
        
     
