# finance-dataset-analysis

# DA Task: Finance Dataset Analysis using Python

In August 2023, I started the Analytica Camp 8-week Business Analytics course. Unfortunately, the course was cut short due to force majeure from the organizers' side, but I was able to complete a few tasks before it ended.

### Project Overview
This project involves analyzing a finance dataset to derive insights related to profit and revenue across different countries and products. The tasks include:

1. Finding and displaying profit for each country, profit for each product, revenue for each country, and revenue for each product in descending order.
2. Identifying the most profitable product in 2014.
3. Identifying the most profitable country.

### Dataset
The analysis was performed on the provided `Finance_dataset.csv`. The dataset contains information on financial transactions across various countries and products.

### Current Work
As of June 2024, I am continuing my studies in data cleaning and analysis at Turing College, focusing on similar datasets.

## Analysis Tasks

### TASK 1: Profit and Revenue Analysis
### TASK 2: Most Profitable Product in 2014
### TASK 3: Most Profitable Country

#### Description:

### TASK 1:
- Display profit for each country in descending order.
- Display profit for each product in descending order.
- Display revenue for each country in descending order.
- Display revenue for each product in descending order.

### TASK 2:
- Identify the most profitable product in the year 2014.

### TASK 3:
- Identify the most profitable country overall.

#### Code Example:
```python
import pandas as pd

# Load the dataset
df = pd.read_csv('Finance_dataset.csv')

# Data Cleaning
df.dropna(inplace=True)

# TASK 1: Analysis
country_profit = df.groupby('Country')['Profit'].sum().sort_values(ascending=False)
product_profit = df.groupby('Product')['Profit'].sum().sort_values(ascending=False)
country_revenue = df.groupby('Country')['Revenue'].sum().sort_values(ascending=False)
product_revenue = df.groupby('Product')['Revenue'].sum().sort_values(ascending=False)

print("Profit by Country:\n", country_profit)
print("Profit by Product:\n", product_profit)
print("Revenue by Country:\n", country_revenue)
print("Revenue by Product:\n", product_revenue)

# TASK 2: Analysis

# Filter data for the year 2014
df_2014 = df[df['Year'] == 2014]

# Analysis
most_profitable_product_2014 = df_2014.groupby('Product')['Profit'].sum().idxmax()

print("Most Profitable Product in 2014:", most_profitable_product_2014)

# TASK 3: Analysis

# Analysis
most_profitable_country = df.groupby('Country')['Profit'].sum().idxmax()

print("Most Profitable Country:", most_profitable_country)

## Installation and Usage

### Prerequisites
- Python 3.x
- Pandas

### Installation
1. **Clone the repository:**
   - Open Git Bash (or any terminal of your choice).
   - Clone the repository using the following command:
     ```bash
     git clone https://github.com/yourusername/finance-dataset-analysis.git
     cd finance-dataset-analysis
     ```
   - This command will clone the repository `finance-dataset-analysis` from GitHub to your local machine and then navigate into the cloned directory.

2. **Install the required packages:**
   - Once you are inside the project directory (`finance-dataset-analysis`), you need to install pandas.
   - Open Git Bash (or your terminal) and execute the following command:
     ```bash
     pip install pandas
     ```
   - This command installs the pandas library, which is necessary for data manipulation and analysis in your project.

### Running the Analysis

1. **Navigate to the repository directory:**
   - If you haven't already, ensure you are in the `finance-dataset-analysis` directory in Git Bash or your terminal:
     ```bash
     cd finance-dataset-analysis
     ```

2. **Run the Jupyter notebooks for each task:**
   - Open each Jupyter notebook (`Task1.ipynb`, `Task2.ipynb`, `Task3.ipynb`) to perform the data analysis tasks:
     - You can open these notebooks using Jupyter Notebook or Jupyter Lab. Start Jupyter Notebook or Jupyter Lab from the command line:
       ```bash
       jupyter notebook
       # or
       jupyter lab
       ```
     - This will open a new tab in your web browser where you can navigate to and open each notebook (`Task1.ipynb`, `Task2.ipynb`, `Task3.ipynb`).
     - Execute the cells in each notebook to see the analysis results.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please fork the repository and submit a pull request. Here's a general outline of how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/improvement`).
3. Make modifications or fixes.
4. Commit your changes (`git commit -am 'Add feature/improvement'`).
5. Push to the branch (`git push origin feature/improvement`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

Vidmantė Skarakodaitė - (www.linkedin.com/in/vidmantė-skarakodaitė-a6ab27300) - vidmante.skarakodaite@gmail.com

Project Link: [https://github.com/vidmanteska/finance-dataset-analysis](https://github.com/vidmanteska/finance-dataset-analysis)
