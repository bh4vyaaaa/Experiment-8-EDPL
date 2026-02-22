#Experiment – 8
Bhavya Pandya
25070123139
E&TC A1
##Title :Tools For Exploratory Data Analysis - NumPy

##Aim : To study and implement the NumPy library in Python and perform various numerical, multidimensional, and statistical operations for Exploratory Data Analysis.

##Objectives :
To understand the architectural concept of N-dimensional arrays (ndarrays)
To explore memory management and contiguous storage in numerical computing
To perform advanced array creation and property inspection
To apply mathematical, vectorized, and broadcasting operations
To understand the difference between array views and deep copies
To apply statistical methods and linear algebra for data insights
Theory on NumPy :
NumPy (Numerical Python) is the foundational package for scientific computing in Python. It provides a powerful N-dimensional array object, sophisticated broadcasting functions, and tools for integrating C/C++ and Fortran code. At its core is the ndarray, which encapsulates n-dimensional arrays of homogeneous data types.

The Architecture of ndarray :
Unlike Python lists, which are arrays of pointers to objects (leading to fragmented memory), NumPy arrays are stored in a contiguous block of memory. This means all elements are stored right next to each other. This architecture allows the CPU to access elements much faster through a process called "pointer arithmetic."

###Characteristics of NumPy :
Vectorization: This is the practice of replacing explicit loops with array expressions. Vectorized code is more concise and runs much faster because the loops occur in C instead of Python.
Homogeneity: Every element must be of the same data type (dtype). This uniformity allows NumPy to predict exactly how much memory each element occupies.
Striding: This describes how NumPy moves through the memory block. A "stride" is the number of bytes to skip in memory to reach the next element in a specific dimension.
Broadcasting: This allows NumPy to treat arrays with different shapes during arithmetic operations. It "stretches" the smaller array across the larger one without actually creating multiple copies of the data in memory.
Axis and Rank: In NumPy, dimensions are called axes. The number of axes is the rank. For example, a 2D array has 2 axes: axis 0 (rows) and axis 1 (columns).
Deep Dive into Core Operations :
1. Memory Management: Views vs. Copies
A critical aspect of NumPy is that slicing an array creates a view rather than a copy. This means the slice shares the same memory as the original array. If you modify the view, the original array changes. This is highly memory-efficient when working with gigabytes of data, but requires the use of the .copy() method when independent arrays are needed.

2. Universal Functions (ufuncs) :
A ufunc is a function that operates on ndarrays in an element-by-element fashion. They support array broadcasting, type casting, and several other standard features. Common ufuncs include np.add, np.sin, and np.exp. These are significantly faster than applying Python's math library functions to array elements via a loop.

3. Advanced Indexing :
NumPy supports "Fancy Indexing," which involves passing an array of indices to access multiple array elements at once. It also supports Boolean Indexing, where you can use a mask (an array of True/False values) to filter data. For example, data[data > 0] would return only the positive values from an array.

NumPy in the Data Science Ecosystem :
NumPy is not just a standalone library; it is the "engine" for the entire Python data science stack:

Pandas: Built directly on top of NumPy; a DataFrame is essentially a collection of NumPy arrays with labels.
Scikit-learn: Uses NumPy arrays for all input and output data in machine learning models.
Matplotlib: Requires NumPy arrays to plot coordinates and pixel data for visualizations.
SciPy: Extends NumPy by adding a collection of algorithms for optimization, integration, and statistics.
Applications of NumPy in EDA :
Dimensionality Reduction: Using Linear Algebra (like SVD or PCA) to simplify complex datasets.
Noise Filtering: Using Fourier Transforms to remove noise from signals or images.
Data Transformation: Normalizing or scaling numerical features (e.g., Min-Max scaling) to prepare data for algorithms.
Simulation: Generating large sets of random data following specific distributions (Normal, Binomial, Poisson) for hypothesis testing.

###Conclusion:-
NumPy is the backbone of numerical computing in Python. By providing efficient memory management through contiguous blocks and performance boosts through vectorization, it overcomes the inherent slowness of standard Python loops. Its ability to handle complex multidimensional structures with simple syntax makes it an indispensable tool for any data scientist or engineer performing exploratory data analysis.
