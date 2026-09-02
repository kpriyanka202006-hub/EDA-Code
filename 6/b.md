import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("weatherHistory.csv")

# Convert Formatted Date to datetime
df["Formatted Date"] = pd.to_datetime(
    df["Formatted Date"], utc=True
)

# Function to determine season
def get_season(month):
    if month in [12, 1, 2]:
        return "Winter"
    elif month in [3, 4, 5]:
        return "Spring"
    elif month in [6, 7, 8]:
        return "Summer"
    else:
        return "Autumn"

# Create Season column
df["Season"] = df["Formatted Date"].dt.month.apply(get_season)

# Sample 2000 records for a readable plot
df_sample = df.sample(
    n=2000,
    random_state=42
)

# Create Pair Plot
sns.pairplot(
    df_sample,
    vars=[
        "Temperature (C)",
        "Humidity",
        "Wind Speed (km/h)",
        "Visibility (km)",
        "Pressure (millibars)"
    ],
    hue="Season",
    diag_kind="hist"
)

# Display the plot
plt.show()




<img width="584" height="279" alt="Screenshot 2026-09-02 152045" src="https://github.com/user-attachments/assets/86332a7b-46f5-45ad-bcca-7980dccb5bff" />
