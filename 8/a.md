import pandas as pd
# Load dataset
df = pd.read_csv(&quot;Rolling_Weather_Dataset.csv&quot;)
# Convert Date column into datetime format
df[&quot;Date&quot;] = pd.to_datetime(df[&quot;Date&quot;], dayfirst=True)
# Set Date as index
df.set_index(&quot;Date&quot;, inplace=True)
# Calculate Rolling Mean
df[&quot;Rolling_Mean&quot;] = df[&quot;Temperature&quot;].rolling(window=7).mean()
# Calculate Rolling Standard Deviation
df[&quot;Rolling_SD&quot;] = df[&quot;Temperature&quot;].rolling(window=7).std()
# Display result
print(df[[&quot;Temperature&quot;, &quot;Rolling_Mean&quot;, &quot;Rolling_SD&quot;]])





output
<img width="1550" height="1014" alt="ex 8 output for a" src="https://github.com/user-attachments/assets/04d7b4fd-905b-4cf2-88ec-a86ded448f06" />

