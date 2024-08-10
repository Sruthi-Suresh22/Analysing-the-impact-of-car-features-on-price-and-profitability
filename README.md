# ANALYSING THE IMPACT OF CAR FEATURES ON PRICE AND PROFITABILITY

### Table of Contents

- [Project Description](#project-description)
- [Dataset Details](#dataset-details)
- [Data Understanding](#data-understanding)
- [Data Cleaning](#data-cleaning)
- [Tasks for Analysis](#tasks-for-analysis)
- [Dashboard Tasks](#dashboard-tasks)
- [Dashboard](#dashboard)
- [Conclusion](#conclusion)

### Project Description

- The automotive industry has been rapidly evolving over the past few decades, with a growing focus on fuel efficiency, environmental sustainability, and technological innovation. 
- As a Data Analyst, we have to find solution for **‘How can a car manufacturer optimize pricing and product development decisions to maximize profitability while meeting consumer demand?’**
- This problem could be approached by analyzing **the relationship between a car's features, market category,** and **pricing**, and identifying which features and categories are **most popular among consumers** and **most profitable for the manufacturer**.
- By using data analysis techniques such as **regression analysis** and **market segmentation**, the manufacturer could develop a pricing strategy that balances consumer demand with profitability, and identify which product features to focus on in future product development efforts.

### Dataset Details

- The dataset contains information on various car models and their specifications, and is titled “Car Features and MSRP’’.
- Number of observations: 11,914
- Number of variables: 16
- File type: CSV (Comma Separated Values)
- The variables in the dataset are:
  - Make: the make or brand of the car
  - Model: the specific model of the car
  - Year: the year the car was released
  - Engine Fuel Type: the type of fuel used by the car (gasoline, diesel, etc.)
  - Engine HP: the horsepower of the car's engine
  - Engine Cylinders: the number of cylinders in the car's engine
  - Transmission Type: the type of transmission (automatic or manual)
  - Driven_Wheels: the type of wheels driven by the car (front, rear, all)
  - Number of Doors: the number of doors the car has
  - Market Category: the market category the car belongs to (Luxury, Performance, etc.)
  - Vehicle Size: the size of the car
  - Vehicle Style: the style of the car (Sedan, Coupe, etc.)
  - Highway MPG: the estimated miles per gallon the car gets on the highway
  - City MPG: the estimated miles per gallon the car gets in the city
  - Popularity: a ranking of the popularity of the car (based on the number of times it has been viewed on Edmunds.com)
  - MSRP: the manufacturer's suggested retail price of the car

### Data Understanding

- Out of 16 columns the dataset contained, 4 columns had blank / null values.
![image](https://github.com/user-attachments/assets/bb3317e6-6732-44ac-9565-79a9084293ff)
![image](https://github.com/user-attachments/assets/80eadcfe-7e34-4c37-b6ca-1bf0f9eb552a)
- Regarding the Duplicate records, there were 715 records which were detected as duplicates.
- Outliers for every numeric columns were detected using Box plot.
![image](https://github.com/user-attachments/assets/e6ee8ac4-b833-4f54-9ef5-e8f71b5f4a5e)
![image](https://github.com/user-attachments/assets/a937ecef-2343-4fbd-8826-ae517bc415a3)
![image](https://github.com/user-attachments/assets/381b77f9-a5d5-4c99-a8f6-eba9962550cc)
![image](https://github.com/user-attachments/assets/50b920a0-b092-409d-b902-57934af02a14)
![image](https://github.com/user-attachments/assets/86dddac8-a2c1-4784-98e7-25a04f2c5f05)
![image](https://github.com/user-attachments/assets/e5b03f23-f63f-4fab-8312-18dbe9be5224)
![image](https://github.com/user-attachments/assets/cab50944-9ab5-4a43-904d-1205644f754e)
![image](https://github.com/user-attachments/assets/1814366b-77b5-415a-8d9b-1cd00bc8a6f2)

### Data Cleaning

- **Handling Blank / NULL values** : The missing values were handled using MODE and MEDIAN Imputation.
- **Duplicate records** : The 715 records which were detected as duplicates were removed.
- **Handling Outliers** : The outlier in Highway MPG which was at extreme end as it was a petrol car with MPG as 354 which is not possible. This was replaced with correct value after manual check on Internet. Other outliers were retained as such.

Therefore, the remaining number of records for Analysis : 11,199

### Tasks for Analysis

**TASK 1: How does the popularity of a car model vary across different market categories?**
- Crossovers are the highest selling cars followed by Flex Fuel and Luxury. Highest average popularity is topped by ‘Flex Fuel, Diesel’, ‘Hatchback, Flex Fuel’ and ‘Crossover, Flex Fuel, Performance’. 
![image](https://github.com/user-attachments/assets/4ada72ac-90f1-42ad-a56a-f774845b35bb)

**TASK 2: What is the relationship between a car's engine power and its price?**
- Car’s Engine Power and it’s Price follows a positive linear relation indicating that as the Horse power increases the price of the car also increases.
![image](https://github.com/user-attachments/assets/8b4642e6-c8ee-447a-800a-ba8efbf4b7db)

**TASK 3: Which car features are most important in determining a car's price?**
- Feature’s that positively affect the Car Price : Engine Cylinder & Transmission Type
- Feature’s that negatively affect the Car price : Vehicle size, Engine Fuel Type, Number of doors. 
![image](https://github.com/user-attachments/assets/f0b1d74e-3271-4561-83e1-b1e6a36f2a54)

**TASK 4: How does the average price of a car vary across different manufacturers?**
- Bugatti, Maybach, Rolls-Royce, Lamborghini has the highest average price whereas Plymouth, Oldsmobile, Suzuki has the least average price.
![image](https://github.com/user-attachments/assets/dfb25e68-0c72-43d0-9ba6-5eac60c868d9)

**TASK 5: What is the relationship between fuel efficiency and the number of cylinders in a car's engine?**
- Engine Cylinders and Average Highway MPG follows a negative trendline indicating that as the number of Engine cylinders increases the average highway MPG decreases.
![image](https://github.com/user-attachments/assets/0ecf321b-410d-464f-806e-526dea696799)

### Dashboard Tasks

**TASK 1: How does the distribution of car prices vary by brand and body style?**
- Chevrolet make with the vehicle style 4dr SUV contribute more to the Car Price while Genesis contribute less to the Car Price. 
![image](https://github.com/user-attachments/assets/a55153aa-061f-4881-868e-203766c7a246)

**TASK 2: Which car brands have the highest and lowest average MSRPs, and how does this vary by body style?**
- Bugatti make with the vehicle style Coupe has the Highest average MSRPs while Plymouth has the lowest average MSRPs. 
![image](https://github.com/user-attachments/assets/60aece97-3477-42bf-acea-6d9fbe30c974)

**TASK 3: How do the different feature such as transmission type affect the MSRP, and how does this vary by body style?**
- Automatic and Manual Transmission type are contributing more to the Average MSRPs.
![image](https://github.com/user-attachments/assets/52df62e5-c284-4620-9c29-b8814a155de7)

**TASK 4: How does the fuel efficiency of cars vary across different body styles and model years?**
![image](https://github.com/user-attachments/assets/21f7fcf5-49f7-4080-81ae-e87fd067ff6f)

**TASK 5: How does the car's horsepower, MPG, and price vary across different Brands?**
![image](https://github.com/user-attachments/assets/696628f8-c53a-4c44-9eca-89a7a7ad71de)

### Dashboard
![image](https://github.com/user-attachments/assets/ed02ecec-d4b5-461c-a0ef-32de19bbc85d)

### Conclusion
This project emphasizes the importance of data analytics in making informed decisions within in the automotive industry. The insights gained from analyzing tasks such as exploring trends in car features and pricing over time, comparing the fuel efficiency of different types of cars, investigating the relationship between a car's features and its popularity, predicting the price of a car based on its features and market category will help the industry in taking inform decisions related to product development, marketing, and pricing.



