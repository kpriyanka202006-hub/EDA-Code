import pandas as pd
pd.set_option("display.width", 120)
pd.set_option("display.max_columns", 20)
# Load dataset
df = pd.read_csv("weatherHistory.csv")
# Convert Formatted Date to datetime
df["Formatted Date"] = pd.to_datetime(df["Formatted Date"], utc=True)
# Create Season
def get_season(month):
    if month in [12, 1, 2]:
        return "Winter"
    elif month in [3, 4, 5]:
        return "Spring"
    elif month in [6, 7, 8]:
        return "Summer"
    else:
        return "Autumn"
df["Season"] = df["Formatted Date"].dt.month.apply(get_season)
# Display result
print(df[["Formatted Date", "Season"]].head()) 


output
<img width="1536" height="1024" alt="ChatGPT Image Sep 2, 2026, 03_18_39 PM" src="https://github.com/user-attachments/assets/074c3106-9e3b-41c0-8bb8-4ceb207f0372" />
