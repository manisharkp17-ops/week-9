# King County House Price Data Analysis

## 📌 Project Overview
This project focuses on analyzing house price data from King County using Python. It involves data inspection, data preprocessing, feature engineering, outlier detection, and data visualization to understand housing prices and property characteristics.

## 🎯 Objectives
- Explore and understand the house price dataset.
- Check missing values and duplicate records.
- Convert date columns into the correct date format.
- Create new features related to property age and renovation.
- Calculate price per square foot for living area and lot size.
- Detect outliers using the Interquartile Range (IQR) method.
- Visualize outliers using box plots.

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook

## 📂 Dataset
The project uses the `kc_house_data.csv` dataset.

The dataset contains housing information, including:
- `price` – Price of the house
- `date` – Date of sale
- `yr_built` – Year the house was built
- `yr_renovated` – Year the house was renovated
- `sqft_living` – Living area in square feet
- `sqft_lot` – Lot size in square feet

**Note:** The CSV dataset must be available in the correct location before running the notebook.

## ⚙️ Project Workflow

### 1. Import Libraries
Import Pandas, NumPy, Matplotlib, and Seaborn for data analysis and visualization.

### 2. Load the Dataset
Load the CSV file into a Pandas DataFrame.

### 3. Data Inspection
- Display the first and last five rows.
- Check dataset information and column names.
- Generate descriptive statistics.
- Check the dataset shape.
- Identify missing values and duplicate records.

### 4. Date Conversion
Convert the `date` column into a datetime format and extract the sale year into a new column named `sale_year`.

### 5. Feature Engineering
Create new columns to obtain additional information about each property.

- `property_Age` – Calculates property age using the current year and the year built.
- `years_since_renovation` – Calculates the difference between the sale year and renovation year for renovated properties.
- `is_renovated` – Indicates whether a property has been renovated, using 1 for renovated and 0 otherwise.

### 6. Price per Square Foot
Calculate the price per square foot for both living area and lot size.

- `price_per_sqft_living` – House price divided by living area.
- `price_per_sqft_lot` – House price divided by lot size.

Zero values in the area columns are replaced with missing values during division to avoid division-by-zero errors.

### 7. Outlier Detection
Use the Interquartile Range (IQR) method to identify outliers in the price-per-square-foot columns.

The method calculates:
- First Quartile (Q1)
- Third Quartile (Q3)
- Interquartile Range (IQR)
- Lower Bound
- Upper Bound

Values outside the calculated bounds are identified as potential outliers.

### 8. Data Visualization
Create box plots using Seaborn and Matplotlib to visualize potential outliers in:
- Price per square foot of living area
- Price per square foot of lot size

## 📊 Results
The notebook performs exploratory data analysis and creates additional property-related features. It also calculates price-per-square-foot metrics, identifies potential outliers using the IQR method, and visualizes their distributions using box plots.

The actual numerical results depend on the dataset used.

## 🚀 How to Run the Project

1. Download or clone this repository.
2. Open `kc_house.ipynb` in Google Colab or Jupyter Notebook.
3. Upload `kc_house_data.csv` to the appropriate location.
4. Install the required libraries if they are not already available:

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

5. Update the dataset path if necessary.
6. Run the notebook cells in order.
7. Review the analysis results and box plot visualizations.

## 📁 Project Structure

```text
King-County-House-Price-Analysis/
│
├── kc_house.ipynb
├── kc_house_data.csv
└── README.md
```

## 🏁 Conclusion
This project demonstrates how Python libraries can be used to explore housing data, create meaningful features, calculate property price metrics, and detect potential outliers. The analysis provides a foundation for understanding house price data and performing further exploratory data analysis.

## 👩‍💻 Author
BCA Student
