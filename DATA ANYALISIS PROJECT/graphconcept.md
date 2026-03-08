Rule of Thumb: How Many Axes?

One numeric variable → 1 axis → Distribution

Use Histogram or Boxplot

Example: Salary distribution → plt.hist(df['Salary'])

Numeric vs Numeric → 2 axes → Relationship

X-axis = independent variable (Experience_Years)

Y-axis = dependent variable (Salary)

Use Scatter plot or Line plot

Example: Experience vs Salary → plt.scatter(df['Experience_Years'], df['Salary'])

Categorical vs Numeric → 2 axes → Comparison

X-axis = category (Department)

Y-axis = numeric value (Salary)

Use Bar chart or Boxplot

Example: Average Salary per Department → df.groupby('Department')['Salary'].mean().plot(kind='bar')

Categorical vs Categorical → 2 axes → Relationship / Count

X-axis = category 1 (Attrition)

Hue/Secondary axis = category 2 (Department)

Use Countplot or Stacked bar chart

Example: Attrition count per Department → sns.countplot(x='Attrition', hue='Department', data=df)

Time vs Numeric → 2 axes → Trend

X-axis = time (Year, Month)

Y-axis = numeric (Salary, count)

Use Line plot

Example: Hiring trend → df.groupby('Joining_Year')['Employee_ID'].count().plot(kind='line')

3️⃣ Quick Graph Selection Cheat Sheet
Goal	X-axis	Y-axis	Graph Type
Distribution of numeric	None	Numeric	Histogram / Boxplot
Compare numeric by category	Categorical	Numeric	Bar plot / Boxplot
Relationship between numeric variables	Numeric	Numeric	Scatter plot / Line plot
Count/frequency of categories	Category	Count	Bar chart / Countplot
Trends over time	Time	Numeric	Line plot
Correlation among numeric	Numeric	Numeric	Heatmap / Pairplot
4️⃣ Examples Using Your HR Dataset
1️⃣ One axis (Distribution)
plt.hist(df['Salary'])
plt.show()

2️⃣ Two axes (Numeric vs Numeric)
plt.scatter(df['Experience_Years'], df['Salary'])
plt.show()

3️⃣ Two axes (Category vs Numeric)
sns.boxplot(x='Department', y='Salary', data=df)

4️⃣ Two axes (Category vs Category)
sns.countplot(x='Attrition', hue='Department', data=df)

5️⃣ Two axes (Time vs Numeric)
df.groupby('joining_year')['Salary'].mean().plot(kind='line')
plt.show()

5️⃣ Remember This Mental Trick

✅ Ask yourself 3 questions:

How many variables am I analyzing?

One → Distribution

Two → Relationship or Comparison

What type of variable is each?

Numeric → Y-axis

Categorical → X-axis

Time → X-axis

What do I want to show?

Distribution → Histogram / Boxplot

Comparison → Bar / Boxplot

Relationship → Scatter / Line

Frequency → Countplot / Bar