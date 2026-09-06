PROGRAM 1
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Weather_Dataset.csv")
condition_count = df['Weather Condition'].value_counts()
plt.figure(figsize=(8,5))
condition_count.plot(kind='bar')
plt.title("Record Count by Weather Condition")
plt.xlabel("Weather Condition")
plt.ylabel("Number of Records")
plt.show()


OUT PUT 1
<img width="769" height="424" alt="Screenshot 2026-09-06 160306" src="https://github.com/user-attachments/assets/5b080ff7-1ea1-4a78-acc0-cb0c781006fd" />


PROGRAM 2
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Weather_Dataset.csv")
condition_count = df['Weather Condition'].value_counts()
plt.figure(figsize=(7,7))
condition_count.plot(kind='pie', autopct='%1.1f%%')
plt.title("Weather Condition Distribution")
plt.ylabel("")
plt.show()

OUT PUT 2
<img width="630" height="528" alt="Screenshot 2026-09-06 160321" src="https://github.com/user-attachments/assets/0bf818d7-af61-4bdd-b550-50e96a098b8e" />



PROGRAM 3
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Weather_Dataset.csv")
df.columns = df.columns.str.strip()
plt.figure(figsize=(8,5))
plt.hist(df["Temperature"], bins=10, edgecolor="black")
plt.title("Distribution of Temperature")
plt.xlabel("Temperature (°C)")
plt.ylabel("Frequency")
plt.grid(True)
plt.show()


OUT PUT 3
<img width="716" height="424" alt="Screenshot 2026-09-06 160342" src="https://github.com/user-attachments/assets/6bf2692c-af6d-42a7-815a-265228c69637" />

PROGRAM 4
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Weather_Dataset.csv")
df.columns = df.columns.str.strip()
plt.figure(figsize=(6,5))
plt.boxplot(df["Temperature"])
plt.title("Box Plot of Temperature")
plt.ylabel("Temperature (°C)")
plt.grid(True)
plt.show()


OUT PUT 4
<img width="615" height="453" alt="Screenshot 2026-09-06 160417" src="https://github.com/user-attachments/assets/ebacb48f-0b1d-4b25-9db5-9a68a3e72a8c" />


PROGRAM 5
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("Weather_Dataset.csv")
df.columns = df.columns.str.strip()
plt.figure(figsize=(8,5))
plt.scatter(df["Humidity"], df["Temperature"])
plt.title("Humidity vs Temperature")
plt.xlabel("Humidity (%)")
plt.ylabel("Temperature (°C)")
plt.grid(True)
plt.show()
 
OUT PUT 5
<img width="743" height="427" alt="Screenshot 2026-09-06 160435" src="https://github.com/user-attachments/assets/e64315c5-5bf8-4c61-851c-982ad867035a" />


