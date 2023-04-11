---
layout: default
title: Using the graph database 
nav_order: 2
parent: Mission editor
grand_parent: Tools
---

# The graph database explained
The graph database is a global key-value database, available for the current `*.logic` file.  
If you are f.e. in the file `build_hq.logic`, every key-value created can be used in that file only.  

It allows creating key-value pairs of type:
- String
- Float
- Int
- Vector

Using this global database, it becomes easy to replace and update values along the whole logic file.

# Using the graph database - example
## Creating new graph database key-value pairs
In the logic file you want to use the graph database, access it using the graph button.  
It's in the top left corner of the node area:  
![](../../../../assets/images/using-the-graph-database_1.png){: width="600px"}  
  
Once the key-value mask opens up, you can create new key-values by clicking  
on the [+] on the right side of the required value type:  
![](../../../../assets/images/using-the-graph-database_2.png){: width="600px"}  

Here you enter the name of the key you are creating, like the name of a variable:  
![](../../../../assets/images/using-the-graph-database_3.png){: width="600px"}  

Once that is done, you fill in an actual value for that key you just created:  
![](../../../../assets/images/using-the-graph-database_4.png){: width="600px"}  

## Using the graph database key-value pairs in nodes
Right-click the node you want to use and select "Edit bindings":  
![](../../../../assets/images/using-the-graph-database_5.png){: width="600px"}  

Select the node binding you want to set and choose your key-value pair:  
![](../../../../assets/images/using-the-graph-database_6.png){: width="600px"}  

When that's done, you can see the changed appearance of the chosen binding:  
![](../../../../assets/images/using-the-graph-database_7.png){: width="600px"}  

Now this node is using your globally set key-value pair.