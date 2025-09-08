# Student Performance Analysis

## Project Summary

This project conducts an exploratory data analysis (EDA) on the `Student_List.csv` dataset to identify and visualize the key factors influencing student academic performance, as measured by Grade Point Average (GPA). By examining a range of variables—from study habits and parental background to extracurricular involvement—this analysis provides data-driven insights into the drivers of student success.

## Key Questions and Objectives

The primary goal was to answer the following questions through data analysis:

1.  What is the overall academic performance distribution of the students in this dataset?
2.  Is there a correlation between parental education levels and a student's GPA?
3.  Which study-related factors, such as weekly study time and school absences, have the strongest correlation with GPA?
4.  How does participation in extracurricular activities impact academic results?
5.  What is the effect of support systems like parental involvement and private tutoring on student GPA?

## Technical Skills Showcase

This project demonstrates proficiency in fundamental data analysis and visualization skills using Python, primarily with the **Pandas** and **Matplotlib** libraries.

* **Data Loading and Inspection:**
    * Importing and loading CSV data into a Pandas DataFrame using `pd.read_csv()`.
    * Initial data assessment using `.head()`, `.shape`, and `.dtypes` to understand the structure, size, and data types of the dataset.
* **Data Wrangling and Transformation:**
    * Converting categorical data into a numerical format using dictionary mapping and the `.replace()` method to enable quantitative analysis (e.g., transforming `ParentalEducation` levels into an ordinal scale).
* **Exploratory Data Analysis (EDA):**
    * **Aggregation and Grouping:** Employing `.groupby()` and `.agg()` to calculate descriptive statistics (mean, median, count) for different segments of the data.
    * **Filtering and Subsetting:** Creating targeted data subsets based on logical conditions to compare distinct student groups (e.g., students with and without extracurricular involvement).
    * **Statistical Calculation:** Computing value counts and percentages to understand distributions, and calculating the Pearson correlation coefficient with `.corr()` to quantify the linear relationship between variables like absences and GPA.
* **Data Visualization:**
    * Creating a variety of plots with **Matplotlib** to communicate findings effectively:
        * **Pie Chart** (`plt.pie`) to show the proportion of students in each grade category.
        * **Histogram** (`.hist()`) to visualize the distribution of student GPAs.
        * **Scatter Plot** (`plt.scatter`) to investigate the relationship and correlation between two numerical variables.
        * **Boxplot** (`.boxplot()`) to compare GPA distributions across different categorical groups.
        * **Bar Chart** (`.plot.bar()`) to compare aggregated metrics (like mean and median GPA) across categories.
    * Customizing plots with titles, labels (`plt.xlabel`, `plt.ylabel`), and legends for clarity and impact.

## Analysis and Key Findings

### Overall Performance

* The analysis revealed a concerning trend: **51% of students** fall into the 'F' grade category (GPA < 2.0), while only 4% achieve an 'A' grade. This indicates a significant population of underperforming students within this dataset.

### Strongest Performance Predictor

* The most significant discovery was a **strong negative correlation of -0.92** between the number of school absences and GPA. This finding strongly suggests that consistent attendance is the most critical factor for academic success among this group of students.

### Impact of Support Systems

* **Parental Support:** A clear positive relationship exists between the level of parental support and student GPA. Both mean and median GPAs increased consistently as support levels rose from "None" to "Very High."
* **Tutoring:** Students receiving tutoring showed a notably higher average GPA (2.12) compared to those who did not (1.80), confirming the positive effect of supplemental education.

### Surprising Correlations

* **Extracurriculars:** Contrary to common assumptions, students involved in all four measured activities (sports, music, volunteering, and others) had a significantly higher mean GPA (2.45) than those involved in none (1.73).
* **Parental Education:** There was no obvious correlation found between a parent's level of education and their child's GPA, suggesting other factors are more influential.

## Tools and Libraries

* **Python:** Core programming language for the analysis.
* **Pandas:** Used for data manipulation, cleaning, and analysis.
* **Matplotlib:** Utilized for creating all data visualizations.
* **Jupyter Notebook:** The development environment for this analysis.

## Setup and Usage

To replicate this analysis or explore the dataset further, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd your-repository-name
    ```
3.  **Install the required libraries:**
    ```bash
    pip install pandas matplotlib jupyter
    ```
4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
5.  Open the `FIT1043_A1.ipynb` file to view and run the code. Ensure the `Student_List.csv` file is in the same directory.