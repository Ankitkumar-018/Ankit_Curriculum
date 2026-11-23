## <span style="color:#2F7DDE">Relational Databases and SELECT Queries</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Relational Databases and SELECT Queries"]
  Q["<b>The Big Question</b><br/><i>How do we ask a table for exactly the rows and columns we want?</i>"]
  CV["<b>Course use case</b><br/>A used-car table of 120 listings filtered to petrol cars under Rs 4 lakh in two cities"]
  RL["<b>Real-world example</b><br/>A fruit seller's ledger of 120 fruits, filtered and sorted for one customer"]

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

Have you ever wondered how a shop owner finds every red fruit under Rs 80 in a long ledger?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Name**</span> the columns you want from a fruit ledger, such as fruit, colour and price.
- <span style="color:#D9660B">**Identify**</span> each different fruit colour once, with no repeats.
- <span style="color:#D9660B">**Describe**</span> how the ledger keeps one fruit in each row and one fact in each column.
- <span style="color:#D9660B">**Apply**</span> price, list, range and name tests to keep only the fruits a customer wants.
- <span style="color:#D9660B">**Design**</span> a rule for red fruits under Rs 80, or any green fruit, with brackets in the right place.
- <span style="color:#D9660B">**Write**</span> a sort that shows the cheapest fruit first and the freshest first when prices match.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> tables, schema, SELECT, DISTINCT, WHERE, AND OR NOT, IN, LIKE, BETWEEN, ORDER BY.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Nandini sells fruit at a market stall. Her ledger lists 120 fruits with colour, price per kg and arrival day. A customer asks for red fruits under Rs 80, or any green fruit. Nandini's helper reads the ledger and lists every red fruit and every green fruit. The customer sees costly red fruit and feels cheated.

A <span style="color:#D9660B">**table**</span> means a grid where each row is one record and each column is one fact.

In this course, you will ask tables for exact rows, the way Nandini wants her ledger to answer.

> <span style="color:#2F7DDE">**Think about it:**</span> Which part of the customer's request did the helper read wrongly?

---

### <span style="color:#2F7DDE">The Fruit Market Ledger Puzzle</span>

Here are four rows of Nandini's ledger.

| Fruit | Colour | Price per kg |
|:----------:|:----------:|:----------:|
| Apple | Red | Rs 180 |
| Guava | Green | Rs 60 |
| Banana | Yellow | Rs 50 |
| Cherry | Red | Rs 60 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Nandini asks for only the fruit and price columns.
- Nandini sees each colour listed once.
- Nandini lists the cheapest fruit first.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - How would Nandini ask for red fruits under Rs 80, or any green fruit, without mixing the two?
> - What should she do when two fruits cost the same?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The ledger has 120 rows and 4 columns. How would you ask for only the fruit names?**
Hint: Name the column you want and the ledger you read from.

**2. A customer wants fruit priced from Rs 50 to Rs 80. Are Rs 50 and Rs 80 inside the range?**
Hint: Decide whether the ends count.

**3. Two fruits cost Rs 60. How should the list order them so it never changes between runs?**
Hint: Think of a second fact that is different for every fruit.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do we write a request so the table returns only the rows we mean, in the order we want?**</span>
>
> Which part of the customer's request would you write first?
