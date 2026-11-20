## <span style="color:#2F7DDE">Pivot Tables and Analysis</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Pivot Tables and Analysis"]
  Q["<b>The Big Question</b><br/><i>How do I turn a long pile of rows into one short, trusted summary?</i>"]
  CV["<b>Course use case</b><br/>Summarising 120 distributor orders worth Rs 1,423,800 into 4 regions with each share"]
  RL["<b>Real-world example</b><br/>A family's pile of grocery receipts totalled by shop"]

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

Have you ever wondered how a pile of receipts turns into one line that says where the money went?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Summarise**</span> a pile of 6 receipts into one line for each shop.
- <span style="color:#D9660B">**Predict**</span> what happens to a bar picture when one receipt changes.
- <span style="color:#D9660B">**Calculate**</span> each shop's share of a Rs 2,000 monthly spend.
- <span style="color:#D9660B">**Differentiate**</span> a tally by shop, by week and by size of bill.
- <span style="color:#D9660B">**Justify**</span> whether a task needs a tally or a value written on each receipt.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Build a pivot table, percent of total, group by date or number, pivot chart linked to the pivot, lookup or pivot.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Meera keeps the month's grocery receipts in a drawer. Her husband asks, "Which shop took most of our money?"

She spends an evening adding receipts shop by shop on a calculator. She misreads one receipt and gets a wrong total.

Next month she must do it all again, because nothing was saved.

A <span style="color:#D9660B">**pivot table**</span> means a small table that adds up a long list of rows into one line for each group.

In this course, you will build summary tables like this from files of 120 rows or more.

> <span style="color:#2F7DDE">**Think about it:**</span> What would let Meera redo the totals in seconds next month?

---

### <span style="color:#2F7DDE">The Grocery Receipts Puzzle</span>

Meera lists six receipts from the month.

| Receipt | Shop | Week | Amount |
|:----------:|:----------:|:----------:|:----------:|
| 1 | Kumar Stores | 1 | Rs 400 |
| 2 | Fresh Mart | 1 | Rs 700 |
| 3 | Kumar Stores | 2 | Rs 300 |
| 4 | Dairy Point | 2 | Rs 200 |
| 5 | Fresh Mart | 3 | Rs 300 |
| 6 | Kumar Stores | 4 | Rs 100 |

<span style="color:#D9660B">**What you want to happen:**</span>

- One line shows the total for each shop.
- Each line also shows its share of the month's spend.
- A bar picture follows the totals when a receipt changes.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which shop gets the biggest share of the Rs 2,000?
> - How would you total the receipts for each week instead?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Two receipts come from Fresh Mart. Which line of a summary holds them together?**
Hint: Think about the group they share.

**2. Fresh Mart's receipts add up to Rs 1,000 of the Rs 2,000 total. What share is that?**
Hint: Divide the shop's amount by the total.

**3. Meera wants each receipt to show its shop's phone number. Does she need a summary or a value on each receipt?**
Hint: Count the lines you expect in the answer.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**When do you want one line for each group, and when one value for each row?**</span>
>
> Which line of Meera's list would you check first to trust a summary?
