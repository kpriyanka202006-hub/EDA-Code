import pandas as pd
import matplotlib.pyplot as plt
# Load dataset
df = pd.read_csv(&quot;Rolling_Weather_Dataset.csv&quot;)
# Convert Date column
df[&quot;Date&quot;] = pd.to_datetime(df[&quot;Date&quot;], dayfirst=True)
# Set index
df.set_index(&quot;Date&quot;, inplace=True)
# Rolling Mean
df[&quot;Rolling_Mean&quot;] = df[&quot;Temperature&quot;].rolling(window=7).mean()
# Plot
plt.figure(figsize=(10,5))
plt.plot(df.index, df[&quot;Temperature&quot;], label=&quot;Original Temperature&quot;)
plt.plot(df.index, df[&quot;Rolling_Mean&quot;], linewidth=3, label=&quot;7-Day Rolling Mean&quot;)
plt.title(&quot;Temperature vs 7-Day Rolling Mean&quot;)
plt.xlabel(&quot;Date&quot;)
plt.ylabel(&quot;Temperature (°C)&quot;)
plt.legend()
plt.show()


output
<img width="538" height="261" alt="Screenshot 2026-09-02 145418" src="https://github.com/user-attachments/assets/608a8ed8-bf3f-49b3-9083-868878b673d9" />
