## 1. Basic CSV Writing

You can write a pandas DataFrame to a CSV file using the `to_csv()` function. This function takes the path of the CSV file as an argument.

### Example:

```python
import pandas as pd

# Sample DataFrame
data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis'],
    'Role': ['Batter', 'Bowler', 'All-Rounder'],
    'Country': ['Australia', 'South Africa', 'South Africa']
}

df = pd.DataFrame(data)

# Writing the DataFrame to a CSV file
df.to_csv('players.csv', index=False)

print("DataFrame written to 'players.csv'")
```

#### Explanation:
- `df.to_csv('players.csv', index=False)`: This writes the DataFrame to a CSV file named players.csv. The **index=False** argument ensures that the row indices are not written to the CSV file.

**NOTE**: The above method will overwrite the data which means that if the file already exist, then it will delete all the contents and then write the new content to it, otherwise if the file is not there, it will create one.

---

## 2. Adding to already existing csv file

```python
import pandas as pd

# Sample DataFrame with new data
data = {
    'PlayerName': ['Shane Warne', 'James Anderson'],
    'Role': ['Bowler', 'Bowler'],
    'Country': ['Australia', 'England']
}

new_df = pd.DataFrame(data)

# Appending new data to an existing CSV file
new_df.to_csv('players.csv', mode='a', header=False, index=False)

print("New data appended to 'players.csv'")
```

#### Explanation:
- `mode='a'`: This appends the data to the existing CSV file.
- `header=False`: This prevents pandas from writing the column names again when appending.

---

- There are many more options while writing to a csv writing only specific columns, specifying custom separator and more, thus I encourage you to explore other options too.
- **While writing, its important to give the correct path**.
- There could also be `NULL` values in the csv, you can handle those as well with some custom values.

---

**[Back to Home Page](https://github.com/RahulRoy-rsp/Learn_Pandas)**