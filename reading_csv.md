## 1. Basic CSV Reading

To read a CSV file into a pandas DataFrame, you can use the `pd.read_csv()` function. This function requires the path to the CSV file as an argument.

### Example:

```python
import pandas as pd

# Reading a CSV file
df = pd.read_csv('players.csv')

# Displaying the DataFrame
print(df)
```

#### Explanation:
- **pd.read_csv('players.csv')**: This reads the CSV file named *players.csv* and loads its contents into a DataFrame.
- **df**: The DataFrame that contains the data from the CSV file.

**NOTE**: The above method will work correctly if the first row is the column names and below that is the data for the respective columns.

---

## 2. CSV without headers, specifying column names

### Example:

```python
import pandas as pd

# Reading a CSV file which does not have headers, thus specifying column names
df = pd.read_csv('players.csv', names=['PlayerName', 'Role', 'Country'])

# Displaying the DataFrame
print(df)
```

#### Explanation:
- `names=['PlayerName', 'Role', 'Country']`: This assigns custom column names to the DataFrame since the CSV doesn't contain headers.

---

## 3. Reading only specific column names from a csv file

### Example:

```python
import pandas as pd

# Reading only the 'PlayerName' and 'Country' columns
df = pd.read_csv('players.csv', usecols=['PlayerName', 'Country'])

# Displaying the DataFrame
print(df)
```

#### Explanation:
- `usecols=['PlayerName', 'Country']`: This reads only the specified columns *('PlayerName' and 'Country')* from the CSV file.

---

- There are many more options while reading a csv like skipping number of rows and reading from a specific row number.
- Usually csv is `comma separated` but there can be other separators as well like a `semi colon` and more, thus I encourage you to explore more options too.
- Who knows what kind of requirement you have and that option is already available.
- **While reading the csv, its important to give the correct path**.
- There could also be `NULL` values in the csv, you can handle those as well with some custom values.

---

**[Back to Home Page](https://github.com/RahulRoy-rsp/Learn_Pandas)**
