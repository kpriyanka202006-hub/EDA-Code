import pandas as pd
from scipy.stats import ttest_ind
df = pd.read_csv("Weather_Dataset.csv")
# Create two groups
sunny = df[df["Weather"] == "Sunny"]["Temperature"]
cloudy = df[df["Weather"] == "Cloudy"]["Temperature"]
# Perform Independent Sample t-test
t_value, p_value = ttest_ind(sunny, cloudy)
# Display results
print("t-value :", t_value)
print("p-value :", p_value)


output 
<img width="509" height="53" alt="Screenshot 2026-09-08 200339" src="https://github.com/user-attachments/assets/1c31304a-172e-423a-aea4-b3cf2eb61584" />

