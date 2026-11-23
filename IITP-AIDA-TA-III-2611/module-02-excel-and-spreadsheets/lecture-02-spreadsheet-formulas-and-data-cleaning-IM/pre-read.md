## <span style="color:#2F7DDE">Spreadsheet Formulas and Data Cleaning</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Spreadsheet Formulas and Data Cleaning"]
  Q["<b>The Big Question</b><br/><i>How do we turn a messy sheet into numbers we can add and trust?</i>"]
  CV["<b>Course use case</b><br/>A store export where a price column added up to 0 and 8 orders were counted twice"]
  RL["<b>Real-world example</b><br/>A school bake sale sheet with spaces, price text and repeated rows"]

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

Have you ever wondered why a sheet adds up to 0 when every cell looks like a number?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> the 3 cells in the bake sale sheet that look like numbers and act like text.
- <span style="color:#D9660B">**Explain**</span> why 'Rs 15' cannot be added until the letters are removed.
- <span style="color:#D9660B">**Apply**</span> a clean-up so ' SAMOSA ' and 'samosa' match.
- <span style="color:#D9660B">**Calculate**</span> the sale value for each row and the total for the day.
- <span style="color:#D9660B">**Check**</span> which row is a repeat and should be kept once.
- <span style="color:#D9660B">**Design**</span> one formula that works when copied down 30 rows.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> formulas, absolute vs relative references, SUM AVERAGE COUNT MIN and MAX, TRIM PROPER and SUBSTITUTE, text to numbers and dates, remove duplicates.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Tara runs the school bake sale. She types each sale into a sheet. At the end she adds the price column and gets 0. One sale is listed twice. Two item names differ only by capital letters and spaces. The treasurer asks for the day's total, and Tara cannot give it.

A <span style="color:#D9660B">**formula**</span> means a rule you type in a cell that works out a value from other cells.

In this course, you will clean a sheet first and then build formulas on it.

> <span style="color:#2F7DDE">**Think about it:**</span> Why does a column of prices add up to 0?

---

### <span style="color:#2F7DDE">Bake Sale Puzzle</span>

Here are 4 rows from Tara's sheet.

| Sale | Item | Qty | Price |
|:----------:|:----------:|:----------:|:----------:|
| 1 | ' SAMOSA ' | 2 | Rs 15 |
| 2 | 'samosa' | 3 | Rs 15 |
| 3 | 'Brownie' | 1 | Rs 40 |
| 3 | 'Brownie' | 1 | Rs 40 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Both samosa rows carry the same clean name.
- Each price becomes a number.
- The repeated brownie sale counts once.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Does the day's total change if row 4 stays?
> - What should happen to the letters Rs in the price?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Row 1 is 2 samosas at Rs 15. What is the sale value?**
Hint: Multiply the quantity by the price.

**2. Row 4 repeats row 3. What does the day's total look like if both stay?**
Hint: Add both brownie rows.

**3. Tara copies a formula down 30 rows, and one cell must stay fixed. Which cell would that be?**
Hint: Think of a number that every row uses.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**What must we fix in a sheet before any formula can be trusted?**</span>
>
> Which row in Tara's sheet would you fix first?
