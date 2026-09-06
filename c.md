PROGRAM 1
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
print(df)


OUT PUT 1
<img width="370" height="186" alt="Screenshot 2026-09-06 153633" src="https://github.com/user-attachments/assets/8146400a-40c9-403c-96a5-f1cf8e8fa540" />

PROGRAM 2
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
print(df.isnull().sum())

OUT PUT 2
<img width="222" height="164" alt="Screenshot 2026-09-06 153655" src="https://github.com/user-attachments/assets/d9207589-abbd-4fd7-aa67-dbcb9eacd331"/> 

PROGRAM 3
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
num_cols = ['Temperature_C', 'Humidity_%', 'Wind_Speed_km_h', 'Precipitation_mm']
for col in num_cols:
df[col] = df[col].fillna(df[col].mean())
print(df)

OUT PUT 3
<img width="787" height="385" alt="Screenshot 2026-09-06 153712" src="https://github.com/user-attachments/assets/08bd30f3-f8ca-4f46-b5f6-cdafc6c9a52b" />



PROGRAM 4
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
df['City'] = df['City'].fillna(df['City'].mode()[0])
print(df)

OUT PUT 4
<img width="782" height="394" alt="Screenshot 2026-09-06 153732" src="https://github.com/user-attachments/assets/1ea8a2bb-d447-476d-b410-551c7454fc3d" />

PROGRAM 5
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
print(df[df.duplicated()])

OUT PUT 5
<img width="788" height="74" alt="Screenshot 2026-09-06 153756" src="https://github.com/user-attachments/assets/cf530ba4-534c-446a-b9ea-627974bcf32c" />


PROGRAM 6
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
df = df.drop_duplicates()
print(df)

OUT PUT 6
<img width="798" height="354" alt="Screenshot 2026-09-06 153819" src="https://github.com/user-attachments/assets/e362ee21-fa22-4518-997d-78771cb4c059" />

PROGRAM 7
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
df['City'] = df['City'].replace('dubai', 'Dubai')
print(df)

OUT PUT 7
<img width="654" height="432" alt="Screenshot 2026-09-06 153835" src="https://github.com/user-attachments/assets/1d65b45d-59f7-477b-a3cd-a3e85bdf166c" />


PROGRAM 8
import pandas as pd
df = pd.read_csv('weather_dataset_2025.csv')
num_cols = ['Temperature_C', 'Humidity_%', 'Wind_Speed_km_h', 'Precipitation_mm']
for col in num_cols:
df[col] = df[col].fillna(df[col].mean())
df['City'] = df['City'].replace('dubai', 'Dubai')
df = df.drop_duplicates()
print("Missing Values:")
print(df.isnull().sum())
print("\nDuplicate Records count:")
print(df.duplicated().sum())
print("\nCleaned Dataset:")
print(df)



OUT PUT 8
<img width="793" height="573" alt="Screenshot 2026-09-06 153859" src="https://github.com/user-attachments/assets/3e339f51-ffba-451e-a938-875a86b335d8" />
