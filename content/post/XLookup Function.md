---
title: "Forget VLookup if You're Using Office 365"
date: 2021-10-16
draft: false
tags: ["Xlookup", "spreadsheet", "excel", "Filter"]
categories: ["Functions"]
---
If you're currently using Office 365, then relying on VLookup is a waste of time :D


Because XLookup will become your best friend forever. Here's how it works:

    ```=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])```

***Note that the arguments in square brackets are optional***

As you may know, VLookup can only look for the data from left to right, not the oposite. With XLookup, you can do both ways. Let's go straight to an example:

**Look for the name of the products with the given product codes below**

![alt](/images/XLookup1.png) 

Suppose this is the master database you have:

![alt](/images/XLookup2.png) 

Here's the formula at **B2** (first image): 

    ```=XLOOKUP(A2,'Master Database'!$A:$A,'Master Database'!$B:$B)```

If the product code is not in the master database and you want to leave it blank, then do this:

    ```=XLOOKUP(A2,'Master Database'!$A:$A,'Master Database'!$B:$B,"")```

![alt](/images/XLookup.gif) 

Have fun!
