## <span style="color:#2F7DDE">Text and Dates with Calculated Columns</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Text and Dates with Calculated Columns"]
  Q["<b>The Big Question</b><br/><i>How do we tidy messy text, count days and spot empty cells in a table?</i>"]
  CV["<b>Course use case</b><br/>A booking table of 120 rows where 19 jobs had no completion date and names carried stray spaces"]
  RL["<b>Real-world example</b><br/>A laundry pickup register with messy names, pickup dates and missing return dates"]

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

Have you ever wondered how a laundry shop knows which bags are still waiting after 5 days?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Name**</span> the day, month and year written on a pickup slip.
- <span style="color:#D9660B">**Identify**</span> the slips that have no return date yet.
- <span style="color:#D9660B">**Apply**</span> text fixes to names written in odd capitals and with extra spaces.
- <span style="color:#D9660B">**Calculate**</span> the price after a 10% discount on a Rs 400 order, and label the new column.
- <span style="color:#D9660B">**Determine**</span> the days between the pickup date and the return date.
- <span style="color:#D9660B">**Use**</span> a rounding rule to show a price in whole rupees.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> text functions, date parts, date difference, calculated columns with AS, ROUND and CAST, missing values.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Latha runs a laundry shop. Customers write their own names on the slips, so one reads '  mEERA  nair'. Each slip has a pickup date and a return date. Three bags have no return date yet. Latha wants a clean list of waiting bags and the price after discount.

A <span style="color:#D9660B">**calculated column**</span> means a new column worked out from other columns, such as price minus discount.

In this course, you will tidy and calculate columns in a query before sharing a report.

> <span style="color:#2F7DDE">**Think about it:**</span> Which slips would Latha miss if she only looked at bags that have a return date?

---

### <span style="color:#2F7DDE">The Laundry Pickup Register Puzzle</span>

Here are three slips from Latha's register.

| Name on slip | Pickup | Return | Price |
|:----------:|:----------:|:----------:|:----------:|
|   mEERA  nair | 2 March | 5 March | Rs 400 |
| ASHA rao | 28 February | 1 March | Rs 250 |
| dev kapoor  | 10 March | No return date | Rs 320 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Latha shows each name with a capital letter and no extra spaces.
- Latha counts the days each bag stayed in the shop.
- Latha lists every bag with an empty return date.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - How would Latha count the days from 28 February to 1 March?
> - What should Latha write for a bag with no return date?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The slip says 10% off Rs 400. What is the price after the discount?**
Hint: Work out the discount first, then subtract.

**2. A bag came in on 28 February and left on 1 March. Does the month change the day count?**
Hint: Count the days of February.

**3. Dev's slip has no return date. Is its return date equal to zero or is it empty?**
Hint: Think of what 'nothing written' means.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can we turn a messy register into a clean, calculated list?**</span>
>
> Which step would you do first: tidy names, count days or find empty cells?
