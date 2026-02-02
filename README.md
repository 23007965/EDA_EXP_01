```
Name : P PARTHIBAN
Register number : 212223230145
```
# Experiment 1: EDA in IPL Dataset

## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

### 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
### 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
### 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
### 4.Top Winning Teams (Univariate Analysis)**
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
### 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
### 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
### 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.

## Program

### Basic info about dataset:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/matches.csv")
df.shape

df.head()
```
### Matches per season:
```python
season_count=df['season'].value_counts().sort_index()
season_count

plt.figure(figsize=(14, 6))
plt.bar(season_count.index, cseason_ount.values)
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Number of IPL Matches Played Per Season")
plt.show()
```

```python
winners=df['winner'].value_counts()
winners.head()

plt.figure(figsize=(14, 5))
plt.bar(winners.head(5).index, winners.head(5).values)
plt.xlabel("Team")
plt.ylabel("Number of Wins")
plt.title("Top 5 Teams with Most Wins in IPL")
plt.show()
```

```python
decisions = df['toss_decision'].value_counts()
decisions

plt.figure(figsize=(6, 4))
plt.bar(decisions.index,decisions.values)
plt.xlabel("Toss Decision")
plt.ylabel("Count")
plt.title("Toss Decision Preference in IPL")
plt.show()
```
```python
top_venues = df['venue'].value_counts().head(5)
top_venues

plt.figure(figsize=(15, 6))
plt.bar(top_venues.index, top_venues.values)
plt.xlabel("Venue")
plt.ylabel("Number of Matches Hosted")
plt.title("Top 5 Venues Hosting Most IPL Matches")
plt.show()
```

## Output

<img width="1712" height="439" alt="image" src="https://github.com/user-attachments/assets/5e35487a-b389-4a72-8ec9-7311e3dea4f7" />

<img width="1376" height="616" alt="image" src="https://github.com/user-attachments/assets/efca3ef4-c705-4cd1-afe5-e06326f9306f" />

<img width="1339" height="522" alt="image" src="https://github.com/user-attachments/assets/83d346f3-4544-47a0-83d3-9270e576cc3b" />

<img width="672" height="436" alt="image" src="https://github.com/user-attachments/assets/0d28d55f-6847-4b63-addd-f25ede4d7ede" />

<img width="1474" height="609" alt="image" src="https://github.com/user-attachments/assets/d1f92b8d-8152-457f-bc6f-b9c867d144dc" />
  
## Result
  This experiment is executed successfully
