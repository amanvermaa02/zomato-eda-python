# :chart_with_upwards_trend: Exploratory Data Analysis (EDA) - Zomato 

---

_An exploratory data analysis of Zomato restaurant data to understand performance, pricing, customer reviews, and popular cuisines._

---

## :spiral_notepad: Table of Contents 


- [Overview](#brain-overview)
- [Problem Statement](#jigsaw-problem-statement)
- [Dataset](#books-dataset)
- [Data Cleaning and Preparation](#pencil2-data-cleaning-and-preparation)
- [Insights](#mag_right-insights)
- [Project Structure](#chains-project-structure)




---

## :brain: Overview 

This project explores Zomato’s restaurant dataset using Python to find key trends and insights. It looks at restaurant types, popular cuisines, pricing, ratings, delivery and booking options, and the role of major restaurant chains. By cleaning the data, creating new features, and visualizing the results, the analysis helps guide business decisions and improve the customer experience.

---

## :jigsaw: Problem Statement 


**1. Online Delivery Trends**
   - How many restaurants offer online delivery, and how does this affect customer ratings?

   - Are customers more satisfied with restaurants that provide delivery options?

**2. Table Booking Insights**

   - What proportion of restaurants allow table booking?

   - Does allowing table booking have an impact on the restaurant’s overall rating?

**3. Location Analysis**

   - Which locations in Bengaluru have the highest-rated restaurants?

   - How does restaurant density vary by location, and where are the best opportunities for new restaurants?

**4. Restaurant Type & Service Patterns**

   - What are the most common restaurant types (e.g., Casual Dining, Quick Bites, Cafes)?

   - How do different restaurant types and service models influence customer ratings?

**5. Cuisine and Cost Analysis**

   - What are the typical cost structures across restaurants?

   - How does price range relate to restaurant popularity and customer satisfaction?

**6. Top Restaurant Chains**

   - Which restaurant chains dominate the Bengaluru food market?

   - How do these major chains perform in terms of ratings compared to smaller or independent restaurants?

---

## :books: Dataset 

The dataset used in this project was sourced from [Kaggle](https://www.kaggle.com/datasets/rishikeshkonapure/zomato). The dataset contains detailed information about restaurants listed on Zomato in Bengaluru, including their locations, cuisines, ratings, costs, and service options.

**Dataset Overview**

- Number of Rows: **51,717**

- Number of Columns: **17**

**Dataset Column Descriptions**

- `url` – Link to the restaurant’s Zomato webpage.
- `address` – Full address of the restaurant.
- `name` – Name of the restaurant.
- `online_order` – Indicates whether the restaurant accepts online orders (Yes/No).
- `book_table` – Shows if table booking is available (Yes/No).
- `rate` – Average customer rating given to the restaurant.
- `votes` – Total number of customer votes or reviews.
- `phone` – Contact number(s) of the restaurant.
- `location` – Locality or area where the restaurant is located.
- `rest_type` – Type or category of restaurant (e.g., Casual Dining, Cafe).
- `dish_liked` – Popular dishes recommended or liked by customers.
- `cuisines` – Cuisines served by the restaurant.
- `approx_cost(for two people)` – Estimated cost for two people dining together.
- `reviews_list` – List of user reviews and ratings for the restaurant.
- `menu_item` – Menu items offered by the restaurant.
- `listed_in(type)` – Type of service or meal category (e.g., Buffet, Delivery, Dine-out).
- `listed_in(city)` – City name in which the restaurant operates (Bengaluru in this dataset).

---

## :pencil2: Data Cleaning and Preparation 

Before performing the analysis, data cleaning and preprocessing were done to ensure the dataset was consistent, accurate, and ready for visualization.

#### :negative_squared_cross_mark: Initial Dataset Overview

* **Total Rows:** 51,717
* **Total Columns:** 17

#### :ladder: Steps Performed

1. **Renamed Columns**

   * Simplified and standardized column names for better readability and ease of use in analysis.

2. **Checked and Updated Data Types**

   * Converted the column **`approx_cost(for two people)`** to a numeric (float) data type for proper cost-based analysis.

3. **Handled Missing Values**

   * Identified missing data across several columns.
   * Summary of missing values before cleaning:

     ```
     rate             7775
     phone            1208
     location           21
     rest_type         227
     dish_liked      28078
     cuisines           45
     cost_for2         346
     rating_clean    10052
     ```
   * Missing values were handled using **mean**, **median**, **mode**, or replaced with **"Unknown"** depending on the data type and context.

4. **Checked for Duplicates**

   * Identified and removed duplicate rows to maintain data integrity.

5. **Dropped Columns with Excessive Missing Values**

   * Columns with more than **50% null or missing values** were removed.

6. **Removed Rows with Null Values**

   * Remaining rows with essential missing information were dropped to ensure clean data for analysis.

7. **Dropped Unnecessary Columns**

   * Removed irrelevant columns that were not useful for analysis like:

     ```
     'url', 'address', 'rate', 'phone', 'reviews_list'
     ```

#### :white_check_mark: Final Dataset Overview

* **Total Rows:** 43,110
* **Total Columns:** 13

---

## :mag_right: Insights

**Univariate Analysis**
1. Restaurants delivering Online or not <br>
![](/images/1.%20Restaurants%20delivering%20Online%20or%20not.png)
<br>
2. Restaurants allowing table booking or not <br>
![](https://raw.githubusercontent.com/amanvermaa02/zomato-eda-python/main/images/two_restaurants_allowing_table_booking_or_not.png)
<br>
3. Table booking vs Rating <br>
![](/images/3%20Table%20booking%20vs%20Rating.png)
<br>
4. Best Location <br>
![](/images/4%20Best%20Location.png)
<br>
5. Restaurant Type <br>
![](/images/5%20Restaurant%20Type.png)
<br>
6. Types of Services <br>
![](/images/6%20Types%20of%20Services.png)
<br> 
7. Cost of Restaurant <br>
![](/images/7%20Cost%20of%20Restaurant.png)
<br>
8. No of Restaurants in a Location <br>
![](/images/8%20No%20of%20Restaurants%20in%20a%20Location.png)
<br>
9. Most Famous Restaurant Chains in Bengaluru <br>
![](/images/9%20Most%20Famous%20Restaurant%20Chains%20in%20Bengaluru.png)
<br>
10. Rating Distributions <br>
![](/images/10%20Rating%20Distributions.png)
<br>
11. Top Cuisines <br>
![](/images/11%20Top%20Cuisines.png)
<br>

**Multivariate Analysis**
1. Relation between Location and Rating <br>
![](/images/1%20Relation%20between%20Location%20and%20Rating%20(M).png)
<br>
2. Gaussian Rest type and Rating <br>
![](/images/2%20Gaussian%20Rest%20type%20and%20Rating%20(M).png)
<br>
3. Relation between Type and Rating <br>
![](/images/3%20Relation%20between%20Type%20and%20Rating%20(M).png)
<br>
4. Votes vs Cost <br>
![](/images/4%20Votes%20vs%20Cost%20(M).png)
<br>
5. Rest Type vs Cost <br>
![](/images/5%20Rest%20Type%20vs%20Cost%20(M).png)
<br>


---
## :chains: Project Structure 

```
zomato-eda-python
    │   README.md
    │       
    ├───images
    │       1 Relation between Location and Rating (M).png
    │       1. Restaurants delivering Online or not.png
    │       10 Rating Distributions.png
    │       11 Top Cuisines.png
    │       2 Gaussian Rest type and Rating (M).png
    │       2 Restaurants allowing table booking or not.png
    │       3 Relation between Type and Rating (M).png
    │       3 Table booking vs Rating.png
    │       4 Best Location.png
    │       4 Votes vs Cost (M).png
    │       5 Rest Type vs Cost (M).png
    │       5 Restaurant Type.png
    │       6 Types of Services.png
    │       7 Cost of Restaurant.png
    │       8 No of Restaurants in a Location.png
    │       9 Most Famous Restaurant Chains in Bengaluru.png
    │
    └───scripts
            zomato_eda.ipynb
```

---






