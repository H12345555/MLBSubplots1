# MLBSubplots1

This project analyzes **Major League Baseball (MLB) 2019 season at-bat data** using Python and Jupyter Notebook. Using a CSV file containing information for all the at-bats of the 2019 MLB season, I was able to transform and manipulate the data to break down different event types (Single, Double, Home Run, etc.) based on what inning they occurred across all MLB games for that year. The project demonstrates **data cleaning, transformation, and visualization skills** by exploring inning-level offensive patterns.


## Dataset and Data Description
- **Dataset:** "2019_atbats.csv" (downloaded from Kaggle)  
- **Size:** >185,000 at-bats (first 100 rows analyzed for demonstration)  
- **Key Columns Used:**
  - "inning" — inning number  
  - "event" — outcome of the at-bat (Single, Double, Walk, Home Run, etc.)


## Data Cleaning & Preprocessing
The dataset was cleaned to focus on offensive events by performing the follwing transformations:
- Dropped irrelevant columns ("ab_id", "g_id", "batter_id", "pitcher_id")
- Standardized all out-type events (Flyout, Lineout, Strikeout, etc.) to "Out"  
- Removed all plays where "event == Out"  
- Sorted remaining events by inning and event  
- Assigned numeric codes to events for plotting purposes (e.g., Single = 4, Home Run = 2)
- Number of outcomes analyzed was reduced from the initial >180,000 to just the first 100 events of the season.


## Visualizations
### 1. Multi-Line Chart
- Displays the frequency of each offensive event across all 9 innings  
- Each inning is represented as a separate colored line  
- X-axis: Event types, Y-axis: Number of occurrences  

### 2. 3×3 Subplot Grid
- 3×3 layout showing one subplot per inning (1–9)  
- Consistent axis scaling for easy comparison  
- Each subplot displays event frequencies using different colors and markers
