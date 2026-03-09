
# International T20 Cricket Data Analysis

This repository contains a **Jupyter Notebook project** that analyzes **International T20 cricket match data** using Python.  
The notebook performs data cleaning, exploratory analysis, and match statistics extraction from the dataset.

## Project File
- `International_T20_Data.ipynb` – Main notebook containing all analysis and functions.

## Objectives

The notebook performs the following tasks:

1. **Rename Dataset Columns**
   - Clean and rename columns to make them easier to understand.
   - Example:
     - `meta.created` → `created_date`
     - `meta.revision` → `revision_number`

2. **Top Venues Analysis**
   - Identify the **top three venues** that hosted the greatest number of international T20 matches.

3. **Team Rivalry Analysis**
   - Find the **pair of cricket teams that played the highest number of T20 matches against each other**.

4. **Team Performance Analysis**
   - Calculate the **win percentage for each team**.
   - Display the **top five teams with the highest win percentages**.

5. **Match Scorecard Function**
   - Implement a function that generates a **scorecard for each match** using innings data.
   - The function returns:
     - Top **4 batsmen** of each team
     - Top **4 bowlers** of the opponent team

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- AST (for parsing structured data)

## How to Run

1. Clone the repository

```
git clone https://github.com/your-username/your-repository-name.git
```

2. Install dependencies

```
pip install pandas numpy
```

3. Run the notebook

Open the notebook using Jupyter:

```
jupyter notebook
```

Then run:

```
International_T20_Data.ipynb
```

## Learning Outcomes

This project demonstrates:

- Data cleaning and preprocessing
- Sports data analysis using Python
- Working with structured cricket match data
- Writing functions to extract match statistics
