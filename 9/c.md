import pandas as pd
# Load the dataset
df = pd.read_csv("Weather_Dataset.csv")
# Group statistics
stats = df.groupby("Weather")["Temperature"].agg(
    ["count", "mean", "std", "min", "max"])
print("Temperature Statistics by Weather Condition")
print(stats)







output
<img width="415" height="99" alt="Screenshot 2026-09-08 200358" src="https://github.com/user-attachments/assets/c6bd0e92-6c35-43bb-9cb3-3a3ddc221c11" />
