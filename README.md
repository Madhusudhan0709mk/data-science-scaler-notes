# data-science-scaler-notes

<h1>Data Science Introduction</h1>
Data Science is a combination of multiple disciplines that uses statistics, data analysis, and machine learning to analyze data and to extract knowledge and insights from it.

<h1>What is Data Science?</h1>
Data Science is about data gathering, analysis and decision-making.

Data Science is about finding patterns in data, through analysis, and make future predictions.

By using Data Science, companies are able to make:

Better decisions (should we choose A or B)
Predictive analysis (what will happen next?)
Pattern discoveries (find pattern, or maybe hidden information in the data)
Where is Data Science Needed?
Data Science is used in many industries in the world today, e.g. banking, consultancy, healthcare, and manufacturing.

<h1>Examples of where Data Science is needed:</h1>

For route planning: To discover the best routes to ship
To foresee delays for flight/ship/train etc. (through predictive analysis)
To create promotional offers
To find the best suited time to deliver goods
To forecast the next years revenue for a company
To analyze health benefit of training
To predict who will win elections
Data Science can be applied in nearly every part of a business where data is available. Examples are:

Consumer goods
Stock markets
Industry
Politics
Logistic companies
E-commerce

<h1>Skills of Data Scientist Work?</h1>
A Data Scientist requires expertise in several backgrounds:

Machine Learning
Statistics
Programming (Python or R)
Mathematics
Databases
A Data Scientist must find patterns within the data. Before he/she can find the patterns, he/she must organize the data in a standard format.

<h1>Here is how a Data Scientist works:</h1>

Ask the right questions - To understand the business problem.
Explore and collect data - From database, web logs, customer feedback, etc.
Extract the data - Transform the data to a standardized format.
Clean the data - Remove erroneous values from the data.
Find and replace missing values - Check for missing values and replace them with a suitable value (e.g. an average value).
Normalize data - Scale the values in a practical range (e.g. 140 cm is smaller than 1,8 m. However, the number 140 is larger than 1,8. - so scaling is important).
Analyze data, find patterns and make future predictions.
Represent the result - Present the result with useful insights in a way the "company" can understand.

<h1>What is Numpy </h1>
the numby is built on c programming ,numpy is the basic of the all data science libraries ,numpy only performed on the numbers not on text type data

<h4> What is vectors</h4>
lists are called vectors or 1-D arrary is a vectors
EX: [1,5,6,9,4,3]

<h4> What is matrix</h4>
2-D array is a matrix
vectors are called matrix
or lists of list  are called matrix
Ex: [[1,5,3,6,6,9],[5,6,4,1,38,8,8]]

not to use on non numerical data example : store cart item names
numby only used with numbers numpy not work on gpu

demo code :

```
import numpy as np
list = [1,2,5,6,3,5]
num = np.array(list)
print(len(num.shape))
```

o/p: 1

1. One dimensional array creating
Create a 1-D array containing the values 1,2,3,4,5:

```
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

o/p: is
[1 2 3 4 5]

2. two dimensional array creating

 ```
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr)
```

o/p is:
[[1 2 3]
 [4 5 6]]

HOW SHAPE IS CALCULATED?
for above shape o/p is (2,3) where the 2 is the inner in list 3 is the 3 number inside each list

3.Create a 3-D array with two 2-D arrays

```
import numpy as np
arr = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])
print(arr)
```

o/p is:
[[[1 2 3]
  [4 5 6]]

 [[1 2 3]
  [4 5 6]]]


<h1> DATA TYPES IN NUMPY <h2>

# Data Types in NumPy
i - integer
b - boolean
u - unsigned integer
f - float
c - complex float
m - timedelta
M - datetime
O - object
S - string
U - unicode string
V - fixed chunk of memory for other type ( void )

```
import numpy as np
arr = np.array([1, 2, 3, 4])
print(arr.dtype)
```
o/p : int64

1. create array from normal to string type

```
import numpy as np
arr = np.array([1,2,3],dtype='S')
print(arr) #o/p is [b'1' b'2' b'3']
print(arr.dtype) #o/p is S1
```

2. converting data type of existing array of decimals to integer

```
import numpy as np
arr = np.array([1.1, 2.1, 3.1])
newarr = arr.astype('i')
print(newarr)
print(newarr.dtype)
```
o/p is
[1 2 3]
int64

<p>other parameter to use</p>
newarr = arr.astype(int)
newarr = arr.astype(bool)

<h4>dirrent typr of creating arrays</h4>

```
np1 = np.array([0,1,2,3,5,5])
print(np1.shape) o/p: 6
```
create the array of n number like for loop using arange

```
np2 = np.arange(10)
print(np2)
```
o/p is [0,1,2,3,4,5,6,7,8,9]

```
np2 = np.arange(0,10,2)
print(np2)
```

o/p is [0,2,4,6,8]

```
np2 = np.zeros(10)
print(np2)
```
o/p is [0,0,0,0,0,0,0,0,0,0]

```
np2 = np.full((3),5)
print(np2)
```
o/p is [5,5,5]

The creation of multidimensionall array

```
np2 = np.full((2,3),5)
print(np2)
```
o/p is 
[[5,5,5]
,[5,5,5]]



# slicing numpy array
```
import numpy as np
np1 = np.array([1,2,4])
print(np1[1:3])
```
o/p:[2,4]

<h1>NUMPY array copy and view</h1>
The Difference Between Copy and View
The main difference between a copy and a view of an array is that the copy is a new array, and the view is just a view of the original array.

The copy owns the data and any changes made to the copy will not affect original array, and any changes made to the original array will not affect the copy.

The view does not own the data and any changes made to the view will affect the original array, and any changes made to the original array will affect the view.


