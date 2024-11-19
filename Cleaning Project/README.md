# **Data Cleaning Project: Airbnb NYC 2019 Dataset**

---

## **Objective**
The objective of this project was to clean and preprocess the Airbnb NYC 2019 dataset to make it suitable for analysis and modeling. Raw datasets often contain missing values, inconsistencies, and formatting issues that hinder accurate analysis. This project focused on resolving these issues to create a clean, structured dataset ready for insights and decision-making.

---

## **Dataset Overview**
The Airbnb NYC 2019 dataset contains 48,895 rows and 16 columns with attributes such as:

- **Host and Listing Information**: `id`, `host_id`, `name`, `host_name`.
- **Location Details**: `neighbourhood_group`, `neighbourhood`, `latitude`, `longitude`.
- **Pricing and Availability**: `price`, `minimum_nights`, `availability_365`.
- **Engagement Metrics**: `number_of_reviews`, `reviews_per_month`, `last_review`.

The dataset provides valuable information about Airbnb listings in New York City but requires preprocessing due to missing values and formatting issues.

---

## **Tools Used**
- **Programming Language**: Python
- **Libraries**:
  - `pandas` for data cleaning and manipulation.
  - `warnings.filterwarnings()` to suppress unnecessary output during operations.

---

## **Steps Undertaken**

### 1. **Data Exploration**
- The dataset was loaded into a pandas DataFrame and inspected using methods like `.head()`, `.info()`, and `.describe()`.
- Missing values were identified using `isna().sum()`:
  - **`reviews_per_month`**: 10,052 missing values.
  - **`last_review`**: Missing entries and improper formatting as an object instead of a date.
- Unique values in categorical columns like `neighbourhood_group` were analyzed, revealing boroughs such as Brooklyn, Manhattan, Queens, Staten Island, and Bronx.

---

### 2. **Handling Missing Values**
#### `last_review`
- Missing values were filled using the **mode** (most frequently occurring date).
- The column was converted to a datetime format using `pd.to_datetime()` for easier manipulation in future analyses.

#### `reviews_per_month`
- Missing values were replaced with the **mean** of the column to preserve numerical consistency.
- This method ensured no rows were dropped unnecessarily while imputing logical values.

### 3. **Final Data Validation**
- A final check using `isna().sum()` confirmed there were no missing values.
- Column types were validated with `.info()`, ensuring the `last_review` column was correctly formatted as a datetime object.
- Unique values in key columns were re-examined to verify no anomalies.

---

## **Results**
- The dataset was cleaned and made ready for analysis:
  - Missing values in `reviews_per_month` were replaced with the column's mean.
  - The `last_review` column was imputed using the mode and converted to a datetime format.
  - No null values remained in the dataset, and all columns were correctly formatted.
- The cleaned dataset maintained its original size of 48,895 rows and became structured for reliable analysis.

---

## **Challenges Faced**
1. **Handling Missing Data**: Imputing values required careful selection of strategies to balance data integrity and statistical accuracy.
2. **Formatting Issues**: Converting `last_review` to a datetime format was challenging but necessary for proper date manipulations.

---

## **Recommendations**
1. **Automate Cleaning Pipelines**: Automating the cleaning process will save time and ensure consistency for similar datasets in the future.
2. **Analyze Imputation Impact**: Evaluate whether imputing values (mean and mode) introduces bias or affects specific analyses.
3. **Add Validation Steps**: Regular validation checks for duplicates, outliers, and invalid entries can further improve data quality.

---

## **Conclusion**
This project demonstrated the importance of data cleaning as the foundation for accurate analysis. By resolving missing values, correcting data types, and ensuring consistency, the Airbnb NYC 2019 dataset was transformed into a reliable format suitable for further exploration and modeling. Clean data is essential for deriving actionable insights and making informed decisions.

---

### **Contact**
Feel free to connect with me for questions or collaboration opportunities:

- **GitHub**: [Your GitHub Profile Link]
- **LinkedIn**: [Your LinkedIn Profile Link]

