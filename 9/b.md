import pandas as pd
from scipy.stats import ttest_ind
# Load the dataset
df = pd.read_csv("Weather_Dataset.csv")
# Create two groups
sunny = df[df["Weather"] == "Sunny"]["Temperature"]
cloudy = df[df["Weather"] == "Cloudy"]["Temperature"]
# Perform Independent Sample t-test
t_value, p_value = ttest_ind(sunny, cloudy)
# Significance level
alpha = 0.05
print("t-value :", t_value)
print("p-value :", p_value)
# Conclusion
if p_value < alpha:
    print("\nConclusion:")
    print("Reject the Null Hypothesis (H0)")
    print("There is a significant difference between")
    print("Temperature during Sunny and Cloudy days.")
else:
    print("\nConclusion:")
    print("Fail to Reject the Null Hypothesis (H0)")
    print("There is no significant difference between")
    print("Temperature during Sunny and Cloudy days.")


output
<img width="325" height="156" alt="Screenshot 2026-09-08 200347" src="https://github.com/user-attachments/assets/421cc1c0-6144-4754-84f5-ebf506de1565" />

