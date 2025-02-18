# My Learning with Pandas Library

## Introduction

In this project, I used the **Pandas library** to work with a dataset containing information about students, including their names, class, score, gender, and whether they passed or not. The goal was to clean, analyze, and derive insights from the data using various **Pandas library** functions. 

To start, I used some basic **Pandas library** functions to understand the data:

- **`head()`**: Displayed the first few rows to get a quick look at the dataset.
- **`info()`**: Provided details about the dataset, including the data types and any missing values.
- **`describe()`**: Gave summary statistics of the numerical columns to understand the distribution of the data.
- **`shape()`**: Helped me understand how many rows and columns the dataset had.

These basic functions helped me better understand the structure of the dataset and the distribution of values.

## Dataset Overview


The dataset is about students in different classes and their grades.
![Screen Shot 2025-02-18 at 18 42 47](https://github.com/user-attachments/assets/d507d6a5-263a-4ddb-b237-602e6f2494ba)


## Functions Used

Here’s a list of the functions I used and examples of how they were applied. You can add screenshots of the full formulas for each function.

1. **Loading Data**: 
    - **`read_csv()`** – Used to load the dataset into a DataFrame.
    - Example: 
      ```python
      import pandas as pd
      df = pd.read_csv('students.csv')
      ```

2. **Understanding the Data**: 
    - **`head()`** – Displayed the first few rows of the dataset to get a quick preview.
      ```python
      df.head()
      ```
    - **`info()`** – Provided a summary of the dataset’s structure.
      ```python
      df.info()
      ```
    - **`describe()`** – Gave summary statistics for the numeric columns.
      ```python
      df.describe()
      ```
    - **`shape()`** – Displayed the number of rows and columns in the dataset.
      ```python
      df.shape
     

3. **Dropping Columns**:
    - **`drop()`** – Dropped the 'passed' column from the dataset.
      ```python
      df = df.drop('passed', axis=1)
      ```
    

4. **Renaming Columns**:
    - **`rename()`** – Renamed the 'mark' column to 'score'.
      ```python
      df = df.rename(columns={'mark': 'score'})
      ```
  

5. **Aggregating Data**:
    - **`groupby()` and `agg()`** – Grouped the data by class and calculated the average score.
      ```python
      df.groupby('class').agg({'mark': 'mean'})
      ```
    - *[Insert screenshot of full formula]*

6. **Filtering Data**:
    - **`df[df['gender'] == 'female']`** – Filtered data to focus on female students.
      ```python
      df[df['gender'] == 'female']
      ```
    - *[Insert screenshot of full formula]*

7. **Sorting Data**:
    - **`sort_values()`** – Sorted the data by score in descending order to find top performers.
      ```python
      df.sort_values(by='mark', ascending=False)
      ```
    

8. **Summing and Averaging Data**:
    - **`sum()`** – Calculated the total score in the dataset.
      ```python
      df['score'].sum()
      ```
    - **`mean()`** – Calculated the average score in the dataset.
      ```python
      df['mark'].mean()
      ```
    

9. **Ranking Data**:
    - **`rank()`** – Ranked the students based on their score, with the highest score first.
      ```python
      df['score'].rank(ascending=False)
      ```


## Findings from the Dataset

By using these functions, I was able to uncover several insights from the dataset:

1. **Average Score by Class**:
    - I grouped the data by class and calculated the average score using `groupby()` and `agg()`. This helped me see which class had the highest average score.
    

2. **Top-Performing Students**:
    - I used `sort_values()` to find the top-performing students by sorting the data by score in descending order.
      

3. **Gender Distribution**:
    - I filtered the data to analyze female students using `df[df['gender'] == 'female']`. This helped me see the gender distribution in the dataset.
    - ![Screen Shot 2025-02-18 at 18 46 23](https://github.com/user-attachments/assets/22027eb3-79a8-4c63-a071-bdfca9464990)


4. **Passing Students**:
    - By using the 'passed' column, I was able to determine how many students passed and how many failed the exam.
    - *[Insert screenshot of pass/fail analysis]*

5. **Total and Average Scores**:
    - I calculated the total score using `sum()` and the average score using `mean()`, which gave me an overall understanding of the students’ performance.
    - 
![Screen Shot 2025-02-18 at 18 47 45](https://github.com/user-attachments/assets/e57c24f5-3a49-4e11-bb98-39ef0896a128)

## Conclusion

Using the **Pandas library**, I was able to effectively clean, manipulate, and analyze the student dataset. With these functions, I gained valuable insights into the students' scores, gender distribution, and pass/fail rates. I’m confident that these techniques will be useful for analyzing similar datasets in the future. 

For a more detailed exploration of the **Pandas library** and how these functions were applied to the dataset, please refer to the attached file where I go deeper into each step and show additional examples.

