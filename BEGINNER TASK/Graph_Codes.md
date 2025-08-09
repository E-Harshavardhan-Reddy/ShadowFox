
## 1. Line Plot

Use Case: Visualizing trends over time or sequential data.

### Matplotlib Example

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Line Plot")
plt.show()
```

### Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.lineplot(x=[1, 2, 3, 4, 5], y=[2, 4, 6, 8, 10])
plt.title("Line Plot")
plt.show()
```

---

## 2. Bar Chart

Use Case: Comparing quantities across categories.

### Matplotlib Example

```python
import matplotlib.pyplot as plt

categories = ["A", "B", "C", "D"]
values = [4, 7, 2, 9]

plt.bar(categories, values)
plt.xlabel("Categories")
plt.ylabel("Values")
plt.title("Bar Chart")
plt.show()
```

### Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.barplot(x=["A", "B", "C", "D"], y=[4, 7, 2, 9])
plt.title("Bar Chart")
plt.show()
```

---

## 3. Scatter Plot

Use Case: Showing the relationship between two numerical variables.

### Matplotlib Example

```python
import matplotlib.pyplot as plt

x = [5, 7, 8, 7, 6, 9, 5, 8]
y = [99, 86, 87, 88, 100, 86, 103, 87]

plt.scatter(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Scatter Plot")
plt.show()
```

### Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.scatterplot(x=[5, 7, 8, 7, 6, 9, 5, 8], y=[99, 86, 87, 88, 100, 86, 103, 87])
plt.title("Scatter Plot")
plt.show()
```

---

## 4. Histogram

Use Case: Distribution of a dataset.

### Matplotlib Example

```python
import matplotlib.pyplot as plt

data = [7, 8, 5, 6, 3, 4, 5, 6, 7, 8, 9, 5, 6, 7]

plt.hist(data, bins=5, color='skyblue', edgecolor='black')
plt.xlabel("Bins")
plt.ylabel("Frequency")
plt.title("Histogram")
plt.show()
```

### Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.histplot([7, 8, 5, 6, 3, 4, 5, 6, 7, 8, 9, 5, 6, 7], bins=5, kde=False, color='skyblue')
plt.title("Histogram")
plt.show()
```

---

## 5. Pie Chart

Use Case: Showing proportions in a dataset.

### Matplotlib Example

```python
import matplotlib.pyplot as plt

sizes = [15, 30, 45, 10]
labels = ["A", "B", "C", "D"]

plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=140)
plt.title("Pie Chart")
plt.show()
```

*(No Seaborn Example – Seaborn does not support Pie Charts directly.)*

---

## 6. Box Plot

Use Case: Showing distribution and outliers in a dataset.

### Matplotlib Example

```python
import matplotlib.pyplot as plt

data = [7, 8, 5, 6, 3, 4, 5, 6, 7, 8, 9, 5, 6, 7]

plt.boxplot(data)
plt.title("Box Plot")
plt.show()
```

### Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.boxplot(data=[7, 8, 5, 6, 3, 4, 5, 6, 7, 8, 9, 5, 6, 7])
plt.title("Box Plot")
plt.show()
```

---

## 7. Heatmap

Use Case: Correlation or intensity matrix (Seaborn only).

### Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

correlation_matrix = heat_df.corr()


fig, ax = plt.subplots(figsize=(8, 6)) # Adjust size for better readability


sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f", ax=ax)
ax.set_title('Correlation Matrix of Iris Dataset')


plt.show()
```

---


