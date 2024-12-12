
# Shop&Go Superstore-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

This dashboard helps the manager of Shop&Go Superstore to analyze  Profit, Sales, Discount, and other paramters they made from the year 2016 to 2019. As we can see the total sales made by the store in those year is (2.31M) with a profit of (286.40K).

Over a period of four year highest profit is made in the Technology category despite (being lowest in quantity) and lowest in furniture. In terms of profit by region, Central region has lowest profit. So they can focus on furniture and Central region to significantly increase profit.

In 2017 sales has decreased (470.53K) and in the year 2019 has highest sales of (733.21K).


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a excel file. The excel file had multiple sheets but we choose Orders sheet.
- Step 2 : As we can see the data can be viewed in Report View, Table View, Model View and DAX query view, we can choose Report View for visualizations. On the right side of Model View there is Data Pane and Visualizations Pane. We made different visuals selecting tiles form the visualizations pane and populating the tile by drag and drop approach or directly selecting data from the Data Pane.
- Step 3 : Under the Home tab > Visualizations > Canvas Background a light yellow color was chosen. A title " Shop&Go Superstore-Dashboard" was given taking a text box.
- Step 4 : To determine the Sum of Profit by Category, donut chart tile was taken and 'Sum of Profit' was passed in the value field and 'Category' in the Legend field.

Snap of Sum of Profit by Category,
![Screenshot 2024-12-01 124512](https://github.com/user-attachments/assets/0b6eb4dc-6b43-4305-b8ae-401e40587728)

In the above diagram, Technology is the highest profit making category with a total (145.454K) which is 50.79% of the total profit. Meanwile Office Supplies (42.77%) is the second highest profit making category and Furniture is least profit making Category.

- Step 5 : For calculating Sum of Profit by Region, we created a donut chart as above passing Sum of Profit and Region in the field section of donut tile.

Snap of Sum of Profit by Region,
![Screenshot 2024-12-01 125417](https://github.com/user-attachments/assets/085e7b44-8e31-4615-a0f2-0d01b0e100b6)

In the figure above, Western Region is making highest profit (37.68%), which is followed by Eastern Region (31.96%) followed by Southern and Central Region with (16.32%) and (13.86%) respectively.


- Step 6 :To represent the Sum of Quantity by Category, we took pie-chart tile form the visualizations pane and filled the Category in the Legend field and Sum og Quantity in the values field.

- Step 7 : Three card visuals were added to the canvas, first one represent Sum of Profit (2.31M), second one represent Sum of Sales (286.4K) and last one represent Sum of Discount (1.56K). 

- Step 8 : We created a Stacked bar chart to know the sum of Quantity vs Segment of products.

Snap: ![Screenshot 2024-12-02 130352](https://github.com/user-attachments/assets/5aec4592-a81b-4680-b684-4a64f088faa3)

Above is the Stacked bar chart of Segment vs Sum of Quantity. Consumer is the top segment with a total quantity of around 19K which is followed by Corporate(11K) and Home Office(6K)
- Step 9 : The one representing Sum of Quantity by Ship Mode, insights us about the Quantity of Products that are shiped through Different Class of Cargo. Standard Class ranked top with (60.19%) of quantity which is followed by Second Class (19.6%). 

Snap: 
![Screenshot 2024-12-12 113608](https://github.com/user-attachments/assets/1708dc95-2317-4b08-a8db-c67bbe59d8b6)

- Step 10 : The next is we created a clustured column chart, showing Sum of Profit by Ship Mode. Highest profit is made from the Standard Class(164K) which is followed by Second Class and First Class. The lowest profit by shiping mode is Same Day (15K), which means shiping done on the same day makes lowest profit.

- Step 11 : For quick review of Sales, Profti and Discount we created three card visuals. They are as shown in the figure below.

Snap: 
![Screenshot 2024-12-12 121417](https://github.com/user-attachments/assets/c559648d-3752-487c-855f-20247576ca94)
- Step 13 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 
- Step 14 : Calculated column was created in which, customers were grouped into various age groups.

for creating new column following DAX expression was written;
       
        Age Group = 
        
        if(airline_passenger_satisfaction[Age]<=25, "0-25 (25 included)",
        
        if(airline_passenger_satisfaction[Age]<=50, "25-50 (50 included)",
        
        if(airline_passenger_satisfaction[Age]<=75, "50-75 (75 included)",
        
        "75-100 (100 included)")))
        
Snap of new calculated column ,

![Snap_1](https://user-images.githubusercontent.com/102996550/174089602-ab834a6b-62ce-4b62-8922-a1d241ec240e.jpg)

        
- Step 15 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(airline_passenger_satisfaction[ID])
        
A card visual was used to represent count of customers.

![Snap_Count](https://user-images.githubusercontent.com/102996550/174090154-424dc1a4-3ff7-41f8-9617-17a2fb205825.jpg)

        
 - Step 16 : New measure was created to find  % of customers,
 
 Following DAX expression was written to find % of customers,
 
         % Customers = (DIVIDE(airline_passenger_satisfaction[Count of Customers], 129880)*100)
 
 A card visual was used to represent this perecntage.
 
 Snap of % of customers who preferred business class
 
 ![Snap_Percentage](https://user-images.githubusercontent.com/102996550/174090653-da02feb4-4775-4a95-affb-a211ca985d07.jpg)

 
 - Step 17 : New measure was created to calculate total distance travelled by flights & a card visual was used to represent total distance.
 
 Following DAX expression was written to find total distance,
 
         Total Distance Travelled = SUM(airline_passenger_satisfaction[Flight Distance])
    
 A card visual was used to represent this total distance.
 
 
 ![Snap_3](https://user-images.githubusercontent.com/102996550/174091618-bf770d6c-34c6-44d4-9f5e-49583a6d5f68.jpg)
 
 - Step 18 : The report was then published to Power BI Service.
 
 
![Publish_Message](https://user-images.githubusercontent.com/102996550/174094520-3a845196-97e6-4d44-8760-34a64abc3e77.jpg)

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://user-images.githubusercontent.com/102996550/174096257-11f1aae5-203d-44fc-bfca-25d37faf3237.jpg)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://user-images.githubusercontent.com/102996550/174074051-4f08287a-0568-4fdf-8ac9-6762e0d8fa94.jpg)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.
# Airlines-Dashboard.md.txt
Displaying # Airlines-Dashboard.md.txt.

