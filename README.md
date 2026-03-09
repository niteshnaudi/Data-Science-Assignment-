# Data-Science-Assignment-1
<b>👉 <a href="https://colab.research.google.com/drive/1WZXf1zzifgluccmjyTCMR2RVcaxA3rWN?usp=sharing">Click Here to view the full assignment in Google Colab</a></b>
# T20 Cricket Match Analytics: ICC Data Science Assignment

> **Academic Details:**
> * **Student Name:** Suraj Chauhan
> * **Roll Number / ID:** 2472040
> * **Program Name:** BSc. (Hons) Computer Science
> * **School / Department:** School of Technology
> * **University Name:** Doon University
> * **Submitted To:** Mr. Kamal Rawal
> * **Academic Year:** 2025-2026

---

## 📌 Project Overview
This project is part of a Data Science assignment simulating a role within the International Cricket Council's (ICC) Analytics Team. The objective is to perform exploratory data analysis (EDA), data cleaning, complex data extraction, and visualization on a dataset comprising 1417 International T20 cricket matches. 

The ultimate goal of this assignment was to transition from basic data manipulation to building a fully functional, TV-broadcast-style scorecard generator using deeply nested ball-by-ball data, and to present key insights visually.

## 📊 Dataset Details
* **Source:** International T20 Cricket Data (Cricsheet format).
* **Size:** 1417 rows (matches) and multiple columns.
* **Key Features:** The dataset contains standard match metadata (venues, teams, toss decisions, winners) as well as a highly complex `innings` column containing stringified dictionaries representing every single legal and illegal delivery bowled in a match.

## 🛠️ Tools & Libraries Used
* **Python 3**
* **Pandas:** For data manipulation, aggregation, and formatting.
* **NumPy:** For numerical operations.
* **Ast (Abstract Syntax Trees):** Specifically `ast.literal_eval`, used to safely parse stringified lists and dictionaries into native Python objects.
* **IPython.display:** For rendering aesthetically pleasing DataFrames in Google Colab.
* **Matplotlib & Seaborn:** For creating professional-grade data visualizations to uncover match trends.

## 🚀 Tasks Accomplished

1. **Data Sanity Checks & Exploration:**
   * Checked the dataset's shape, data types, and non-null counts.
   * Identified and managed missing values and duplicate records to ensure data integrity.

2. **Data Cleaning (Column Renaming):**
   * Automatically stripped redundant prefixes (`meta.` and `info.`) from all column names using Regex.
   * Standardized column names (e.g., `info.venue` to `venue`, `meta.created` to `created_date`) for easier querying.

3. **Matchup & Venue Analytics:**
   * Identified the top venues that hosted the highest number of T20 matches.
   * Engineered a new column using Python tuples to correctly identify the most frequent team matchup regardless of the "Team 1 vs Team 2" column order.

4. **Performance Metrics:**
   * Calculated the exact Win Percentage for all teams (Matches Won / Matches Played * 100), handling edge cases like "No Result" matches.
   * Extracted and displayed the Top 5 performing teams.

5. **Data Visualization:**
   * **Venue Analysis:** Generated a horizontal bar chart to showcase the Top 10 venues globally.
   * **Team Dominance:** Plotted a vertical bar chart comparing the Win Percentages of the Top 10 teams.
   * **Toss Insights:** Created a pie chart analyzing the strategic distribution of toss decisions (Bat vs. Field).

6. **Advanced Feature Engineering (The Scorecard Function):**
   * Built a custom Python function `get_scorecard()` that parses deeply nested JSON-like strings.
   * **Batting Stats:** Calculated total runs and balls faced (excluding wides) for individual batsmen, extracting the Top 4 scorers.
   * **Bowling Stats:** Calculated wickets (excluding run outs), total runs conceded (excluding byes/leg-byes), and converted legal deliveries into standard cricket overs (e.g., 20 balls = 3.2 overs).
   * Formatted the final output to perfectly mimic the Side-by-Side TV Broadcast graphic (Top 4 Batsmen vs Top 4 Bowlers).

## 💻 How to Run the Code
1. Open the provided Jupyter Notebook via the Google Colab link at the top of this page.
2. Ensure the dataset `International_T20_Data.csv` is uploaded to the root directory of your Colab session.
3. Run the cells sequentially from top to bottom. 
4. The final cell contains the execution block for the `get_scorecard()` function, which will output the formatted innings tables for the first match in the dataset.

## 🧠 Key Learnings & Challenges
The biggest challenge in this dataset was handling the `innings` and `teams` columns. Because the data was exported to a CSV, Python lists and dictionaries were converted into raw text strings. Learning how to use `ast.literal_eval` to safely reconstruct these data structures was a major breakthrough. Additionally, coding the precise logic for cricket metrics—such as ensuring a "wide" doesn't count as a ball faced for a batsman, or calculating overs using modulo math—was a great exercise in translating real-world domain rules into Python code.
