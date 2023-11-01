# Data Cleaning: Sports Car Prices

Source: https://www.kaggle.com/datasets/rkiattisak/sports-car-prices-dataset/

For this project, data with focused metrics in car make, price, speed was accessed and cleaned exclusively through excel with insights and visualizations gathered through pivot tables.

Conclusion: Based on this spread, it looks like there are relatively fewer manufacturers creating sports cars within the "entry level to mid level" budget category vs sports cars that are considered "luxury". Beyond this, it does seem like the general trend lends itself to faster cars generally being more expensive specifically within that metric of 0-60mph time. 

## Step 1:
Duplicates were removed through the native Excel function Data > Remove Duplicates, including blank entries.

## Step 2: 
An IFS statement was then used to partition prices by brackets defined by the following: 
```
=IFS(H2<50000, "Entry Level",  H2<80000, "Mid-Level", H2>=80000, "Luxury")
```

## Step 3: 
Pivot tables were then created looking at price by 0-60mph time and price by car make. I partly wanted to see if there was any association related to 0-60mph speed, which in turn could be suggestive of relative torque, to price. Additionally, small consistency changes were made, such as changing the denomination of average price to whole numbers, and refining the list of values for seconds under 0-60mph as some values didn't quite fit. 

## Step 4: 
Small dashboard was created with graphs derived from the pivot tables established earlier. 
