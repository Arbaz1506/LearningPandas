# Learning Pandas

This repository contains a comprehensive collection of Jupyter notebooks organized by topics, designed for learning and practicing Pandas programming concepts from basics to advanced levels.

## 📁 Notebook Structure

The repository is structured into numbered notebooks, each focusing on a specific Pandas topic. Follow the notebooks in numerical order for a logical learning progression:

### 1. Pandas1.ipynb - Fundamentals
Introduction to Pandas and DataFrame basics:

- Pandas overview and advantages over traditional data handling
- Series and DataFrame creation methods
- DataFrame properties (shape, dtypes, columns, index)
- Reading data from CSV files
- DataFrame inspection and info methods
- Displaying and summarizing DataFrames
- Basic data types in Pandas

### 2. Pandas2.ipynb - Data Inspection & Selection
Data selection, filtering, and accessing techniques:

- Accessing columns and rows (loc, iloc, at, iat)
- Boolean indexing and filtering
- Selecting subsets of data
- Working with conditional selections
- Index manipulation
- Renaming columns and indices
- Handling different column types

### 3. Pandas3.ipynb - Data Cleaning & Preprocessing
Essential data cleaning techniques:

- Handling missing values (dropna, fillna, interpolate)
- Data type conversions
- Removing duplicates
- String operations on columns
- Data validation and quality checks
- Standardizing and normalizing data
- Handling outliers

### 4. Pandas4.ipynb - Data Aggregation & Grouping
Grouping and summarizing data:

- GroupBy operations and aggregations
- Multiple aggregation functions
- Group statistics (mean, sum, count, min, max)
- Custom aggregation functions
- Pivot tables and cross-tabulations
- Apply functions to groups
- Hierarchical grouping

### 5. Pandas5.ipynb - Merging & Joining DataFrames
Combining multiple DataFrames:

- Merge operations (inner, outer, left, right)
- Join operations
- Concatenating DataFrames
- Working with multiple keys
- Handling duplicate columns
- Set operations on DataFrames
- Combining by index and columns

### 6. Pandas6.ipynb - Working with Time Series Data
Time-based data operations:

- DateTime operations and parsing
- Time series indexing
- Resampling and frequency conversion
- Rolling windows and moving averages
- Time-based grouping and aggregation
- Handling timezone information
- Date range generation

### 7. Pandas7.ipynb - Advanced Data Manipulation
Complex transformation techniques:

- MultiIndex DataFrames
- Stacking and unstacking data
- Melting and pivoting
- Window functions
- Custom transformations
- Memory optimization techniques
- Performance tips for large datasets

### 8. Pandas8.ipynb - Statistical Analysis
Statistical operations and analysis:

- Descriptive statistics
- Correlation and covariance analysis
- Distribution analysis
- Statistical tests basics
- Data profiling
- Outlier detection methods
- Summary statistics by groups

### 9. Pandas9.ipynb - Real-World Data Projects
Practical projects combining all concepts:

- End-to-end data analysis workflows
- Real-world dataset exploration
- Data wrangling and preparation
- Exploratory Data Analysis (EDA)
- Data visualization with Pandas
- Combining multiple data sources
- Building analytical pipelines

## 📊 Datasets

The repository includes sample datasets for practice:

- **anime.csv** - Anime dataset with ratings, genres, and metadata
  - Useful for practicing grouping, filtering, and aggregation
  
- **Countries.csv** - Country data for practicing joins and merges
  - Perfect for learning merge and join operations

## 🚀 Getting Started

**Prerequisites:** Ensure you have Python 3.8 or higher installed on your system.

### Clone the Repository:
```bash
git clone https://github.com/Arbaz1506/LearningPandas.git
cd LearningPandas
```

### Install Required Packages:
```bash
pip install pandas numpy jupyter openpyxl
```

### Navigate to Notebooks:
Start with Pandas1.ipynb and progress sequentially.

### Run Notebooks:
Launch Jupyter and open the notebooks:
```bash
jupyter notebook
```

## 📖 Learning Path

For optimal learning, follow this sequence:

1. **Start with Fundamentals** (Pandas1.ipynb) - Learn Series and DataFrame creation
2. **Master Data Selection** (Pandas2.ipynb) - Understand indexing and filtering
3. **Clean Your Data** (Pandas3.ipynb) - Handle missing values and preprocessing
4. **Group and Aggregate** (Pandas4.ipynb) - Summarize and analyze data
5. **Merge Datasets** (Pandas5.ipynb) - Combine multiple data sources
6. **Explore Time Series** (Pandas6.ipynb) - Work with temporal data
7. **Advanced Manipulation** (Pandas7.ipynb) - Complex transformations
8. **Analyze Statistically** (Pandas8.ipynb) - Statistical operations
9. **Build Projects** (Pandas9.ipynb) - Real-world applications

## ✨ Key Features

Each notebook includes:

- Well-commented code demonstrating core concepts
- Executable cells with immediate output feedback
- Practical examples using real-world datasets
- Step-by-step explanations of Pandas functions
- Performance comparisons and best practices
- Common pitfalls and how to avoid them
- Visualization examples with matplotlib

## 💡 Practical Examples

### Creating a DataFrame
```python
import pandas as pd

data = {'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 35],
        'Score': [85, 90, 88]}
df = pd.DataFrame(data)
```

### Filtering Data
```python
# Filter rows where Age > 25
filtered_df = df[df['Age'] > 25]

# Multiple conditions
result = df[(df['Age'] > 25) & (df['Score'] >= 90)]
```

### GroupBy Operations
```python
# Group by column and calculate mean
grouped = df.groupby('Category')['Score'].mean()

# Multiple aggregations
agg_result = df.groupby('Category').agg({
    'Score': ['mean', 'max', 'count'],
    'Age': 'mean'
})
```

### Merging DataFrames
```python
df1 = pd.DataFrame({'key': ['A', 'B'], 'value1': [1, 2]})
df2 = pd.DataFrame({'key': ['A', 'B'], 'value2': [3, 4]})

# Inner merge
merged = pd.merge(df1, df2, on='key')
```

### Handling Missing Values
```python
# Drop rows with missing values
df.dropna()

# Fill missing values
df.fillna(0)
df.fillna(method='ffill')  # Forward fill
```

## 🛠️ Technologies

- **Pandas** - Data manipulation and analysis library
- **NumPy** - Numerical computing foundation
- **Jupyter** - Interactive notebook environment
- **Python** - Programming language

## ⚡ Performance Considerations

Key insights for optimal Pandas usage:

- Vectorized operations are significantly faster than loops
- Use appropriate data types to reduce memory usage
- GroupBy operations are more efficient than manual iteration
- Merge operations have different performance based on key types
- Use copy() when creating independent copies of data
- Avoid chained indexing; use loc/iloc for clarity
- Consider chunking large datasets for memory efficiency

## 📚 Additional Resources

- [Pandas Official Documentation](https://pandas.pydata.org/docs/)
- [Pandas Cheat Sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)
- [10-minute Pandas Tutorial](https://pandas.pydata.org/getting_started/intro_tutorials/index.html)

## 🤝 Contributing

Contributions are welcome! Please:

- Add new examples or improve existing ones
- Follow the notebook structure and naming conventions
- Ensure code is well-commented and readable
- Test your code before submitting
- Suggest improvements to existing materials

## 📄 License

This project is open-source and free for educational purposes. You are welcome to use and modify the code according to the MIT License.

## 👤 Author

Created by **Arbaz Salam** ([@Arbaz1506](https://github.com/Arbaz1506))

**Last Updated:** February 2026

---

**Happy Learning!** 📊 Start with Pandas1.ipynb and progress through the notebooks to master Pandas data manipulation skills.
