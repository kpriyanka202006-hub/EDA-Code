import pandas as pd
df = pd.read_csv("messy_weather_2025.csv")
print("Original Column Names:")
print(df.columns)
df.rename(
    columns={
        "dt": "Date",
        "loc": "City",
        "temp": "Temperature_C",
        "hum": "Humidity_%",
        "ws": "Wind_Speed_km_h",
        "prec": "Precipitation_mm"
    },
    inplace=True
)

print("\nRenamed Column Names:")
print(df.columns)


output

