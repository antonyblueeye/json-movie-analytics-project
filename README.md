# Wikipedia Movie Data Processing & Analysis (JSON Task)

This repository contains a Python-based data analysis project focused on gathering, cleaning, consolidating, and visualizing movie data extracted from a public Wikipedia repository on GitHub in JSON format. The implementation follows a structured sequence of analysis tasks within a Jupyter Notebook template.

## 📌 Project Objectives & Steps

The notebook sequentially executes the following data engineering and analysis pipeline:

1. **Dynamic URL Generation:** Utilized `numpy.arange` to programmatically build an array of target years (1980s to 2020s) and concatenate them into raw GitHub download URLs.
2. **Data Parsing & Cleaning:** Fetched individual JSON chunks via the `requests` library, flattened the nested records into Pandas DataFrames, dropped unnecessary metadata columns (`href`, `extract`, `thumbnail`, etc.), and discarded incomplete records with missing values using `dropna()`.
3. **Data Integration & Export:** Merged the clean subsets into a unified master dataset consisting of **11,216 rows and 4 core columns** (`title`, `year`, `cast`, `genres`). A local copy was exported to `movies_from_1980_to_2020.csv` to ensure data persistence.
4. **Exploratory Data Analysis (EDA):** Inspected data integrity, column data types, and structural alignment using `.head()` and `.info()` methods.
5. **Genre Frequency Analysis & Visualization:** Extracted the Top 10 most popular movie genres. Generated frequency distributions, a summary table, and visualized the distribution using Bar and Pie charts powered by `matplotlib`.
6. **Cast & Genre In-depth Aggregation:** Performed advanced cross-tabulation (using `pivot_table` and percentage calculations) comparing the top cast members against the primary movie genres.

## 🛠️ Tech Stack & Dependencies

The project relies purely on Python's core Data Science ecosystem:
* **Python 3**
* **Pandas** – For robust data manipulation, schema transformations, and table aggregations.
* **NumPy** – For sequential indexing and vector operations.
* **Matplotlib.pyplot** – For rendering interactive and static distribution plots.
* **Requests** – For retrieving remote JSON payloads over HTTP.

## 📊 Summary of Insights (Top 10 Genres)

Based on the processed historical data spanning over four decades, the final breakdown highlights the dominant genres:

| Rank | Genre | Movie Count |
| :---: | :--- | :---: |
| 1 | Comedy | 3,995 |
| 2 | Drama | 3,801 |
| 3 | Action | 1,537 |
| 4 | Thriller | 1,430 |
| 5 | Horror | 1,186 |
| 6 | Romance | 1,113 |
| 7 | Science Fiction | 781 |
| 8 | Crime | 741 |
| 9 | Fantasy | 580 |
| 10 | Animated | 558 |

*(Detailed visualization charts and relative cross-tables with cast performance are fully rendered inside the notebook cells).*

## 🚀 How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
   cd your-repo-name
