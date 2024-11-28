## 1. `loc`: Label-based Indexing

The `loc` method is primarily used for selecting data by labels (i.e., row and column names).

### Syntax:

```python
df.loc[row_label, column_label]
```

### Example:

```python
import pandas as pd

data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis'],
    'Role': ['Batter', 'Bowler', 'All-Rounder'],
    'Country': ['Australia', 'South Africa', 'South Africa']
}

df = pd.DataFrame(data)

# Retreiving the Role for the second row (index starts from 0)
# '1' is the label of the second row, 'Role' is the column label
result = df.loc[1, 'Role']
print(result)
```
#### Output:
```
Bowler
```

## 2. `iloc`: Integer-location based Indexing

The `iloc` method is used for selecting data by integer positions. It works on row and column indices, where both row and column numbers are zero-based.

### Syntax:

```python
df.iloc[row_index, column_index]
```

### Example:

```python
import pandas as pd

data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis'],
    'Role': ['Batter', 'Bowler', 'All-Rounder'],
    'Country': ['Australia', 'South Africa', 'South Africa']
}

df = pd.DataFrame(data)

# Retreiving the value of second row and third column 
result = df.iloc[1, 2]
print(result)
```
#### Output
```
South Africa
```

## 3. Selecting Multiple Rows and Columns

Both `loc` and `iloc` can also be used to select multiple rows or columns by passing a list or range of labels/indices.

### Example: Selecting Multiple Rows and Columns using `loc`

```python
import pandas as pd

data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis'],
    'Role': ['Batter', 'Bowler', 'All-Rounder'],
    'Country': ['Australia', 'South Africa', 'South Africa']
}

df = pd.DataFrame(data)

# Retreiving top two rows and selecting only PlayerName and Country
result = df.loc[0:1, ['PlayerName', 'Country']]
print(result)
```
#### Output
| PlayerName | Country
| -------- | ------- |
Ricky Ponting | Australia
Dale Steyn |South Africa

### Example: Selecting Multiple Rows and Columns using `iloc`

```python
import pandas as pd

data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis'],
    'Role': ['Batter', 'Bowler', 'All-Rounder'],
    'Country': ['Australia', 'South Africa', 'South Africa']
}

df = pd.DataFrame(data)

# Selecting multiple rows and columns using iloc
result = df.iloc[0:2, [0, 2]]  # Rows 0 to 1, Columns 0 and 2
print(result)
```
#### Output
| PlayerName | Country
| -------- | ------- |
Ricky Ponting | Australia
Dale Steyn |South Africa

---

- There are many use cases of selecting data from a dataframe using `loc` and `iloc`, we can use conditional statement as well.
- `loc` uses labels (i.e., the actual row/column names), while `iloc` uses integer-based indexing (i.e., the position of the row/column).
- Both `loc` and `iloc` support slicing and boolean indexing.
- When using slicing (eg: `df.loc[0:1, :]` or `df.iloc[0:2, :]`), the ending index is included when using `loc` (label-based), but it is excluded when using `iloc` (integer-based).

---

**[Back to Home Page](https://github.com/RahulRoy-rsp/Learn_Pandas)**