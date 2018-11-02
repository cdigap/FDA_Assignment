# Fundamentals of Data Analysis Assignment
The assignment concerns the well-known Anscombe’s quartet dataset. We are required to create a Jupyter notebook analysing the dataset. There are four distinct tasks to be carried out in your Jupyter notebook.

1. Explain the background to the dataset – who created it, when it was created, and any speculation you can find regarding how it might have been created.
2. Plot the interesting aspects of the dataset.
3. Calculate the descriptive statistics of the variables in the dataset.
4. Explain why the dataset is interesting, referring to the plots and statistics above.

# Anscombe’s quartet dataset

## Analysis

Anscombe’s quartet dataset was contructed in 1973 by the statistician Francis Anscombe. This is an interesting set of data which clearly provides a useful caution against applying individual statistical methods to data without graphing them. The dataset shows the effects of outliers on Statistical properties. This data set has identical Statiscal properties but has a totally different view when graphed, this article described the difference among the statisticians that"numerical calculations are exact, but graphs are rough."[1] 

Anscombe's quartet is a set of four datasets with each dataset consisting of eleven x, y data points.

Unnamed: 0	x1	x2	x3	x4	y1	y2	y3	y4

0	1	10	10	10	8	8.04	9.14	7.46	6.58

1	2	8	8	8	8	6.95	8.14	6.77	5.76

2	3	13	13	13	8	7.58	8.74	12.74	7.71

3	4	9	9	9	8	8.81	8.77	7.11	8.84

4	5	11	11	11	8	8.33	9.26	7.81	8.47

5	6	14	14	14	8	9.96	8.10	8.84	7.04

6	7	6	6	6	8	7.24	6.13	6.08	5.25

7	8	4	4	4	19	4.26	3.10	5.39	12.50

8	9	12	12	12	8	10.84	9.13	8.15	5.56

9	10	7	7	7	8	4.82	7.26	6.42	7.91

10	11	5	5	5	8	5.68	4.74	5.73	6.89

## Dataset Plots

# Plotting the data to help understand the data better.

data_file.plot(kind='scatter',x="x1", y="y1")

sns.regplot(data_file['x1'],data_file['y1'])

data_file.plot(kind='scatter',x="x2", y="y2")

sns.regplot(data_file['x2'],data_file['y2'])

data_file.plot(kind='scatter',x="x3", y="y3")

sns.regplot(data_file['x3'],data_file['y3'])

data_file.plot(kind='scatter',x="x4", y="y4")

sns.regplot(data_file['x4'],data_file['y4'])


From the above graphs we can clearly see that each dataset we can see that each one is different and doesnot have the same features. They are correspond to different perspective.

## Descriptive Statistics

# Describe funtion is going to give us the usual statistical numbers as shown below.
df = data_file.describe()
df

Unnamed: 0	x1	x2	x3	x4	y1	y2	y3	y4

count	11.000000	11.000000	11.000000	11.000000	11.000000	11.000000	11.000000	11.000000	11.000000

mean	6.000000	9.000000	9.000000	9.000000	9.000000	7.500909	7.500909	7.500000	7.500909

std	3.316625	3.316625	3.316625	3.316625	3.316625	2.031568	2.031657	2.030424	2.030579

min	1.000000	4.000000	4.000000	4.000000	8.000000	4.260000	3.100000	5.390000	5.250000

25%	3.500000	6.500000	6.500000	6.500000	8.000000	6.315000	6.695000	6.250000	6.170000

50%	6.000000	9.000000	9.000000	9.000000	8.000000	7.580000	8.140000	7.110000	7.040000

75%	8.500000	11.500000	11.500000	11.500000	8.000000	8.570000	8.950000	7.980000	8.190000

max	11.000000	14.000000	14.000000	14.000000	19.000000	10.840000	9.260000	12.740000	12.500000

## Inference

From the above table you can notice that the Count, Mean , Std are almost in the same, this is a different view of data.

Even though statistical measures are same but the data is different.

So with this we understand that we need to be sensible and should have circumstantial analysis and visualization.

Always plot your data to better understand before making any conclusions.

## References 
1. https://en.wikipedia.org/wiki/Anscombe%27s_quartet, Anscombe, F. J. (1973). "Graphs in Statistical Analysis". American Statistician. 27 (1): 17–21. doi:10.1080/00031305.1973.10478966. JSTOR 2682899.
2. https://vincentarelbundock.github.io/Rdatasets/csv/datasets/anscombe.csv
