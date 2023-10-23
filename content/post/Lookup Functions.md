---
title: "Simple Lookup Functions for Excel and Google Sheets"
date: 2021-06-22
draft: false
tags: ["Vlookup", "spreadsheet", "excel", "GoogleSheet","Dget","Index","Match"]
categories: ["Functions"]
---
**Scenario:** You are assigned to manage 5 items from the purchasing manager. In the systems the company is using, you exported a list of all products they have as well as the data of the stock on hand (SOH), you would like to look for the product names and the stock on hand from the codes given. 

First, download your practice sheet here: https://drive.google.com/drive/folders/1G5aJb4IUIJfac0PBnGZ9gDHB4ku3RT2R?usp=sharing

![alt](/images/gif01.gif)


Here are what you can do on your spreadsheet to look for the information more quickly and effectively:

# 1. The Most Simple Function Vlookup

The descriptions in column B of your spreadsheet is empty, you want to look for their names from the product list. Use **VLOOKUP**!

When typing ```=VLOOKUP``` on _Excel_ or _Google Sheets_, the instructions will appear to help you figure out what kind of data you should put into the function, it looks like this:

_**Excel:**_ 

![alt](/images/img03.png) 
_**Google Sheets:**_

![alt](/images/img05.png)

Note that **VLOOKUP** can only look for the data from left to right, not the opposite. In this case, if you want to look for the description of the products in column B, you can totally use this function to get the names from the product list:

    ```=VLOOKUP(A2,'Product List'!$A$2:$B$10,2,FALSE)```

![alt](/images/img01.jpg)

There you go! You got the descriptions for your assigned products.

# 2. Best Friends Forever Index & Match 

What if your managers gave you only the names, and you want to look for the codes. Remember VLOOKUP can only look for the data from left to right. Now you want to find the information from right to left. What should you do? Use INDEX & MATCH!

![alt](/images/img06.png)

Here is how **INDEX** works:

    ```=INDEX(array, row_num, column_num)```

(1) _array_ is a range where you want to search for the product codes, which is column A in **Product List**
(2) _row_num_ is the row in which it contains the product codes
(3) _column_num_ is the column in which it contains the product codes

What about **MATCH**? It will help you identify exactly which row or column will have the information. 

    ```=MATCH(lookup_value, lookup_array, [match_type])```

(1) _lookup_value_ is the product names in column B of your data          
(2) _lookup_array_ is the products names in the column B of the **Product List**     
(3) _[match_type]_ choose 0 to return exact match


In this case, apply this formula:

    ```=INDEX('Product List'!$A$2:$A$10,MATCH(Purchasing!B11,'Product List'!$B$2:$B$10,0),1)```

![alt](/images/gif02.gif)

DONE. Easy peasy!

Have fun!
