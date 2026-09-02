import pandas as pd

import matplotlib.pyplot as plt
# Load dataset
df = pd.read_csv(&quot;Rolling_Weather_Dataset.csv&quot;)
# Convert Date column
df[&quot;Date&quot;] = pd.to_datetime(df[&quot;Date&quot;], dayfirst=True)
# Set index
df.set_index(&quot;Date&quot;, inplace=True)
# Rolling Standard Deviation
df[&quot;Rolling_SD&quot;] = df[&quot;Temperature&quot;].rolling(window=7).std()
# Plot
plt.figure(figsize=(10,5))
plt.plot(df.index, df[&quot;Rolling_SD&quot;], linewidth=3)
plt.title(&quot;7-Day Rolling Standard Deviation&quot;)
plt.xlabel(&quot;Date&quot;)
plt.ylabel(&quot;Standard Deviation&quot;)
plt.show()



output
<img width="443" height="217" alt="Screenshot 2026-09-02 145427" src="https://github.com/user-attachments/assets/6701d0f8-bfdc-4c41-a1c8-8f342ae6ae0b" />
