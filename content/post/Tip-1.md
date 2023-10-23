---
title: "Tip #1 - How to Remove or Automatically Update Links in a Speadsheet"
date: 2021-09-18
draft: false
tags: ["find-links", "tips", "excel", "spreadsheet","excel-tips"]
categories: ["Functions"]
---
My colleagues often wonder how I could solve excel problems in seconds and everything about excel seems so easy for me. The answer is I know some interesting tips that can help me find the problem quickly. Here is one of them.

Suppose you open an excel speadsheet and this message pops up: "This workbook contains links to one or more external sources that could be unsafe."

![alt](/images/links.png)

# 1. Find The Links and Remove Them
You find this message annoying and want to remove all the links in the workbook. Follow below steps to remove them:

**Step 1:** In Home tab, under Editing, click **Find & Select** -> select **Find**. Alternatively, you can just press **Ctrl + F**.

**Step 2:** Type in ".xl" in the **Find what** box. Select within **Workbook** as the following:

![alt](/images/find.png)

Boom! You can now see the link associated with one or more cells in the spreadsheet. Remove them if you want!

# 2. Update Links Automatically

If you want to keep the links but don't want to see the message every time you open the file. You want it to be updated automatically. Here's the tip:

Go to **File** -> **Options** -> **Trust Center** -> **Trust Center Settings...** -> **External Content** -> Under **Security settings for Workbook Links**, select **Enable automatic update for all Workbook Links**

DONE. Easy peasy!

Have fun!
