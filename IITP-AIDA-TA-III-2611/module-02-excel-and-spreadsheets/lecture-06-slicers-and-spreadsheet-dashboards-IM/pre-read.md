## <span style="color:#2F7DDE">Slicers and Spreadsheet Dashboards</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Slicers and Spreadsheet Dashboards"]
  Q["<b>The Big Question</b><br/><i>How can one sheet show key numbers that react when we pick a filter?</i>"]
  CV["<b>Course use case</b><br/>An insurance dashboard where the top city changed from Delhi to Mumbai when Health was picked"]
  RL["<b>Real-world example</b><br/>A neighbourhood bakery order board with a button per item type and red late orders"]

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

Have you ever wondered how a bakery board can change from all orders to cakes only with one tap?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**List**</span> the 3 key numbers the bakery owner wants on one sheet.
- <span style="color:#D9660B">**Describe**</span> what a filter button does to a summary table and its chart.
- <span style="color:#D9660B">**Interpret**</span> a red row on the order board.
- <span style="color:#D9660B">**Examine**</span> why one total ignores the button while another follows it.
- <span style="color:#D9660B">**Build**</span> a rule that colours every late order.
- <span style="color:#D9660B">**Check**</span> a cell that shows a broken value.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> slicer, pivot chart, conditional formatting (flag rows), KPI dashboard (key numbers on one sheet), fixing #VALUE! #DIV/0! and circular references.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Rekha runs a bakery. She keeps one order sheet for cakes, bread and cookies. She wants a board that shows total money, the top item and late orders. She taps a button for cakes. The chart changes, but the total does not. One cell shows an error because there were no cookie orders.

A <span style="color:#D9660B">**dashboard**</span> means one sheet that shows the key numbers of a business at a glance.

In this course, you will build a sheet whose numbers move together and show no broken cells.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did the chart change when Rekha tapped Cakes, while the total stayed the same?

---

### <span style="color:#2F7DDE">Bakery Board Puzzle</span>

Here are 4 orders from Rekha's sheet.

| Order | Item | Money | Status |
|:----------:|:----------:|:----------:|:----------:|
| 1 | Cake | Rs 900 | Delivered |
| 2 | Bread | Rs 120 | Late |
| 3 | Cake | Rs 1,100 | Delivered |
| 4 | Cookies | Rs 0 | Late |

<span style="color:#D9660B">**What you want to happen:**</span>

- Every late order is coloured red.
- The total and the chart both follow the button.
- A missing item shows 'n/a' and not an error.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What does a rate of money per order show when there are 0 orders?
> - Which numbers should follow the button?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which orders in the table are late?**
Hint: Read the Status column.

**2. The total for Cakes alone is how much?**
Hint: Add the two cake rows.

**3. The rate for cookies divides by 0 orders. What should the cell say?**
Hint: Choose a word that says why there is no number.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**Which numbers on a dashboard must move when we pick a filter?**</span>
>
> Which cell on Rekha's board would you test first for a broken value?
