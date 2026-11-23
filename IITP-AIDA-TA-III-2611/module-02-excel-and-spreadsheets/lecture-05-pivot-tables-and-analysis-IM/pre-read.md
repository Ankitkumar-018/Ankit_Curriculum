## <span style="color:#2F7DDE">Pivot Tables and Analysis</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Pivot Tables and Analysis"]
  Q["<b>The Big Question</b><br/><i>How can one table sum up 140 rows, and what keeps it current?</i>"]
  CV["<b>Course use case</b><br/>A pizza chain where one pivot showed Indiranagar at 34.6 percent of Rs 1,07,428"]
  RL["<b>Real-world example</b><br/>A flower shop's weekly sales book summed by flower, with a share of the total"]

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

Have you ever wondered how a flower seller knows which flower earns the most without adding by hand?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Summarise**</span> the week's sales by flower in one small table.
- <span style="color:#D9660B">**Calculate**</span> the share of the total for each flower.
- <span style="color:#D9660B">**Compare**</span> a sum with an average when one big order is in the group.
- <span style="color:#D9660B">**Explain**</span> why a sale added below the table is missing from its totals.
- <span style="color:#D9660B">**Determine**</span> when you need a summary table and when you need a value on every row.
- <span style="color:#D9660B">**Plan**</span> a monthly view of the same sales book.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> build a pivot table, percent of total, group by date or number, pivot refresh and source range, lookup or pivot.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Geeta sells flowers. She notes every sale in a book: the flower, the day and the money. At the end of the week she wants the total for each flower. She adds by hand and takes an hour. A friend shows a summary table that does it in a second. On Saturday Geeta adds one more sale below the table, and the totals do not change.

A <span style="color:#D9660B">**pivot table**</span> means a summary table that groups rows and adds them up for you.

In this course, you will summarise rows into groups and check the total against the source.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did the totals stay the same after Geeta added a new sale?

---

### <span style="color:#2F7DDE">Flower Book Puzzle</span>

Here is part of Geeta's sales book.

| Flower | Day | Money |
|:----------:|:----------:|:----------:|
| Rose | Monday | Rs 300 |
| Jasmine | Monday | Rs 150 |
| Rose | Tuesday | Rs 450 |
| Marigold | Tuesday | Rs 100 |

<span style="color:#D9660B">**What you want to happen:**</span>

- One line per flower with its total.
- Each flower's share of the week's money.
- The new Saturday sale appears in the totals.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What is the share of roses if the four rows are the whole week?
> - What would a wedding order of Rs 8,000 do to an average?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The four rows add up to Rs 1,000. What share of the money did roses bring?**
Hint: Add the two rose rows first.

**2. Which is easier to read for a week of 300 sales: the book or a summary by flower?**
Hint: Think about the count of lines you must read.

**3. Geeta wants the same book grouped by month. What would she group?**
Hint: Look at the Day column.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can we sum a long list of rows and be sure no row was missed?**</span>
>
> Which total in Geeta's summary would you check against the book first?
