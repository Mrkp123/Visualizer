 
# Pandas Analyzer & Data Visualization

A menu-driven Python application for sales data analysis, data manipulation, statistical computation, and visualization. This project integrates **Pandas, NumPy, Matplotlib, and Seaborn** with Object-Oriented Programming (OOP) principles to provide an interactive data analysis toolkit.

## 🚀 Features

### 1. Load Dataset
- Load sales data from CSV files.
- Automatically detect missing or invalid file paths.
- Generate a synthetic sales dataset when the requested file does not exist.
- Convert the `Date` column into datetime format.
- Display dataset dimensions and column names.

### 2. Explore Data
Explore the loaded dataset through:
- Displaying the first five rows using `head()`.
- Displaying the last five rows using `tail()`.
- Viewing column names.
- Checking column data types.
- Displaying dataset information using `info()`.
- Viewing dataset shape, memory usage, and numeric columns.

### 3. Handle Missing Data
Manage missing values using different techniques:
- Display rows containing missing values.
- Fill missing numeric values with column means.
- Drop rows containing missing values.
- Replace missing values with a user-defined value.

### 4. Mathematical Operations
Perform element-wise calculations on DataFrame columns.

**Supported operations:**
- Addition (`+`)
- Subtraction (`-`)
- Multiplication (`*`)
- Division (`/`)

Operations can be performed between:
- Two numeric columns.
- A numeric column and a scalar value.

Results are stored as new columns in the DataFrame.

### 5. NumPy Array Operations
Convert numeric DataFrame columns into NumPy arrays and perform:
- Array indexing.
- Array slicing.
- Element-wise arithmetic with scalar values.
- Element-wise arithmetic between two columns.
- Array concatenation.
- Array splitting using `np.array_split()`.
- Summary statistics using NumPy.

### 6. Combine DataFrames
Combine the current dataset with another DataFrame using:
- **Concatenation:** Stack rows using `pd.concat()`.
- **Merge:** Combine datasets using a common key with `pd.merge()`.
- **Join:** Combine DataFrames using their indexes with `DataFrame.join()`.

Supports inner, left, right, and outer join operations.

### 7. Split DataFrame
Split datasets into smaller groups using:
- Region.
- Product.
- Year extracted from the `Date` column.
- A specified number of equal chunks.

### 8. Search, Sort, and Filter
Perform data exploration through:
- Case-insensitive text search within a selected column.
- Sorting records in ascending or descending order.
- Filtering numeric rows using comparison operators.
- Filtering records within a specified date range.

Supported comparison operators:

| Operator | Description |
|---|---|
| `>` | Greater than |
| `<` | Less than |
| `==` | Equal to |
| `!=` | Not equal to |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

### 9. Aggregating Functions
Calculate aggregate values for selected numeric columns:
- Sum
- Mean
- Count
- Minimum
- Maximum
- Median
- Standard deviation

Also supports:
- Multiple aggregations.
- Group-wise aggregation using categorical columns.

### 10. Descriptive Statistics
Generate statistical summaries using Pandas:
- `describe()` summary.
- Standard deviation.
- Variance.
- Percentiles and quantiles.
- Correlation matrix.

### 11. Pivot Tables
Create interactive pivot tables by selecting:
- Index column.
- Columns column.
- Numeric values column.
- Aggregation function.

Supported aggregation functions:
- Sum
- Mean
- Count
- Minimum
- Maximum

### 12. Data Visualization

Generate different types of visualizations using Matplotlib and Seaborn.

| Visualization | Library | Purpose |
|---|---|---|
| Bar Plot | Matplotlib | Compare aggregated values across categories |
| Line Plot | Matplotlib | Display trends |
| Scatter Plot | Matplotlib | Explore relationships between numeric variables |
| Pie Chart | Matplotlib | Show category distributions |
| Histogram | Matplotlib | Understand numeric distributions |
| Stack Plot | Matplotlib | Compare cumulative numeric values |
| Heatmap | Seaborn | Visualize correlations |
| Box Plot | Seaborn | Examine numeric distributions by category |
| Subplots Dashboard | Matplotlib | Display multiple plots together |

### 13. Save Visualization
- Save the most recently generated plot.
- Automatically add the `.png` extension when no extension is supplied.
- Save plots at 300 DPI for high-quality output.
- Automatically create the destination directory when required.

## 🛠️ Technologies Used

- **Python 3** – Core programming language.
- **Pandas** – Data manipulation and analysis.
- **NumPy** – Numerical operations and array processing.
- **Matplotlib** – Data visualization and plotting.
- **Seaborn** – Statistical visualization.

## 📦 Python Libraries and Important Functions

| Library | Functions / Methods |
|---|---|
| Pandas | `read_csv()`, `DataFrame()`, `head()`, `tail()`, `info()`, `describe()` |
| Pandas | `groupby()`, `merge()`, `concat()`, `pivot_table()`, `join()` |
| Pandas | `fillna()`, `dropna()`, `sort_values()`, `to_datetime()` |
| NumPy | `array()`, `arange()`, `concatenate()`, `array_split()` |
| NumPy | `greater()`, `less()`, `equal()`, `corrcoef()` |
| NumPy | `nansum()`, `nanmean()`, `nanmedian()`, `nanstd()` |
| Matplotlib | `subplots()`, `bar()`, `plot()`, `scatter()`, `pie()`, `hist()` |
| Seaborn | `set_theme()`, `heatmap()`, `boxplot()` |

## 🧠 Object-Oriented Programming Concepts

The project uses a `SalesDataAnalyzer` class to organize and manage data analysis operations.

- **Class and Object:** Encapsulates the complete analysis toolkit inside the `SalesDataAnalyzer` class.
- **Constructor (`__init__`):** Initializes the dataset, file path, and visualization attributes.
- **Destructor (`__del__`):** Attempts to release Matplotlib resources when the object is destroyed.
- **Encapsulation:** Uses private helper methods prefixed with `_` to organize internal operations.
- **Class Method (`@classmethod`):** Tracks the total number of created analyzer objects using `get_instance_count()`.
- **Static Methods (`@staticmethod`):** Provides reusable utilities such as `dataframe_info()` and `create_sample_dataset()`.
- **Class Attributes:** Stores instance counts and operation mappings.
- **Instance Methods:** Handle loading, cleaning, analyzing, combining, and visualizing data.

## 📂 Project Structure

```text
Pandas-Analyzer-Data-Visualization/
│
├── main.py
├── data/
│   └── sales_data.csv
│
└── README.md
```

**Note:** The `data/sales_data.csv` file can be generated automatically by the application when a requested dataset path does not exist and the user agrees to create a synthetic dataset.

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Pandas-Analyzer-Data-Visualization.git
```

### 2. Navigate to the Project Directory

```bash
cd Pandas-Analyzer-Data-Visualization
```

### 3. Install Required Libraries

```bash
pip install numpy pandas matplotlib seaborn
```

### 4. Run the Application

```bash
python main.py
```

## 📋 Main Menu

After running the program, the following menu is displayed:

```text
=======================================================
      Data Analysis & Visualization Program
=======================================================
Please select an option:
1. Load Dataset
2. Explore Data
3. Perform DataFrame Operations
4. Handle Missing Data
5. Generate Descriptive Statistics
6. Data Visualization
7. Save Visualization
8. Exit
=======================================================
```

Load a CSV dataset first, then select the required analysis or visualization option.

## 📊 Sample Dataset

The application can generate a synthetic sales dataset containing the following columns:

| Column | Description |
|---|---|
| `SalesID` | Unique sales record identifier |
| `Date` | Sales transaction date |
| `Product` | Product category |
| `Region` | Sales region |
| `Units` | Number of units sold |
| `UnitPrice` | Price per unit |
| `Sales` | Total sales amount |
| `Profit` | Profit amount |

The default sample generator creates 200 records and intentionally inserts some missing values to demonstrate data-cleaning techniques.

## 🎯 Learning Objectives

This project helps practice:

- Reading and processing CSV datasets.
- DataFrame creation and manipulation.
- Data cleaning and missing-value handling.
- NumPy array conversion and operations.
- DataFrame merging, joining, concatenation, and splitting.
- Searching, sorting, and filtering records.
- Group-wise aggregation and pivot tables.
- Descriptive and statistical analysis.
- Data visualization with Matplotlib and Seaborn.
- Saving generated charts.
- Applying OOP concepts to a practical data analysis application.
- Handling invalid inputs and runtime errors.

## 🔮 Future Improvements

- Add interactive dashboards using Streamlit.
- Export cleaned datasets and analysis results to CSV or Excel.
- Add more advanced statistical tests.
- Implement automated report generation.
- Add additional visualization types.
- Introduce automated unit testing.
- Improve date and numeric input validation.

## 👨‍💻 Author

**Your Name**

GitHub: [Your GitHub Profile](https://github.com/your-username)

## 📄 License

This project is available for educational and learning purposes. You are welcome to explore, modify, and improve it.
