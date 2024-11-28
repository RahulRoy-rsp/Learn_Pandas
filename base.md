## 1. Reading top n number of rows

- You can use the `head()` method to view the first `n` rows of a DataFrame. 
- By default, it shows the first 5 rows, but you can specify a different number.

### Syntax:
```
dataframe_name.head(number_of_rows)
```

## 2. Reading bottom n number of rows

- You can use the `tail()` method to view the last `n` rows of a DataFrame. 
- Similar to `head()`, by default it shows the last 5 rows, but you can specify any number.

### Syntax:
```
dataframe_name.tail(number_of_rows)
```

## 3. Finding out the number of rows

- To find out the `number of rows` in a DataFrame, you can use the `shape` attribute. 
- The `first value` of the tuple returned by shape represents the number of rows.

### Syntax:
```
dataframe_name.shape[0]
```

## 4. Finding out the number of columns

- To find out the `number of columns` in a DataFrame, you can use the `shape` attribute. 
- The `second value` of the tuple returned by shape represents the number of columns.

### Syntax:
```
dataframe_name.shape[1]
```

## 5. Finding out the dimensions of a dataframe

- To find the `dimensions` of a DataFrame (i.e number of rows and columns), you can use the `shape` attribute. 
- It returns a *tuple* with the `number of rows and columns`.

### Syntax:
```
dataframe_name.shape
```

---
### Example:
```python
import pandas as pd

# Sample DataFrame
data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis', 'Ajanta Mendis', 'Kapil Dev'],
    'Role': ['Batter', 'Bowler', 'All-Rounder', 'Bowler', 'All-Rounder'],
    'Country': ['Australia', 'South Africa', 'South Africa', 'Sri Lanka', 'India']
}

df = pd.DataFrame(data)

# Reading the top 3 rows
top_rows = df.head(3)
print(top_rows)

# Reading the bottom 2 rows
bottom_rows = df.tail(2)
print(bottom_rows)

# Finding the number of rows
num_rows = df.shape[0]
print(f'Number of rows: {num_rows}')

# Finding the number of columns
num_columns = df.shape[1]
print(f'Number of columns: {num_columns}')

# Finding the dimensions of the DataFrame
dimensions = df.shape
print(f'Dimensions: {dimensions}')
```

---
- These methods are useful but this does not mean that these are the only way to achieve a specific thing, there exist other ways as well.

---

**[Back to Home Page](https://github.com/RahulRoy-rsp/Learn_Pandas)**