## <span style="color:#2F7DDE">Aggregation and GROUP BY</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Aggregation and GROUP BY"]
  Q["<b>The Big Question</b><br/><i>How do we turn 120 rows into a few honest numbers?</i>"]
  CV["<b>Course use case</b><br/>120 grocery sale lines summed per category, with 3 categories above Rs 7,000"]
  RL["<b>Real-world example</b><br/>A household expense notebook with 30 entries and totals per category"]

  CUR ==> Q
  Q ==>|&nbsp;Used in the course&nbsp;| CV
  Q ==>|&nbsp;Seen in real life&nbsp;| RL

  classDef currSes fill:#ffe0b2,stroke:#ef6c00,color:#4e342e,stroke-width:3px
  classDef ask fill:#e3f2fd,stroke:#1565c0,color:#0d47a1,stroke-width:3px
  classDef val fill:#e8f5e9,stroke:#2e7d32,color:#1b5e20

  class CUR currSes
  class Q ask
  class CV,RL val

  linkStyle default stroke-width:3px
```

---

### <span style="color:#2F7DDE">What You'll Learn</span>

Have you ever wondered how a family finds the total spent on vegetables from 30 scribbled entries?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Explain**</span> why counting all entries, entries with a shop note and different shops give 3 answers.
- <span style="color:#D9660B">**Calculate**</span> the total, average, smallest and largest of 30 expenses.
- <span style="color:#D9660B">**Determine**</span> the total spent on each category in the notebook.
- <span style="color:#D9660B">**Compare**</span> removing small expenses before totalling with removing small totals after totalling.
- <span style="color:#D9660B">**Trace**</span> the order in which the notebook reads one request, step by step.
- <span style="color:#D9660B">**Check**</span> why a request that mixes single entries with category totals is refused.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> COUNT, SUM, AVG, MIN, MAX, GROUP BY, HAVING, clause order.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Kavita keeps a notebook of the family's expenses for March. It has 30 entries, each with a category and an amount. Eighteen entries name a shop. Her husband asks, 'How often did we shop?' Kavita counts only the entries with a shop name. She says 18. The real count is 30.

A <span style="color:#D9660B">**total**</span> means the sum of all the entries in one group.

In this course, you will summarise rows of a table into counts, totals and averages per group.

> <span style="color:#2F7DDE">**Think about it:**</span> Which count would you give the family, and why?

---

### <span style="color:#2F7DDE">The Household Expense Notebook Puzzle</span>

Here are four entries from Kavita's notebook.

| Category | Amount | Shop name |
|:----------:|:----------:|:----------:|
| Vegetables | Rs 220 | Fresh Mart |
| Vegetables | Rs 140 | Not written |
| Travel | Rs 600 | Not written |
| Milk | Rs 90 | Dairy Point |

<span style="color:#D9660B">**What you want to happen:**</span>

- Kavita finds the total for each category.
- Kavita keeps only the categories above Rs 1,000.
- Kavita counts entries in a way that matches the question.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What does the count become if empty shop names are left out?
> - Would a category total change if Kavita first removed all entries below Rs 100?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The notebook has 30 entries and 12 have no shop name. How can you count all 30?**
Hint: Count the rows, not one filled column.

**2. Vegetables total Rs 1,400 across 5 entries. Is Rs 1,400 one entry or a group total?**
Hint: Think about the number of entries it combines.

**3. Kavita wants 'categories above Rs 1,000'. Should she filter entries or totals?**
Hint: Ask which numbers exist before and after adding.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do we summarise rows into one number per group and keep only the groups that matter?**</span>
>
> Which count would you trust for the family's shopping trips?
