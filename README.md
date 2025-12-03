# MLBSubplots1
This project analyzes Major League Baseball (MLB) 2019 season at-bat data using Python and Jupyter Notebook. Using Python and a .csv file containing infomration for all the at-bats of the 2019 MLB season, I was able to transform and manipulate the data to breakdown different event types (single, double, home run, etc.) based on what inning they occurred across all of the MLB games for that year. The project demonstrates data cleaning, transformation, and visualization skills by exploring inning-level offensive patterns

##Data Description
Dataset: 2019_atbats.csv (downloaded from Kaggle)
Size: >185,000 at-bats (first 100 rows analyzed for demonstration)
Unnecessary columns were dropped to simplify analysis (e.g., ab_id, g_id, batter_id, pitcher_id)
Key Columns Used:
  inning — inning number
  event — outcome of the at-bat (Single, Double, Walk, Home Run, etc.)

##Data Cleaning & Reprocessing
The dataset was cleaned to focus on offensive events:
  Dropped irrelevant columns
  Standardized all out-type events (Flyout, Lineout, Strikeout, etc.) to "Out"
  Removed all plays where event == "Out"
  Sorted remaining events by inning and event
  Assigned numeric codes to events for plotting purposes (e.g., Single → 4, Home Run → 2)

##Visualizations
1. Multi-Line Chart:
  Displays the frequency of each offensive event across all 9 innings
  Each inning is represented as a separate colored line
  X-axis: Event types, Y-axis: Number of occurrences

2. 3×3 Subplot Grid:
  3×3 layout showing one subplot per inning (1–9)
  Consistent axis scaling for easy comparison
  Each subplot displays event frequencies using different colors and markers
