## <span style="color:#2F7DDE">Structuring and Validating Data Across Sheets</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Structuring and Validating Data Across Sheets"]
  Q["<b>The Big Question</b><br/><i>How can three sheets become one tidy table that stays clean?</i>"]
  CV["<b>Course use case</b><br/>Three city delivery sheets stacked into one table of 120 rows"]
  RL["<b>Real-world example</b><br/>A hostel mess with three block sheets, a meal dropdown and a bill category"]

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

Have you ever wondered how three hostel blocks can send one combined meal list without mistakes?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**List**</span> the 3 block sheets and the columns they share.
- <span style="color:#D9660B">**Explain**</span> why a meal dropdown stops the typo 'Vegg' from entering.
- <span style="color:#D9660B">**Classify**</span> each bill as Low, Medium or High with a rule on the amount.
- <span style="color:#D9660B">**Compare**</span> a sheet sorted by one column with a sheet sorted as whole rows.
- <span style="color:#D9660B">**Interpret**</span> a formula that gives Refund, Call or None.
- <span style="color:#D9660B">**Build**</span> one combined table from the three block sheets.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> split a column, dropdown validation, filter and sort, consolidate from other sheets, stack sheets into one table, IF function, nested IF formula, reading an unfamiliar nested formula.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Kiran runs the hostel mess. Block A, Block B and Block C each keep a sheet. Names sit in one cell, such as Asha Rao. A student typed Vegg as a meal. Someone sorted only the bill column, and the bills slid away from the names. Kiran needs one clean list by Friday.

A <span style="color:#D9660B">**dropdown**</span> means a cell that accepts only the values on a list.

In this course, you will combine tabs, lock entries and label rows with one formula.

> <span style="color:#2F7DDE">**Think about it:**</span> What happens to a bill when only its column is sorted?

---

### <span style="color:#2F7DDE">Hostel Mess Puzzle</span>

Here are 3 rows from Block A.

| Name | Meal | Bill |
|:----------:|:----------:|:----------:|
| Asha Rao | Veg | Rs 1,400 |
| Bilal Khan | Non-veg | Rs 2,300 |
| Chitra Iyer | Vegg | Rs 2,800 |

<span style="color:#D9660B">**What you want to happen:**</span>

- The meal column accepts only Veg, Non-veg or Jain.
- Each bill gets a label: Low, Medium or High.
- The three block sheets join into one list.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which row would a dropdown have blocked?
> - What should a blank bill be labelled?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Low is up to Rs 1,500 and Medium is up to Rs 2,500. Which label does Rs 2,300 get?**
Hint: Check the first limit, then the next.

**2. Names and bills are sorted as separate columns. What goes wrong?**
Hint: Think about which cells stay together.

**3. Three sheets have the same 3 columns. How do you place Block B under Block A?**
Hint: Think of stacking rows, not columns.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can three sheets and three typists keep one list intact?**</span>
>
> Which column in the mess sheet would you lock first?
