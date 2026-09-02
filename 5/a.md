import pandas as pd
# Load the dataset
df = pd.read_excel("weatherHistory.xlsx")
# Select numerical columns and drop constant column
num_data = df.select_dtypes(include=["number"]).drop(
    columns=["LoudCover"]
)
# Create correlation matrix
corr_matrix = num_data.corr()
# Display correlation matrix
print("Correlation Matrix")
print(corr_matrix) 



output
<img width="495" height="96" alt="image" src="https://github.com/user-attachments/assets/65ad367c-12f0-42d3-b769-28c7fecf8ab0" />
