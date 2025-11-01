---
title: "🌊 Pandas Adventure With Spongebob And Friends!"
seoTitle: "Pandas and Spongebob's Ocean Adventure"
seoDescription: "Join SpongeBob and friends as they dive deep into data with Python Pandas, through a colorful, whimsical journey of coding fun!"
datePublished: Sat Nov 01 2025 09:08:51 GMT+0000 (Coordinated Universal Time)
cuid: cmhg28nft000802ky0fo387sd
slug: pandas-adventure-with-spongebob-and-friends
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1761987992241/0ef91ff5-14fa-42be-94b8-bb3650468327.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1761988082863/a8cc8dc3-d7e2-4bc7-960f-c2466fac3670.png
tags: data-science, pandas

---

### *A Super-Duper, Eye-Popping, Jellyfish-Zapping Guide to Python Pandas!*

#### *Now with 200% more sparkle, emojis, colors, and Krusty Krab flair!*

---

> **"I’m ready! I’m ready! …to DATA DIVE!"**  
> — **SpongeBob SquarePants** 🧽✨

---

## 1️⃣ **Step 1: Summon Pandas!**

### *Let’s invite the data party to Bikini Bottom!*

```python
import pandas as pd   # pd = "Pandas Delight" 🍍
```

> **Patrick:** *"Do pandas live under rocks too?"*  
> **Squidward:** *“No, Patrick. It’s a* ***library****. Like a book.”*  
> **SpongeBob:** *"A book of DATA?! YAY!"*

**Output:** *(Silent loading… like a jellyfish sneaking up!)*

---

## 2️⃣ **Step 2: Create a Series – Jellyfish Catch Scoreboard!**

```python
jellyfish_catch = pd.Series(
    [5, 3, 8, 2],
    index=['SpongeBob', 'Patrick', 'Squidward', 'Mr. Krabs']
)
print(jellyfish_catch)
```

### **Jellyfish Leaderboard**

```plaintext
SpongeBob     5  ⭐⭐⭐⭐⭐
Patrick       3  ⭐⭐⭐
Squidward     8  ⭐⭐⭐⭐⭐⭐⭐⭐
Mr. Krabs     2  ⭐⭐
```

> **SpongeBob:** *"I’m #1! Jellyfishing champion!"*  
> **Squidward:** *"8? Naturally. I used classical music as bait."*  
> **Patrick:** *"I caught 3… then napped on them."*

**Try this:**

```python
jellyfish_catch['Patrick']  # → 3
```

---

## 3️⃣ **Step 3: DataFrame – Krusty Krab Employee Dashboard!**

```python
employees = pd.DataFrame({
    'Name': ['SpongeBob', 'Patrick', 'Squidward', 'Mr. Krabs'],
    'Job': ['Fry Cook', 'Under Rock', 'Cashier', 'Boss'],
    'Salary': [100, 0, 50, 1000],
    'Jellyfish': [5, 3, 8, 2]
})
```

### **Krusty Krab Employee Stats**

| # | **Name** | **Job** | **Salary** | **Jellyfish** |
| --- | --- | --- | --- | --- |
| 0 | **SpongeBob** | Fry Cook | **100** | 5 |
| 1 | **Patrick** | Under Rock | **0** | 3 |
| 2 | **Squidward** | Cashier | **50** | 8 |
| 3 | **Mr. Krabs** | Boss | **1000** | 2 |

> **Mr. Krabs:** *"Argh! Me money! And me bonus plan!"*  
> **Patrick:** *"I have a job? Cool!"*

**Quick Tricks:**

* `employees['Salary']` → All paychecks
    
* `employees.head(2)` → Peek at top 2 (SpongeBob & Patrick)
    

---

## 4️⃣ **Step 4: Read CSV – Open the Treasure Bottle!**

`bikini_bottom.csv`:

```plaintext
Name,Job,Salary,Jellyfish
SpongeBob,Fry Cook,100,5
Patrick,Under Rock,0,3
Squidward,Cashier,50,8
Mr. Krabs,Boss,1000,2
```

```python
df = pd.read_csv('bikini_bottom.csv')
```

**Same table appears!**

> **SpongeBob:** *"Data from the deep blue sea!"*  
> **Patrick:** *"Is there soda in the file?"*

**Pro Tip:** Use `delimiter=';'` for European-style CSVs!

---

## 5️⃣ **Step 5: Filter – Find the Rich & Famous!**

```python
high_earners = df[df['Salary'] > 50]
```

### **Bikini Bottom Millionaires Club**

| Name | Job | Salary | Jellyfish |
| --- | --- | --- | --- |
| **SpongeBob** | Fry Cook | **100** | 5 |
| **Mr. Krabs** | Boss | **1000** | 2 |

> **Patrick:** *"I didn’t qualify. Again."*  
> **Squidward:** *"A filter for refinement. Finally."*

**Try:**

* `df.loc[0:1]` → First two rows
    
* `df.iloc[-1]` → Last row (Mr. Krabs!)
    

---

## 6️⃣ **Step 6: Math & Bonuses – Jellyfish = Clams!**

```python
df['Bonus'] = df['Jellyfish'] * 10
```

### **Payday with Jellyfish Bonuses!**

| Name | Job | Salary | Jellyfish | **Bonus** |
| --- | --- | --- | --- | --- |
| SpongeBob | Fry Cook | 100 | 5 | **50** |
| Patrick | Under Rock | 0 | 3 | **30** |
| Squidward | Cashier | 50 | 8 | **80** |
| Mr. Krabs | Boss | 1000 | 2 | **20** |

```python
avg_by_job = df.groupby('Job')['Salary'].mean()
```

### **Average Salary by Job**

```plaintext
Boss          1000.0  
Fry Cook       100.0  
Cashier         50.0  
Under Rock       0.0
```

> **Mr. Krabs:** *"Jellyfish = PROFIT!"*  
> **Patrick:** *"30 clams? I’m rich in naps!"*

---

## 7️⃣ **Step 7: Fix Missing Data – Plug the Holes!**

```python
import numpy as np
df = pd.DataFrame({
    'Name': ['SpongeBob', 'Patrick', 'Squidward'],
    'Salary': [100, np.nan, 50]
})
df['Salary'] = df['Salary'].fillna(0)
```

### **Cleaned & Official**

| Name | Salary |
| --- | --- |
| SpongeBob | **100.0** |
| Patrick | **0.0** |
| Squidward | **50.0** |

> **Patrick:** *"I had missing data? I was napping!"*  
> **Squidward:** *"Officially worth 0. Perfect."*

**Or drop:** `df.dropna()` → Bye, Patrick!

---

# **Pandas Merging DataFrames: The Great Bikini Bottom Reunion!**

*Starring SpongeBob, Patrick, Squidward, and Mr. Krabs*

---

**SpongeBob bounces in with a clipboard:**

> "Today we’re having a **Krusty Krab Employee Reunion Party**! But oh no! The data got split into **two tables** — like when Squidward rips a clarinet sheet in half! We need to **merge** them back together using **Pandas**!"

**Patrick drools:**

> "Merge? Like merging ice cream flavors? I vote for **Vanilla-Chocolate-Krabby-Patty Swirl**!"

**Squidward groans:**

> "No, you pink disaster. **Merging DataFrames** means combining two tables based on a **common column** — like matching names or IDs. It’s not edible."

**Mr. Krabs claps claws:**

> "Argh! If we merge the data, I can see who’s earning what **and** how many patties they flipped! More data = more money!"

---

Let’s dive into **4 types of merges** with **funny examples** and **real code**!

---

## Step 1: Prepare Two DataFrames (The Split-Up!)

> **Table 1: Employee Info** (`employees_df`)  
> **Table 2: Performance Records** (`performance_df`)

```python
import pandas as pd

# Table 1: Who are they?
employees_df = pd.DataFrame({
    'Name': ['SpongeBob', 'Patrick', 'Squidward', 'Sandy'],
    'Job': ['Fry Cook', 'Nap Expert', 'Cashier', 'Scientist'],
    'Employee_ID': [101, 102, 103, 104]
})

# Table 2: How many Krabby Patties did they make?
performance_df = pd.DataFrame({
    'Employee_ID': [101, 102, 103, 105],
    'Patties_Flipped': [500, 2, 300, 1000],
    'Complaints': [0, 50, 200, 0]
})

print("Employees Table:")
print(employees_df)
print("\nPerformance Table:")
print(performance_df)
```

**Output:**

```plaintext
Employees Table:
       Name         Job  Employee_ID
0  SpongeBob    Fry Cook          101
1    Patrick  Nap Expert          102
2  Squidward     Cashier          103
3      Sandy   Scientist          104

Performance Table:
   Employee_ID  Patties_Flipped  Complaints
0          101             500           0
1          102               2          50
2          103             300         200
3          105            1000           0
```

---

**SpongeBob gasps:**

> "Sandy has no performance record! And who’s **Employee 105**? A mystery fry cook?!"

**Patrick:**

> "Maybe it’s me on a good day!"

---

## Step 2: The 4 Types of Merges (Like Dance Moves!)

| Merge Type | Like a Party... | Keeps... |
| --- | --- | --- |
| `inner` | Only invited guests | Only matching IDs |
| `outer` | Everyone shows up | All people, even loners |
| `left` | Home team + guests | All from left table |
| `right` | Guest list rules | All from right table |

---

### 1\. **Inner Merge** – Only the Cool Kids (Matching IDs)

```python
inner_merge = pd.merge(employees_df, performance_df, on='Employee_ID', how='inner')
print("Inner Merge (Only Matches):")
print(inner_merge)
```

**Output:**

```plaintext
       Name         Job  Employee_ID  Patties_Flipped  Complaints
0  SpongeBob    Fry Cook          101             500           0
1    Patrick  Nap Expert          102               2          50
2  Squidward     Cashier          103             300         200
```

**SpongeBob:** "Yay! Only the ones in **both** lists!"  
**Sandy:** "Hey! Where’d I go?"  
**Mystery 105:** "And me?!"  
**Squidward:** "Finally, some peace."

---

### 2\. **Outer Merge** – Everyone’s Invited (Even Strangers!)

```python
outer_merge = pd.merge(employees_df, performance_df, on='Employee_ID', how='outer')
print("Outer Merge (Everyone!):")
print(outer_merge)
```

**Output:**

```plaintext
       Name         Job  Employee_ID  Patties_Flipped  Complaints
0  SpongeBob    Fry Cook          101           500.0         0.0
1    Patrick  Nap Expert          102             2.0        50.0
2  Squidward     Cashier          103           300.0       200.0
3      Sandy   Scientist          104             NaN         NaN
4        NaN         NaN          105          1000.0         0.0
```

**Patrick:** "Look! Mystery worker! And Sandy’s here but with no stats!"  
**Mr. Krabs:** "NaN means no data! But **1000 patties**? I want to meet 105!"

---

### 3\. **Left Merge** – Home Team First!

```python
left_merge = pd.merge(employees_df, performance_df, on='Employee_ID', how='left')
print("Left Merge (All Employees):")
print(left_merge)
```

**Output:**

```plaintext
       Name         Job  Employee_ID  Patties_Flipped  Complaints
0  SpongeBob    Fry Cook          101           500.0         0.0
1    Patrick  Nap Expert          102             2.0        50.0
2  Squidward     Cashier          103           300.0       200.0
3      Sandy   Scientist          104             NaN         NaN
```

**Sandy:** "I’m here! Even if I didn’t flip patties."  
**SpongeBob:** "Left merge = Keep **everyone from the left table**!"

---

### 4\. **Right Merge** – Guests Rule!

```python
right_merge = pd.merge(employees_df, performance_df, on='Employee_ID', how='right')
print("Right Merge (All Performers):")
print(right_merge)
```

**Output:**

```plaintext
       Name         Job  Employee_ID  Patties_Flipped  Complaints
0  SpongeBob    Fry Cook          101             500           0
1    Patrick  Nap Expert          102               2          50
2  Squidward     Cashier          103             300         200
3        NaN         NaN          105            1000           0
```

**Mr. Krabs:** "Who is 105?! They flipped **1000 patties**! Promote them! Fire Patrick!"

---

## Bonus: Merge on Different Column Names!

> What if one table uses `ID`, the other uses `Emp_ID`?

```python
# Rename for demo
perf2 = performance_df.rename(columns={'Employee_ID': 'Emp_ID'})

merged_diff = pd.merge(employees_df, perf2, left_on='Employee_ID', right_on='Emp_ID', how='inner')
print(merged_diff)
```

Works the same! Just tell Pandas which columns to match.

---

## Pro Tip: Check for Duplicates!

```python
# Uh oh! Two SpongeBobs?
employees_dup = pd.DataFrame({
    'Name': ['SpongeBob', 'SpongeBob'], 
    'Employee_ID': [101, 101]
})

# Merge will duplicate rows!
```

**Squidward:** "Never merge without checking uniqueness! Use `.duplicated()` or set index."

---

## Final Cheat Sheet (Print & Stick on Fridge!)

```python
pd.merge(df1, df2, on='key', how='inner')   # Only matches
pd.merge(df1, df2, on='key', how='outer')   # Everyone
pd.merge(df1, df2, on='key', how='left')    # Keep all from df1
pd.merge(df1, df2, on='key', how='right')   # Keep all from df2
```

---

## Your Turn! Mini Challenge

**Make two DataFrames:**

1. `customers`: Name, Favorite\_Food
    
2. `orders`: Name, Item\_Bought, Price
    

**Merge them** to see:

* Who ordered what?
    
* Who hasn’t ordered? (`left` on customers)
    
* All orders, even from unknown people? (`outer`)
    

---

**SpongeBob jumps up:**

> "Merging is like a **group hug with data**! Now we know who’s flipping patties, who’s napping, and who’s secretly a Krusty Krab superstar!"

**Patrick:**

> "Can we merge nap times next?"

**Mr. Krabs:**

> "Only if it makes money!"

---

**You’re now a Pandas Merge Master!**  
Try it in your Jupyter Notebook. Next adventure: **Grouping & Pivot Tables** with Plankton trying to steal the formula using `.groupby()`!

# **Pandas GroupBy: Plankton’s Evil Data Heist!**

*Starring SpongeBob, Patrick, Squidward, Mr. Krabs… and* ***PLANKTON*** *as the data villain!*

---

**Scene: Chum Bucket – 3 AM**  
*Plankton sneaks into the Krusty Krab database with a tiny USB stick shaped like a pickle.*

> **Plankton (cackling):**  
> "With **GroupBy**, I’ll group all Krabby Patty sales by **day**, **hour**, and **employee**! Then I’ll find the **weakest hour** to steal the formula! MUHAHA!"

**SpongeBob bursts in with a laptop:**

> "Not so fast, Plankton! We’ll use **GroupBy + Visualization** to **protect the recipe** with **beautiful charts**!"

---

Let’s learn **Pandas GroupBy** with **funny examples**, **real code**, and **cool visual diagrams** (ASCII + real plots)!

---

## Step 1: The Data – Krusty Krab Sales Log

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Set style for pretty plots
plt.style.use('seaborn')
sns.set_palette("husl")

# Krusty Krab Sales Data (one week)
data = {
    'Date': ['2025-10-27', '2025-10-27', '2025-10-27', '2025-10-28', '2025-10-28', '2025-10-29', '2025-10-29'],
    'Day': ['Monday', 'Monday', 'Monday', 'Tuesday', 'Tuesday', 'Wednesday', 'Wednesday'],
    'Hour': [12, 13, 18, 12, 19, 13, 20],
    'Employee': ['SpongeBob', 'Squidward', 'SpongeBob', 'SpongeBob', 'Squidward', 'SpongeBob', 'Squidward'],
    'Patties_Sold': [50, 20, 60, 55, 30, 70, 25],
    'Revenue': [250, 100, 300, 275, 150, 350, 125]
}

df = pd.DataFrame(data)
df['Date'] = pd.to_datetime(df['Date'])
print(df)
```

**Output:**

```plaintext
        Date        Day  Hour   Employee  Patties_Sold  Revenue
0 2025-10-27    Monday    12  SpongeBob            50      250
1 2025-10-27    Monday    13   Squidward            20      100
2 2025-10-27    Monday    18  SpongeBob            60      300
3 2025-10-28   Tuesday    12  SpongeBob            55      275
4 2025-10-28   Tuesday    19   Squidward            30      150
5 2025-10-29 Wednesday    13  SpongeBob            70      350
6 2025-10-29 Wednesday    20   Squidward            25      125
```

---

## Step 2: What is **GroupBy**?

> **SpongeBob:**  
> "GroupBy is like sorting jellyfish by **color**, then counting how many in each group!"

> **Plankton (whispering):**  
> "Or grouping sales by **hour** to find when guards are sleepy…"

---

### **GroupBy = Split → Apply → Combine**

```plaintext
┌────────────────────┐
│     Original DF    │
├────────────────────┤
│ Date | Hour | Emp  │
│ Mon  | 12   | SB   │
│ Mon  | 13   | SQ   │
│ ...                │
└────────────────────┘

       ▼ SPLIT ▼
┌───────┐  ┌───────┐  ┌───────┐
│ Mon   │  │ Tue   │  │ Wed   │
└───────┘  └───────┘  └───────┘

       ▼ APPLY (e.g. sum) ▼
┌───────┐  ┌───────┐  ┌───────┐
│ 130   │  │ 85    │  │ 95    │
└───────┘  └───────┘  └───────┘

       ▼ COMBINE ▼
┌────────────────────┐
│ Day  | Total Sold   │
│ Mon  | 130          │
│ Tue  | 85           │
│ Wed  | 95           │
└────────────────────┘
```

---

## Step 3: GroupBy in Action – Plankton’s Plans Foiled!

---

### **1\. Total Patties Sold Per Day**

```python
daily_sales = df.groupby('Day')['Patties_Sold'].sum().reset_index()
print(daily_sales)
```

**Output:**

```plaintext
         Day  Patties_Sold
0    Monday           130
1   Tuesday            85
2 Wednesday            95
```

**Plankton:** "Monday is busiest! I’ll strike on **Tuesday at 7 PM**!"

---

### **2\. Average Revenue Per Employee**

```python
emp_perf = df.groupby('Employee').agg({
    'Patties_Sold': 'mean',
    'Revenue': 'sum'
}).round(2)
print(emp_perf)
```

**Output:**

```plaintext
           Patties_Sold  Revenue
Employee                        
SpongeBob          58.75     1175
Squidward          25.00      375
```

**SpongeBob flexes:** "I’m the **Patty King**!"  
**Squidward:** "I’m the **Nap King**."

---

### **3\. Busiest Hour? (Plankton’s Target!)**

```python
hourly = df.groupby('Hour')['Patties_Sold'].sum().reset_index()
print(hourly)
```

**Output:**

```plaintext
   Hour  Patties_Sold
0    12           105
1    13            90
2    18            60
3    19            30
4    20            25
```

**Plankton:** "12 PM and 1 PM are chaos! I’ll sneak in at **8 PM**!"

---

## Step 4: **Visual Diagrams** – Catch Plankton with Charts!

---

### **Bar Chart: Sales by Day**

```python
plt.figure(figsize=(8,5))
bars = plt.bar(daily_sales['Day'], daily_sales['Patties_Sold'], color=['#ff9999','#66b3ff','#99ff99'])
plt.title('Krabby Patties Sold Per Day', fontsize=16, fontweight='bold')
plt.xlabel('Day')
plt.ylabel('Patties Sold')
plt.ylim(0, 150)

# Add labels on bars
for bar in bars:
    height = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, height + 5,
             f'{int(height)}', ha='center', fontweight='bold')

plt.tight_layout()
plt.show()
```

**ASCII Preview:**

```plaintext
Patties Sold Per Day
150 |                                  
100 |           ████                  
 50 |  ████     ████     ████         
  0 |  ████     ████     ████         
     Mon      Tue      Wed
        130     85       95
```

---

### **Line Chart: Hourly Traffic (Plankton’s Map!)**

```python
plt.figure(figsize=(9,5))
plt.plot(hourly['Hour'], hourly['Patties_Sold'], marker='o', linewidth=3, markersize=8, color='purple')
plt.title('Patties Sold by Hour – Plankton’s Danger Zone!', fontsize=16, fontweight='bold')
plt.xlabel('Hour (24h)')
plt.ylabel('Patties Sold')
plt.grid(True, alpha=0.3)

# Highlight danger zone
plt.axvspan(18, 20, color='red', alpha=0.2, label='Plankton Target Zone')
plt.legend()
plt.tight_layout()
plt.show()
```

**ASCII Preview:**

```plaintext
     105  o
          |
     90   o
          |
     60      o
          |
30-40        o     o
          |
     0   12 13 18 19 20  → Hour
         [======PLANKTON ZONE======]
```

---

### **Heatmap: Employee vs Hour (Spy Grid!)**

```python
pivot = df.pivot_table(values='Patties_Sold', index='Employee', columns='Hour', aggfunc='sum', fill_value=0)
plt.figure(figsize=(8,4))
sns.heatmap(pivot, annot=True, cmap="YlGnBu", fmt='d', linewidths=.5)
plt.title('Employee Heatmap: Who Works When?', fontsize=16)
plt.xlabel('Hour')
plt.ylabel('Employee')
plt.tight_layout()
plt.show()
```

**ASCII Heatmap:**

```plaintext
Employee     | 12  13  18  19  20
-------------|------------------
SpongeBob    | 50  70  60   0   0   ← SUPERSTAR!
Squidward    |  0  20   0  30  25
```

**SpongeBob:** "I’m in **blue** — that means **hot**!"  
**Plankton:** "SpongeBob at **1 PM** = 70 patties! I’ll avoid him!"

---

## Step 5: Multi-Level GroupBy – Plankton’s Final Plan

```python
multi = df.groupby(['Day', 'Employee'])['Patties_Sold'].sum().unstack(fill_value=0)
print(multi)
```

**Output:**

```plaintext
Employee   SpongeBob  Squidward
Day                           
Monday            110         20
Tuesday            55         30
Wednesday          70         25
```

**Plankton:** "Monday Squidward shift = only **20 patties**! That’s my **in**!"

---

## Step 6: Catch Plankton with **Alerts**!

```python
# Find low-performance shifts
low_shifts = df[df['Patties_Sold'] < 30]
print("PLANKTON ALERT! Low Activity Shifts:")
print(low_shifts[['Day', 'Hour', 'Employee', 'Patties_Sold']])
```

**Output:**

```plaintext
PLANKTON ALERT! Low Activity Shifts:
        Day  Hour   Employee  Patties_Sold
1    Monday    13   Squidward            20
4   Tuesday    19   Squidward            30
6 Wednesday    20   Squidward            25
```

**Mr. Krabs:** "SQUIDWARD! You’re fired… unless you guard the formula tonight!"

---

## Final Cheat Sheet (Stick on Krusty Krab Wall!)

```python
df.groupby('column').agg({'col2': 'sum'})      # Basic
df.groupby(['A','B']).size()                   # Count per group
df.groupby('col').mean().reset_index()         # Clean output
pivot = df.pivot_table(values='X', index='Y', columns='Z')
```

---

## Your Mission: **Stop Plankton!**

1. **Add a new column**: `Shift = 'Lunch' if Hour < 15 else 'Dinner'`
    
2. **Group by** `Shift` and `Employee` → Who sells more at dinner?
    
3. **Plot a pie chart**: % of total sales by employee
    
4. **Highlight Plankton’s weakest hour in red**
    

---

**SpongeBob salutes:**

> "With **GroupBy + Charts**, we turned data into a **security system**!"

**Plankton (trapped in a bar chart):**

> "CURSE YOU, PANDAS VISUALIZATION!"

**Patrick:**

> "Can we group ice cream flavors now?"

---

**You’re now a GroupBy Guardian!**  
Next: **Pivot Tables with Gary the Snail** (meow = melt, pivot, stack!)

# **Pandas Pivot Tables with Gary the Snail!**

*Meow! (That means: “Let’s reshape data like a pro!”)*

---

**Scene: SpongeBob’s Pineapple House – Data Science Lab**  
*Gary the Snail slowly slides in, leaving a trail of* ***structured data****. He’s wearing tiny glasses and holding a* ***mini laptop****.*

> **Gary (meow):**  
> *“Meeeow… pivot… meow… reshape… meow.”*  
> *(Translation: “Pivot tables let you twist and turn data like a Rubik’s cube made of Krabby Patties!”)*

**SpongeBob cheers:**

> "Gary’s here to teach us **pivot tables**! He’s the **slow but steady** data wizard!"

**Patrick drools:**

> "Can we pivot into ice cream?"

**Squidward sighs:**

> "Pivot tables = **reshape** wide data into tall, or tall into wide. Like folding laundry… but useful."

---

Let’s learn **Pivot Tables** with **Gary’s Snail Trail Data**, **funny examples**, **real code**, and **awesome visual diagrams**!

---

## Step 1: Gary’s Snail Trail Log (The Raw Data)

Gary records his **snail adventures** every day: where he went, what he ate, and how slow he was.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Gary's Adventure Log
data = {
    'Date': ['2025-10-27', '2025-10-27', '2025-10-28', '2025-10-28', '2025-10-29', '2025-10-29'],
    'Location': ['Pineapple', 'Rock', 'Pineapple', 'Rock', 'Pineapple', 'Rock'],
    'Meal': ['Krabby Patty', 'Seaweed Salad', 'Krabby Patty', 'Seaweed Salad', 'Krabby Patty', 'Seaweed Salad'],
    'Speed_cm_per_min': [2.1, 1.8, 2.3, 1.9, 2.0, 1.7],
    'Happiness': [10, 6, 9, 7, 10, 5]  # Out of 10
}

df = pd.DataFrame(data)
df['Date'] = pd.to_datetime(df['Date'])
print(df)
```

**Output:**

```plaintext
        Date   Location          Meal  Speed_cm_per_min  Happiness
0 2025-10-27  Pineapple  Krabby Patty               2.1         10
1 2025-10-27       Rock  Seaweed Salad               1.8          6
2 2025-10-28  Pineapple  Krabby Patty               2.3          9
3 2025-10-28       Rock  Seaweed Salad               1.9          7
4 2025-10-29  Pineapple  Krabby Patty               2.0         10
5 2025-10-29       Rock  Seaweed Salad               1.7          5
```

---

## Step 2: What is a **Pivot Table**?

> **Gary (meow):**  
> *“Meeeow… long → wide… meow… wide → long… meow.”*  
> *(Translation: Pivot = rearrange data like reshaping clay!)*

---

### **Long vs Wide Format** – Gary’s Diagram!

```plaintext
LONG FORMAT (df)               WIDE FORMAT (pivot)
┌─────────────────┐          ┌────────────────────────┐
│ Date │ Loc │ Meal │          │ Meal       │ Krabby │ Salad │
│------├-----┼------│          │------------┼--------┼-------│
│ 10-27│ Pin │ KP   │  →→→→   │ Pineapple  │  2.1   │  -    │
│ 10-27│ Rock│ SS   │          │ Rock       │   -    │  1.8  │
│ 10-28│ Pin │ KP   │          └────────────────────────┘
│ ...                    │
└─────────────────┘
```

---

## Step 3: **Pivot** – Turn Long into Wide!

### **Goal:** Average speed per **Location** and **Meal**

```python
pivot_speed = df.pivot_table(
    values='Speed_cm_per_min', 
    index='Location', 
    columns='Meal', 
    aggfunc='mean'
).round(2)

print("Pivot Table: Speed by Location & Meal")
print(pivot_speed)
```

**Output:**

```plaintext
Meal         Krabby Patty  Seaweed Salad
Location                                
Pineapple            2.13            NaN
Rock                  NaN           1.80
```

**Gary (meow):**

> *"Meeeow! Pineapple + Krabby Patty =* ***2.13 cm/min****! Rock + Salad =* ***1.8****!"*

---

### **Visual: Heatmap of Gary’s Speed**

```python
plt.figure(figsize=(6,4))
sns.heatmap(pivot_speed, annot=True, cmap="Blues", fmt='.2f', linewidths=1, cbar_kws={'label': 'Speed (cm/min)'})
plt.title("Gary's Speed Heatmap", fontweight='bold')
plt.ylabel("Location")
plt.xlabel("Meal")
plt.tight_layout()
plt.show()
```

**ASCII Heatmap:**

```plaintext
Location │ Krabby Patty │ Seaweed Salad
─────────┼──────────────┼──────────────
Pineapple│     2.13     │     (empty)
Rock     │   (empty)    │     1.80
```

**Gary glows blue at Pineapple!**

---

## Step 4: **Melt** – Wide → Long (Gary’s Reverse Pivot!)

> **SpongeBob:**  
> "What if we want to **un-pivot**? Like turning a pizza back into dough?"

> **Gary (meow):**  
> *"Meeeow…* `pd.melt()`… meow."

```python
# Make a wide table first
wide = df.pivot_table(values='Happiness', index='Date', columns='Location', aggfunc='mean')
print("Wide Table:")
print(wide)

# Melt it back to long!
long = wide.reset_index().melt(id_vars='Date', value_vars=['Pineapple', 'Rock'], 
                               var_name='Location', value_name='Happiness')
print("\nMelted Back to Long:")
print(long.dropna())
```

**Output:**

```plaintext
Wide Table:
Location    Pineapple  Rock
Date                       
2025-10-27       10.0   6.0
2025-10-28        9.0   7.0
2025-10-29       10.0   5.0

Melted Back to Long:
        Date   Location  Happiness
0 2025-10-27  Pineapple       10.0
1 2025-10-28  Pineapple        9.0
2 2025-10-29  Pineapple       10.0
3 2025-10-27       Rock        6.0
4 2025-10-28       Rock        7.0
5 2025-10-29       Rock        5.0
```

**Gary slides in a circle:**

> *"Meeeow… wide → long… long → wide… meow."*

---

## Step 5: **Multi-Level Pivot** – Gary’s Full Report!

### **Happiness by Date, Location, and Meal**

```python
pivot_full = df.pivot_table(
    values='Happiness',
    index=['Date', 'Location'],
    columns='Meal',
    aggfunc='mean'
)

print(pivot_full)
```

**Output:**

```plaintext
Meal                 Krabby Patty  Seaweed Salad
Date       Location                             
2025-10-27 Pineapple           10.0            NaN
           Rock                  NaN            6.0
2025-10-28 Pineapple            9.0            NaN
           Rock                  NaN            7.0
2025-10-29 Pineapple           10.0            NaN
           Rock                  NaN            5.0
```

---

### **Bar Plot: Gary’s Happiness Over Time**

```python
# Reset for plotting
plot_df = df.groupby(['Date', 'Location'])['Happiness'].mean().reset_index()

plt.figure(figsize=(10,5))
sns.barplot(data=plot_df, x='Date', y='Happiness', hue='Location', palette=['#ff9999', '#66b3ff'])
plt.title("Gary's Happiness: Pineapple vs Rock", fontweight='bold')
plt.xticks(rotation=45)
plt.ylabel("Happiness (out of 10)")
plt.legend(title="Location")
plt.tight_layout()
plt.show()
```

**ASCII Bar Chart:**

```plaintext
Happiness
10 |  ████       ████
 9 |  ████       ████
 8 |  
 7 |             ████
 6 |       ████
 5 |                   ████
   +-----------------------
     10-27  10-28  10-29  → Date
     [Pineapple]  [Rock]
```

**Gary loves Pineapple every day!**

---

## Step 6: **Stack & Unstack** – Gary’s Magic Tricks!

```python
# Stack: columns → index
stacked = pivot_speed.stack()
print("Stacked (columns become index):")
print(stacked)

# Unstack: index → columns
unstacked = stacked.unstack()
print("\nUnstacked (back to wide):")
print(unstacked)
```

**Gary spins in a shell:**

> *"Meeeow… stack… unstack… meow."*

---

## Step 7: **Pivot with Multiple Aggregations**

```python
multi_agg = df.pivot_table(
    values=['Speed_cm_per_min', 'Happiness'],
    index='Location',
    columns='Meal',
    aggfunc={'Speed_cm_per_min': 'mean', 'Happiness': 'max'}
)
print(multi_agg)
```

---

## Final Cheat Sheet (Gary’s Shell Etching)

```python
# PIVOT: Long → Wide
df.pivot_table(values='X', index='A', columns='B', aggfunc='mean')

# MELT: Wide → Long
pd.melt(df_wide, id_vars=['Date'], value_vars=['A','B'])

# STACK / UNSTACK
df_stacked = df_wide.stack()
df_wide = df_stacked.unstack()
```

---

## Your Mission: **Gary’s Data Challenge!**

1. **Pivot** Gary’s data to show **average speed** by **Date** (index) and **Meal** (columns)
    
2. **Melt** it back and remove NaN
    
3. **Plot** a line chart of Gary’s speed over time, colored by **Location**
    
4. **Bonus:** Add a column `Mood = 'Happy' if Happiness >= 8 else 'Grumpy'` and pivot by mood!
    

---

**Gary (meow):**

> *"Meeeow… you did it… meow… data master… meow."*  
> *(Translation: “You’re now a pivot table ninja!”)*

**SpongeBob hugs Gary:**

> "Thanks, Gary! You turned messy data into a **snail-shaped masterpiece**!"

**Patrick:**

> "Can we pivot into a nap now?"

---

**You’re a Pivot Table Pro!**  
Next adventure: **Time Series with Sandy Cheeks** (resampling, rolling averages, and rocket-powered forecasts!)

# **Pandas Time Series with Sandy Cheeks!**

*“Yee-haw! Let’s wrangle time like a Texas tornado!”*

---

**Scene: Sandy’s Treedome – High-Tech Lab**  
*Sandy Cheeks straps on her* ***rocket boots*** *and plugs in a* ***supercomputer****. A giant screen shows a* ***wiggly line of Krabby Patty sales over time****.*

> **Sandy (Texas accent):**  
> "Howdy, y’all! Time series is like **trackin’ a stampede** — you gotta know **when** the cows are comin’, **how fast**, and **when to dodge**!  
> We’ll use **Pandas** to **resample**, **roll**, and **forecast** like true data wranglers!"

**SpongeBob bounces:**

> "Yay! Time travel with data!"

**Patrick:**

> "Can we go back to nap time?"

**Squidward:**

> "Finally, something *useful* — I want to know when the lunch rush ends so I can nap."

---

Let’s ride into **Time Series Land** with **Sandy’s Krusty Krab Sales Data**, **real code**, **funny examples**, and **rocket-powered visual diagrams**!

---

## Step 1: The Data – Krusty Krab Sales Over 2 Weeks

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Set style
plt.style.use('seaborn-v0_8')
sns.set_palette("rocket")

# Generate 2 weeks of hourly sales (Oct 27 - Nov 9, 2025)
dates = pd.date_range('2025-10-27 08:00', '2025-11-09 22:00', freq='H')
np.random.seed(42)
sales = 20 + 50 * np.sin(np.pi * (np.arange(len(dates)) % 24) / 12)  # Daily pattern
sales += np.random.normal(0, 15, len(dates))  # Noise
sales = np.clip(sales, 0, None).astype(int)

df = pd.DataFrame({
    'timestamp': dates,
    'sales': sales,
    'day_of_week': dates.day_name(),
    'hour': dates.hour
})
df = df.set_index('timestamp')

print(df.head(10))
```

**Sample Output:**

```plaintext
                     sales day_of_week  hour
timestamp                                    
2025-10-27 08:00:00     23      Monday     8
2025-10-27 09:00:00     38      Monday     9
2025-10-27 10:00:00     62      Monday    10
2025-10-27 11:00:00     88      Monday    11
2025-10-27 12:00:00    105      Monday    12
...
```

---

## Step 2: What is **Time Series**?

> **Sandy:**  
> "A time series is data with a **timestamp** — like a **movie of sales**, not just a photo!"

---

### **Time Series Anatomy** – Sandy’s Diagram!

```plaintext
┌────────────────────────────────────────────────────┐
│              Krusty Krab Sales Over Time           │
│                                                    │
│     ▲ Sales                                        │
│ 120 │                  ████                        │
│ 100 │             ████    ████                     │
│  80 │        ████          ████                  │
│  60 │   ████                ████                 │
│  40 │ ███                   ████                 │
│  20 │██                      ████               │
│   0 └─────────────────────────────────────────────► Time
│     Mon Tue Wed Thu Fri Sat Sun Mon Tue Wed Thu Fri │
└────────────────────────────────────────────────────┘
       ↑           ↑           ↑
    Morning    Lunch Rush   Evening
```

---

## Step 3: **Resampling** – Zoom In or Out!

> **Sandy:**  
> "Resampling = changin’ the **frequency** — like switchin’ from **hourly** to **daily**!"

---

### **1\. Daily Total Sales**

```python
daily_sales = df['sales'].resample('D').sum()
print(daily_sales.head())
```

**Output:**

```plaintext
timestamp
2025-10-27    987
2025-10-28    842
2025-10-29    920
...
Freq: D, Name: sales, dtype: int64
```

---

### **2\. Weekly Average**

```python
weekly_avg = df['sales'].resample('W').mean().round(1)
print(weekly_avg)
```

---

### **Visual: Resampled Sales**

```python
fig, ax = plt.subplots(2, 1, figsize=(12, 8), sharex=True)

# Hourly
df['sales'].plot(ax=ax[0], title='Hourly Sales (Raw)', alpha=0.7, linewidth=0.8)
ax[0].set_ylabel('Sales')

# Daily
daily_sales.plot(ax=ax[1], title='Daily Total Sales (Resampled)', color='purple', marker='o')
ax[1].set_ylabel('Total Sales')
ax[1].set_xlabel('Date')

plt.tight_layout()
plt.show()
```

**ASCII Preview:**

```plaintext
Hourly:  ▁▂▃▅▆██▇▆▅▃▂▁▁▂▃▅▆██▇▆▅▃...
Daily:        ▇▅▆▇▆▅▇▆▅▇▆...
```

---

## Step 4: **Rolling Windows** – Smooth the Ride!

> **Sandy:**  
> "Rolling = **glidin’ average** — like a tumbleweed rollin’ over bumps!"

---

### **3-Day Rolling Average**

```python
rolling_3d = daily_sales.rolling(window=3).mean()
rolling_7d = daily_sales.rolling(window=7).mean()

plt.figure(figsize=(12, 5))
daily_sales.plot(label='Daily', alpha=0.5)
rolling_3d.plot(label='3-Day Rolling', linewidth=2)
rolling_7d.plot(label='7-Day Rolling', linewidth=3)
plt.title('Krusty Krab Sales: Raw vs Smoothed', fontweight='bold')
plt.legend()
plt.ylabel('Sales')
plt.tight_layout()
plt.show()
```

**Sandy:** "See? The **7-day roll** shows the **trend** — sales are climbin’!"

---

## Step 5: **Time-Based Indexing & Slicing**

```python
# Lunch rush: 11 AM - 2 PM
lunch = df.between_time('11:00', '14:00')
print(f"Lunch average: {lunch['sales'].mean():.1f} patties/hour")

# Weekends only
weekends = df[df.index.day_name().isin(['Saturday', 'Sunday'])]
print(f"Weekend total: {weekends['sales'].sum()} patties")
```

---

## Step 6: **Seasonality** – Daily Pattern!

```python
# Average sales by hour
hourly_pattern = df.groupby('hour')['sales'].mean()

plt.figure(figsize=(10, 5))
hourly_pattern.plot(kind='bar', color='orange', edgecolor='black')
plt.title('Average Sales by Hour – The Daily Stampede!', fontweight='bold')
plt.xlabel('Hour')
plt.ylabel('Avg Sales')
plt.axvspan(10.5, 13.5, color='red', alpha=0.2, label='Lunch Rush')
plt.legend()
plt.tight_layout()
plt.show()
```

**ASCII Bar Chart:**

```plaintext
Avg Sales by Hour
100 |           ████
 80 |       ████    ████
 60 |   ████          ████
 40 | ███               ████
 20 |██                 ████
  0 +--------------------→
     8  10  12  14  16  18  20
         [LUNCH RUSH]
```

---

## Step 7: **Forecasting** – Sandy’s Rocket Prediction!

```python
# Simple: Use 7-day rolling mean as forecast
forecast = daily_sales.copy()
forecast = forecast.rolling(7).mean().shift(1)  # Yesterday's trend

# Plot last 10 days + forecast
recent = daily_sales[-10:]
pred = forecast[-10:]

plt.figure(figsize=(10, 5))
recent.plot(label='Actual', marker='o')
pred.plot(label='7-Day Forecast', marker='x', linestyle='--', linewidth=2)
plt.title('Krusty Krab Sales Forecast – Sandy’s Crystal Ball!', fontweight='bold')
plt.legend()
plt.ylabel('Daily Sales')
plt.tight_layout()
plt.show()
```

**Sandy:** "If we keep the trend, **tomorrow = ~920 patties**! Stock up!"

---

## Step 8: **Anomaly Detection** – Catch the Glitch!

```python
# Z-score: how far from rolling mean?
df['z_score'] = (df['sales'] - df['sales'].rolling(24).mean()) / df['sales'].rolling(24).std()
anomalies = df[abs(df['z_score']) > 2.5]

plt.figure(figsize=(12, 4))
df['sales'].plot(alpha=0.7, label='Sales')
plt.scatter(anomalies.index, anomalies['sales'], color='red', s=50, label='Anomaly!')
plt.title('Anomaly Detected! Plankton Strike?', fontweight='bold')
plt.legend()
plt.tight_layout()
plt.show()
```

**SpongeBob:** "A sales drop at 3 AM? That’s **Plankton o’clock**!"

---

## Final Cheat Sheet (Sandy’s Lasso)

```python
df.resample('D').sum()           # Daily total
df.rolling(7).mean()             # 7-day average
df.between_time('11:00','14:00') # Time slice
df.groupby(df.index.hour).mean() # By hour
df.shift(1)                      # Yesterday
df.pct_change()                  # % change
```

---

## Your Mission: **Sandy’s Time Wrangling Challenge!**

1. **Resample** to **business hours only** (9 AM – 5 PM)
    
2. **Plot** a **7-day rolling** with **shaded weekends**
    
3. **Find** the **busiest hour of the week** (e.g., “Friday 12 PM”)
    
4. **Forecast** next 3 days using **rolling mean**
    
5. **Bonus:** Add a column `is_lunch_rush = True` if hour in \[11,12,13\]
    

---

**Sandy tips her helmet:**

> "Yee-haw! You just **tamed time** like a wild bronco!  
> With **resampling**, **rolling**, and **forecasting**, the Krusty Krab is **Plankton-proof**!"

**Gary (meow):**

> *"Meeeow… time… series… meow."*  
> *(Translation: “Next: Machine Learning with Mermaid Man!”)*

---

**You’re a Time Series Trailblazer!**