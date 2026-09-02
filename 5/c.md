 import pandas as pd
df = pd.read_excel("weatherHistory.xlsx")
# Select numerical columns and drop constant column
num_data = df.select_dtypes(include=["number"]).drop(
    columns=["LoudCover"]
)
corr_matrix = num_data.corr()
print("Highly Correlated Variable Pairs\n")
for i in range(len(corr_matrix.columns)):
    for j in range(i + 1, len(corr_matrix.columns)):
        value = corr_matrix.iloc[i, j]

        if value > 0.8 or value < -0.8:
            print(
                corr_matrix.columns[i],
                "<-->",
                corr_matrix.columns[j],
                "=",
                round(value, 2)
            )


output
<img width="325" height="69" alt="image" src="https://github.com/user-attachments/assets/c8c3f54c-a5f7-4c42-bad0-167bea69d1c6" />

