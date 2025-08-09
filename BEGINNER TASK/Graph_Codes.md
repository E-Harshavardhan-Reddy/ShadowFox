# 📊 Graph Types with Code Examples
# This section includes commonly used plot types, each demonstrated with both Plotly Express and Seaborn/Matplotlib examples.


# 1. 📈 Line Plot
# Use Case: Visualizing trends over time.


# ➤ Plotly Express Example
import plotly.express as px

line_df = {'Day': [1, 2, 3, 4, 5], 'Visitors': [10, 12, 8, 15, 20]}
fig = px.line(line_df, x='Day', y='Visitors', title='Website Visitors Over Days', markers=True)
fig.show()

import seaborn as sns
flights = sns.load_dataset("flights")
fig = px.line(flights, x="month", y="passengers", color="year", title="Monthly Passengers per Year")
fig.show()


# 2. 📊 Bar Chart
# Use Case: Comparing values across categories.


# ➤ Plotly Express Example
bar_df = {'Platform': ['A', 'B', 'C', 'D'], 'Users (in millions)': [23, 45, 56, 78]}
fig = px.bar(bar_df, x='Platform', y='Users (in millions)', title='Social Media Platform Users')
fig.show()

data = sns.load_dataset("titanic")
fig = px.bar(data, x="class", title="Titanic Passengers by Class", color="class",
             category_orders={"class": ["First", "Second", "Third"]})
fig.show()


# 3. 🔵 Scatter Plot
# Use Case: Showing relationships between two variables.


# ➤ Plotly Express Example
scatter_df = {'Age': [25, 30, 35, 40, 45], 'Income': [40, 50, 60, 65, 70]}
fig = px.scatter(scatter_df, x='Age', y='Income', title='Age vs. Income')
fig.show()

fig = px.scatter(scatter_df, x='Age', y='Income', title='Age vs. Income',
                 color='Age', size='Income')
fig.show()


# 4. 📉 Histogram
# Use Case: Displaying data distribution.


# ➤ Plotly Express Example
fig = px.histogram(scatter_df, x='Income', nbins=10, title='Income Distribution')
fig.show()

fig = px.histogram(scatter_df, x='Income', nbins=10, title='Income Distribution', marginal="rug")
fig.show()


# 5. 🥧 Pie Chart
# Use Case: Showing proportions.


# ➤ Plotly Express Example
pie_df = {'Activity': ['Work', 'Sleep', 'Exercise', 'Leisure'],
          'Hours': [8, 8, 2, 6]}
fig = px.pie(pie_df, values='Hours', names='Activity', title='Daily Activities')
fig.show()


# 6. 📦 Box Plot
# Use Case: Summarizing distribution with min, max, median, and outliers.


# ➤ Plotly Express Example
box_df = {'Department': ['HR', 'IT', 'Finance', 'IT', 'HR'],
          'Salary': [50000, 60000, 55000, 62000, 52000]}
fig = px.box(box_df, x='Department', y='Salary', title='Salary Distribution by Department')
fig.show()

# ➤ Seaborn Example
import matplotlib.pyplot as plt
fig, ax = plt.subplots()
sns.boxplot(data=box_df, x='Department', y='Salary', ax=ax)
ax.set_title('Salary Distribution by Department')
plt.show()


# 7. 🌡️ Heatmap
# Use Case: Correlation or intensity matrix.

# ➤ Seaborn Example
heat_df = sns.load_dataset("iris")
correlation_matrix = heat_df.corr()

fig, ax = plt.subplots(figsize=(8, 6))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f", ax=ax)
ax.set_title('Correlation Matrix of Iris Dataset')
plt.show()
