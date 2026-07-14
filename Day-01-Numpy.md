#  Day 01 – NumPy Fundamentals

** Date:** 14 July 2026

---

#  Goal of Today's Learning

Today's objective was to build a strong foundation in **NumPy**, the core Python library for numerical computing and data analysis. I focused on understanding how NumPy arrays work, how they differ from Python lists, and how to efficiently perform array operations without using loops.

---

#  Topics Covered

## 1. Introduction to NumPy
- What is NumPy?
- Why NumPy is used in Data Science
- Advantages of NumPy over Python Lists
- Installing and Importing NumPy

---

## 2. Array Creation
- Creating arrays using `np.array()`
- Creating arrays with `np.arange()`
- Creating arrays with `np.linspace()`
- Creating arrays using `np.zeros()`
- Creating arrays using `np.ones()`

---

## 3. Array Attributes
- Shape of an array (`shape`)
- Number of dimensions (`ndim`)
- Size of an array (`size`)
- Data type (`dtype`)

---

## 4. Indexing and Slicing
### 1D Arrays
- Indexing
- Negative Indexing
- Slicing

### 2D Arrays
- Row Indexing
- Column Indexing
- Row & Column Slicing

---

## 5. Mathematical & Vectorized Operations
- Addition
- Subtraction
- Multiplication
- Division
- Modulus
- Power
- Vectorized Calculations

---

## 6. Reshaping Arrays
- `reshape()`
- Converting 1D → 2D
- Converting 2D → 3D
- Converting arrays into one dimension

---

## 7. Flattening Arrays
- `flatten()`
- `ravel()`
- Difference between View and Copy

---

## 8. Copying Arrays
- Shallow Copy
- Deep Copy

---

## 9. Boolean Indexing
- Filtering Data
- Masking
- Multiple Conditions
- `np.where()`

---

## 10. Statistical Functions
- `sum()`
- `mean()`
- `max()`
- `min()`
- `argmax()`

---

## 11. Random Module
- Random Integers
- Random Float Numbers
- Random Choice
- Random Seed
- Normal Distribution

---

## 12. Sorting
- `sort()`
- `argsort()`

---

## 13. Unique Values
- `unique()`
- `return_counts=True`

---

## 14. Practice Questions
Solved practice questions related to:
- Array Creation
- Indexing
- Slicing
- Reshaping
- Filtering
- Sorting
- Random Numbers
- Statistical Functions
- Unique Values

---

#  Functions Practiced

```python
np.array()
np.arange()
np.linspace()
np.zeros()
np.ones()
np.shape
np.ndim
np.size
np.dtype

reshape()
flatten()
ravel()
copy()

sum()
mean()
max()
min()
argmax()

sort()
argsort()

unique()

where()

random.randint()
random.rand()
random.choice()
random.seed()
random.normal()
```

---

#  Concepts I Understood Today

- NumPy arrays are much faster and more memory-efficient than Python lists.
- Vectorized operations allow mathematical calculations without writing loops.
- Reshaping changes only the structure of an array while keeping the same data.
- `flatten()` creates a new copy of the array, whereas `ravel()` usually returns a view of the original array.
- Boolean indexing makes filtering data simple and efficient.
- `axis=0` performs operations column-wise, while `axis=1` performs operations row-wise.
- `argsort()` returns the indices that would sort an array instead of the sorted values themselves.
- Using `seed()` makes random number generation reproducible, which is useful for experiments.

---

#  Key Learnings

Today I learned that NumPy is designed to perform numerical computations efficiently. Instead of using loops, NumPy allows operations on entire arrays at once, making programs faster and easier to write. I also understood that many data science libraries such as Pandas, Scikit-learn, TensorFlow, and PyTorch are built on top of NumPy, making it an essential foundation for future learning.

---

#  Challenges Faced

- Initially, I was confused between `axis=0` and `axis=1`.
- Understanding the difference between `flatten()` and `ravel()` required practical examples.
- It took some practice to understand Boolean indexing and filtering.
- Reshaping arrays requires that the total number of elements remains the same.

---

#  How I Solved Them

- Practiced multiple examples for each concept.
- Drew diagrams to understand rows, columns, and axes.
- Solved indexing and slicing exercises.
- Compared outputs of `flatten()` and `ravel()` by modifying arrays.
- Read the NumPy documentation and experimented with examples.

---

#  Practical Skills Gained

After today's learning, I can now:

- Create NumPy arrays efficiently.
- Access and modify elements using indexing and slicing.
- Perform mathematical operations without loops.
- Filter data using Boolean conditions.
- Reshape arrays into different dimensions.
- Generate random datasets.
- Sort arrays and retrieve sorted indices.
- Find unique values and count their occurrences.
- Apply basic statistical functions to datasets.

---

#  Reflection

Today's session strengthened my understanding of how NumPy simplifies numerical computations. Before learning NumPy, I relied on Python lists for storing and processing data. After practicing NumPy, I realized how much more efficient and readable array operations become through vectorization.

The most interesting concept for me was Boolean indexing because it allows filtering data with simple conditions instead of writing multiple loops and `if` statements.

I also understood that writing small practice programs after each concept helps reinforce learning much better than only reading theory.

Overall, today's learning has given me confidence to work with arrays and has prepared me for the next stage of data analysis using Pandas.

---

#  Progress

- ✅ Python Fundamentals
- ✅ Data Structures
- ✅ NumPy Basics
- ✅ NumPy Intermediate Concepts

**Overall Progress in NumPy:** **~80% Completed**

---

#  Next Learning Goals

- Array Concatenation
- Array Splitting
- Broadcasting
- Universal Functions (Ufuncs)
- Matrix Operations
- Linear Algebra Basics
- File Handling using NumPy

---

#  Resources Used

- Official NumPy Documentation
- Training Notes
- Practice Programs
- Self-written Exercises

---

##  Daily Summary

Today I completed the major fundamentals of NumPy, including array creation, indexing, slicing, reshaping, vectorized operations, filtering, sorting, random number generation, and statistical analysis. Through hands-on coding and practice questions, I gained confidence in using NumPy for numerical computations and data manipulation. This knowledge forms a strong foundation for learning **Pandas** and performing real-world data analysis.