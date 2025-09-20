# PROGRAMMING-ASSIGNMENT-4---DATA-WRANGLING-AND-DATA-VISUALIZATION
deadline: September 25, 2025

<br>

## Table of Contents
1. Objectives
2. Programming Assignment 4.1
3. Programming Assignment 4.2
4. Author

<br>

## I. Objectives
1. To identify the codes and functions needed in cleaning and visualizing data 
2. To be able to apply and use the different codes and functions in creating a Python program that will be used in data wrangling and data visualization

<br>

## II. Programming Assignment 4.1
``Instruction ``
Create the following data frames based on the format provided: 

#### (a) Filename: Instru = [“Name”, “GEAS”, “Electronics >70”]; where track is constant as Instrumentation and hometown Luzon

##### Entire Code:
```python
import pandas as pd 

raw_a = pd.read_excel("board2.xlsx") 
Instru = raw_a.loc [(raw_a["Track"]=='Instrumentation') 
                 & (raw_a["Hometown"]=='Luzon') 
                 & (raw_a["Electronics"]>70), 
                 ['Name', 'GEAS', 'Electronics']].reset_index(drop = True) 
Instru
```
##### Step-by-step Thought Process.
1. awdawdawda
```python
import pandas as pd 
```
2. awdawdawda
```python
raw_a = pd.read_excel("board2.xlsx") 
```
3. awdawdawda
```python
Instru = raw_a.loc [(raw_a["Track"]=='Instrumentation') 
                 & (raw_a["Hometown"]=='Luzon') 
                 & (raw_a["Electronics"]>70), 
                 ['Name', 'GEAS', 'Electronics']].reset_index(drop = True) 
```
4. dwdad
```python
Instru
```

<br>

#### (b) Filename: Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; where hometown is constant as Mindanao and gender Female 

##### Entire Code:
```python
```

<br>

## II. Programming Assignment 4.2
``Instruction``
Create a visualization that shows how the different features contributes to average grade. Does chosen track in college, gender, or hometown contributes to a higher average score? 

##### Entire Code for calculations:
```python
import pandas as pd 

raw2 = pd.read_excel("board2.xlsx") 
raw2['Average'] = raw2[['Math','Electronics','GEAS','Communication']].mean(axis=1) 


Avg_Track = raw2.groupby("Track")["Average"].mean() 
Avg_Gender = raw2.groupby("Gender")["Average"].mean() 
Avg_Hometown = raw2.groupby("Hometown")["Average"].mean() 

Avg_Track_df = raw2.groupby("Track")["Average"].mean().reset_index() 
Avg_Gender_df = raw2.groupby("Gender")["Average"].mean().reset_index() 
Avg_Hometown_df = raw2.groupby("Hometown")["Average"].mean().reset_index() 
```

##### Entire Code for data visualization graph 1:
Graph 1: Average Grades by Track
```python
import matplotlib.pyplot as plt

Avg_Track.plot(kind="bar", color="Yellow", title="Average Grade by track", ylabel="Average Grade", xlabel="Track")
plt.show()
```

###### Output graph 1:

##### Entire Code for data visualization graph 2:
Graph 2: Average Grades by Gender
```python
import matplotlib.pyplot as ply

Avg_Gender.plot(kind="bar", color="pink", title = "Average Grade by Gender", ylabel="Average Grade", xlabel="Gender")
plt.show()
```

###### Output graph 2: 

##### Entire Code for data visualization graph 3:
Graph 3: Average Grades by Hometown
```python
import matplotlib.pyplot as ply

Avg_Hometown.plot(kind="bar", color="blue", title="Average Grade by Hometown", ylabel="Average Grade", xlabel="Hometown")
plt.show()
```

###### Output graph 3:

<br>

##### Step-by-step Thought Process.
1. awdawd
```python
import pandas as pd 
```
2. awdawd
```python
raw2 = pd.read_excel("board2.xlsx") 
raw2['Average'] = raw2[['Math','Electronics','GEAS','Communication']].mean(axis=1) 
```
3. dwada
```python
Avg_Track = raw2.groupby("Track")["Average"].mean() 
Avg_Gender = raw2.groupby("Gender")["Average"].mean() 
Avg_Hometown = raw2.groupby("Hometown")["Average"].mean() 
```
4. asdwa
```python
Avg_Track_df = raw2.groupby("Track")["Average"].mean().reset_index() 
Avg_Gender_df = raw2.groupby("Gender")["Average"].mean().reset_index() 
Avg_Hometown_df = raw2.groupby("Hometown")["Average"].mean().reset_index() 
```
5. asdwa
```python
import matplotlib.pyplot as plt

Avg_Track.plot(kind="bar", color="Yellow", title="Average Grade by track", ylabel="Average Grade", xlabel="Track")
plt.show()
```
5. asdwa
```python
import matplotlib.pyplot as ply

Avg_Gender.plot(kind="bar", color="pink", title = "Average Grade by Gender", ylabel="Average Grade", xlabel="Gender")
plt.show()
```
6. dawda
```python
import matplotlib.pyplot as ply

Avg_Hometown.plot(kind="bar", color="blue", title="Average Grade by Hometown", ylabel="Average Grade", xlabel="Hometown")
plt.show()
```
8. dwada
```python

```
9. dwada
```python

```
10. dwada
```python

```







