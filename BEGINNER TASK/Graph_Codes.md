

### Graph Types with Code Examples

## This section includes commonly used plot types, each demonstrated with both Matplotlib and Seaborn examples.



### 1. Line Plot

**Use Case:** Visualizing trends over time.

#### ➤ Matplotlib Example

```python
import plotly.express as px

fig = px.line(line_df, x='Day', y='Visitors', title='Website Visitors Over Days', markers=True)
fig.show()
```

#### ➤ Seaborn Example

```python
import plotly.express as px

fig = px.line(flights, x="month", y="passengers", color="year", title="Monthly Passengers per Year")
fig.show()
```

---

### 2. Bar Chart

**Use Case:** Comparing values across categories.

#### ➤ Matplotlib Example

```python
import plotly.express as px

fig = px.bar(bar_df, x='Platform', y='Users (in millions)', title='Social Media Platform Users')
fig.show()
```

#### ➤ Seaborn Example

```python
import plotly.express as px
import seaborn as sns

data = sns.load_dataset("titanic")
fig = px.bar(data, x="class", title="Titanic Passengers by Class", color="class",
             category_orders={"class": ["First", "Second", "Third"]})
fig.show()
```

---

### 3. Scatter Plot

**Use Case:** Showing relationships between two variables.

#### ➤ Matplotlib Example

```python
import plotly.express as px

fig = px.scatter(scatter_df, x='Age', y='Income', title='Age vs. Income')
fig.show()
```

#### ➤ Seaborn Example

```python
import plotly.express as px

fig = px.scatter(scatter_df, x='Age', y='Income', title='Age vs. Income', color='Age', size='Income')
fig.show()
```

---

### 4. Histogram

**Use Case:** Displaying data distribution.

#### ➤ Matplotlib Example

```python
import plotly.express as px

fig = px.histogram(scatter_df, x='Income', nbins=10, title='Income Distribution')
fig.show()
```

#### ➤ Seaborn Example

```python
import plotly.express as px

fig = px.histogram(scatter_df, x='Income', nbins=10, title='Income Distribution', marginal="rug")
fig.show()
```

---

### 5. Pie Chart

**Use Case:** Showing proportions (Matplotlib only).

#### ➤ Matplotlib Example

```python
import plotly.express as px

fig = px.pie(pie_df, values='Hours', names='Activity', title='Daily Activities')
fig.show()
```

---

### 6. Box Plot

**Use Case:** Summarizing spread and outliers in data.

#### ➤ Matplotlib Example

```python
import plotly.express as px

fig = px.box(box_df, x='Department', y='Salary', title='Salary Distribution by Department')
fig.show()
```

#### ➤ Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
sns.boxplot(data=box_df, x='Department', y='Salary', ax=ax)
ax.set_title('Salary Distribution by Department')
plt.show()
```

---

### 7. Heatmap

**Use Case:** Correlation or intensity matrix (Seaborn only).

#### ➤ Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

correlation_matrix = heat_df.corr()
fig, ax = plt.subplots(figsize=(8, 6))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f", ax=ax)
ax.set_title('Correlation Matrix of Iris Dataset')
plt.show()
```

---


