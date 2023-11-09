pip3 install pandas
pip3 install matplotlib


df = pd.read_csv("data_small/TG_STAID000001.txt", skiprows=20, parse_dates=["    DATE"])
print(df[0:10])

df.columns

df['   TG']

df[['   TG', '    DATE']]

df.loc[df['   TG'] != -999]

df.loc[df['   TG'] != -999['   TG'].mean() / 10

df.loc[df['   TG'] != -999['   TG'].max() / 10

df.loc[df['   TG'] != -999['   TG'].min() / 10

df.loc[df['   TG'] != -999['   TG'].hist()

# Get certain cells

df.loc[df['    DATE']=="1860-01-05"]  # DataFrame

df.loc[df['    DATE']=="1860-01-05"]['   TG'].squeeze() / 10

df.loc[df['   TG'] == ['   TG'].max()]['    DATE'].squeeze()

df.loc[3, '   TG']

# Calculate a new column out of existing column

import numpy as np
df["TG0"] = df['   TG'].mask(df['   TG'] == -9999, np.nan)

df["TG"] = df['TG0'] / 10

df["Fahrenheit"] = df["TG"] * (9/5) + 32

# Plotting

df["Fahrenheit"].hist()

df["TG"].hist()

df.plot(x='    DATE', y="TG", figsize=(15, 3))

df[100, 1000].plot(x='    DATE', y="TG", figsize=(15, 3))

