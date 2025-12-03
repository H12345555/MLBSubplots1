# MLBSubplots1

This project analyzes **Major League Baseball (MLB) 2019 season at-bat data** using Python and Jupyter Notebook. Using a CSV file containing information for all the at-bats of the 2019 MLB season, I transformed and manipulated the data to break down different event types (Single, Double, Home Run, etc.) based on the inning in which they occurred across all MLB games for that year. The project demonstrates **data cleaning, transformation, and visualization skills** by exploring inning-level offensive patterns.

## Dataset and Data Description

- **Dataset:** `2019_atbats.csv` (downloaded from Kaggle)  
- **Size:** >185,000 at-bats  
- **Key Columns Used:**
  - `inning` — inning number  
  - `event` — outcome of the at-bat (Single, Double, Walk, Home Run, etc.)

## Data Cleaning & Preprocessing

The dataset was cleaned to focus on offensive events by performing the following transformations:

- Dropped irrelevant columns (`ab_id`, `g_id`, `batter_id`, `pitcher_id`)  
- Standardized all out-type events (Flyout, Lineout, Strikeout, etc.) to `"Out"`  
- Removed all plays where `event == "Out"`  
- Sorted remaining events by inning and event  
- Assigned numeric codes to events for plotting purposes (e.g., Single = 4, Home Run = 2)  
- Limited analysis to the first 100 events of the season using the `head` function  
- Considered only the first 9 innings of a game (no extra-inning data used)

## Visualizations

### Multi-Line Chart

- Displays the frequency of each offensive event across all 9 innings  
- Each inning is represented as a separate colored line  
- **X-axis:** Event/Outcome  
- **Y-axis:** Number of occurrences for each outcome  

### 3×3 Subplot Grid

- Displays the same information as the multi-line chart, but split across 9 subplots (one per inning)  
- Subplots arranged in a 3×3 layout  
- Each subplot uses different colors and markers to indicate event frequencies  
- **X-axis:** Event/Outcome  
- **Y-axis:** Number of occurrences for each outcome
