🎬 Netflix Content Viewership Analysis (Python Project)

This project analyzes the Netflix Titles Dataset (sourced from Kaggle) to uncover insights about Netflix’s content library.
The workflow is structured into three key steps:

Exploring the dataset

Cleaning & preprocessing

Performing analysis to extract meaningful insights

The project was developed in Visual Studio Code using the Jupyter Notebook extension.

📂 Dataset

Source: Netflix Titles Dataset - Kaggle

Entries: 8,807 titles

Features: 12 columns including show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description.

⚙️ Steps Followed
🔹 1. Exploring Dataset

Viewed first and last records with .head() and .tail().

Checked dataset dimensions: (8807, 12).

Inspected data types and null values with .info().

Summary statistics with .describe() for numerical and categorical columns.

Verified no duplicate records.

🔹 2. Cleaning Dataset

Converted date_added column to datetime type.

Split duration into duration_num (numeric) and duration_type (string).

Filled missing values:

director, cast, country → "unknown"

rating, duration_type, date_added → filled using mode

duration_num → filled using mean

Standardized string formatting: converted all text columns to lowercase and stripped extra spaces.

Final cleaned dataset saved as: netflix_cleaned_dataset.csv.

🔹 3. Analysis

Performed analysis using Pandas (grouping, value_counts, exploding lists):

📊 Movies vs TV Shows – Movies dominate (6,131) compared to TV Shows (2,676).

🌍 Top Countries – United States (3,690) & India (1,046).

🌍 Bottom Countries – East Germany & Montenegro with only 1 entry each.

📅 Top Release Years – 2018 (1,147), 2017 (1,032), 2019 (1,030).

📅 Bottom Release Years – 1947, 1959, 1966 (all with 1 entry).

🎥 Top Directors – Rajiv Chilaka (22), Jan Suter (21).

🎭 Top Genres – International Movies (2,752), Dramas (2,427).

🎭 Bottom Genres – Classic & Cult TV (28), TV Shows (16).

📈 Statistical summary of release year:

Average release year ≈ 2014

Standard deviation ≈ 8.2 years

25% before 2013, 50% before 2017, 75% before 2019

The combined analysis was saved in netflix_analysis_csv_file.csv.

📊 Final Insights

🎬 Netflix’s library is movie-heavy compared to TV shows.

🌍 Content production is dominated by the US and India.

⏳ Peak production years: 2017–2019, showing Netflix’s global expansion phase.

📅 The earliest title dates back to 1925, latest in 2021.

📉 Minimal contributions from some countries → opportunity for localized content expansion.

🚀 Tools & Technologies

Python (Pandas, NumPy)

Jupyter Notebook (VS Code Extension)

Matplotlib / Seaborn (for visualizations, optional)
