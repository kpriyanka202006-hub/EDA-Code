import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
# Load the dataset
df = pd.read_excel("weatherHistory.xlsx")
# Select numerical columns and drop constant column
num_data = df.select_dtypes(include=["number"]).drop(
    columns=["LoudCover"]
)
# Create correlation matrix
corr_matrix = num_data.corr()
# Draw heatmap
plt.figure(figsize=(8, 6))
sns.heatmap(
    corr_matrix,
    annot=True,
    cmap="coolwarm",
    fmt=".2f"
)
plt.title("Correlation Matrix Heatmap")
plt.show()


output
<img width="382" height="317" alt="image" src="https://github.com/user-attachments/assets/ef30a50f-7714-4566-a698-a55abd607b4b" />
