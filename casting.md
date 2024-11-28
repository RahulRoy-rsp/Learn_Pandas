## 1. Changing the Data Type of a Single Column

You can change the data type of a single column using the `astype()` method.

### Example: Converting a Column to Integer

```python
import pandas as pd

# Sample DataFrame
data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis'],
    'Age': ['49', '41', '49']  # Here, Age is represented as a string
}

df = pd.DataFrame(data)

# Converting 'Age' column to an integer
df['Age'] = df['Age'].astype(int)

# Displaying the DataFrame
print(df)
```

#### Explanation:
- `df['Age'].astype(int)`: Converts the Age column from a *string* type to an *integer* type.

---

## 2. Changing the Data Type of Multiple Columns

You can change the data type of multiple columns at once using a dictionary inside the astype() method.

### Example: Converting Multiple Columns to Integer

```python
import pandas as pd

# Sample DataFrame
data = {
    'PlayerName': ['Ricky Ponting', 'Dale Steyn', 'Jack Kallis'],
    'Age': ['49', '41', '49'],  # Age as string
    'Score': ['100', '90', '95'],  # Score as string
}

df = pd.DataFrame(data)

# Converting 'Age' and 'Score' columns to integer type
df = df.astype({'Age': 'int', 'Score': 'int'})

# Displaying the DataFrame
print(df)
```
#### Explanation:
- `df.astype({'Age': 'int', 'Score': 'int'})`: Converts both the Age and Score columns to integer type.
---
- Always ensure that the data you are converting is compatible with the target type. For instance, trying to convert a non-numeric string to an integer will throw an error unless handled.
- Its important to go through the number of data types available for the conversion, especially when you deal with date and time conversion as there are multiple ways to do the same thing, so its up to you how you convert.
- You can refer the official documentation.

---
**[Back to Home Page](https://github.com/RahulRoy-rsp/Learn_Pandas)**