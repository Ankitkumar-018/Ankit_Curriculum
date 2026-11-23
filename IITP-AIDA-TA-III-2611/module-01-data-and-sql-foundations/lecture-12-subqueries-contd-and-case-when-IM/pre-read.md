## <span style="color:#2F7DDE">Subqueries Contd and CASE WHEN</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Subqueries Contd and CASE WHEN"]
  Q["<b>The Big Question</b><br/><i>How can one question sit inside another, and how do labels and blanks stay honest?</i>"]
  CV["<b>Course use case</b><br/>A cinema report where 12 blank discounts hid Rs 2.83 lakh of ticket money"]
  RL["<b>Real-world example</b><br/>A school canteen price list with a blank discount cell, a zero-sale stall and three price tags"]

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

Have you ever wondered how a canteen board tags each snack as Costly, Fair or Cheap on its own?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> the 2 snacks priced above the canteen average of Rs 25.
- <span style="color:#D9660B">**Classify**</span> each of the 5 snacks as Costly, Fair or Cheap by its price.
- <span style="color:#D9660B">**Predict**</span> how blank discounts move the money total from Rs 1,900 to Rs 1,000.
- <span style="color:#D9660B">**Explain**</span> why Juice, with 0 sold, breaks a price-per-item sum.
- <span style="color:#D9660B">**Trace**</span> a total that runs without a warning and still shows the wrong money.
- <span style="color:#D9660B">**Check**</span> the total against a figure you already know, such as the cash box.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> subquery in WHERE, subquery in FROM, CASE WHEN and bucketing, COALESCE and NULLIF, join filter and aggregate in one query, fixing a query that runs but gives the wrong answer.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Meena runs the school canteen board. Each week she lists snacks, prices and counts sold. Last week the board said the canteen earned Rs 1,000. The cash box held Rs 1,900. Two snacks had a blank discount. The board skipped them without a word.

A <span style="color:#D9660B">**subquery**</span> means a question placed inside another question, so the first answer feeds the second.

In this course, you will place one query inside another and test each total against a figure you know.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did the board show Rs 1,000 when the cash box held Rs 1,900?

---

### <span style="color:#2F7DDE">Canteen Board Puzzle</span>

Here is part of Meena's board for one week.

| Snack | Price | Sold | Discount per item |
|:----------:|:----------:|:----------:|:----------:|
| Samosa | Rs 15 | 40 | Rs 0 |
| Sandwich | Rs 30 | 20 | Blank |
| Pasta | Rs 45 | 10 | Rs 5 |
| Juice | Rs 25 | 0 | Rs 0 |
| Biscuits | Rs 10 | 30 | Blank |

<span style="color:#D9660B">**What you want to happen:**</span>

- The board lists the snacks priced above the average price.
- Each snack gets a tag that matches its price.
- The money total counts every snack, even with a blank discount.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What should the board do with a blank in the discount column?
> - How do you work out a price per item for Juice, which sold 0?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The 5 prices add up to Rs 125. Which snacks cost more than the average?**
Hint: Divide the sum by 5 first.

**2. A blank discount is treated as Rs 0. What is the money for Sandwich, with 20 sold?**
Hint: Price minus discount, times the count sold.

**3. The board adds only the snacks with a filled discount. Which snacks are left out?**
Hint: Look at the Discount column.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**Which part of a board can you trust only after you check it against a figure you know?**</span>
>
> What would you test first on Meena's board before sending it to the principal?
