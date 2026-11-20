## <span style="color:#2F7DDE">Relational Databases and SELECT Queries</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Relational Databases and SELECT Queries"]
  Q["<b>The Big Question</b><br/><i>How do I ask a big table for exactly the rows I need?</i>"]
  CV["<b>Course use case</b><br/>Asking a 120-row medicines table for the 12 in-stock tablets under Rs 35"]
  RL["<b>Real-world example</b><br/>A station clerk searching a lost-and-found register for the right bag"]

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

Have you ever wondered how a station clerk finds your lost bag among hundreds of entries?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Describe**</span> how a register stores each found item as a row with fixed columns.
- <span style="color:#D9660B">**Explain**</span> why mixing "and" with "or" without brackets changes the list.
- <span style="color:#D9660B">**Use**</span> a comparison to pick items found on platform 3 or higher.
- <span style="color:#D9660B">**Apply**</span> a list, a range and a name pattern to narrow 5 items.
- <span style="color:#D9660B">**Build**</span> a rule that joins three conditions into one request.
- <span style="color:#D9660B">**Write**</span> a request that sorts items by colour, then by platform.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Tables rows and schema, SELECT, WHERE, AND OR and NOT, IN LIKE and date range (BETWEEN), ORDER BY.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mr. Das is the clerk at a railway station. A traveller asks, "Show me black or blue bags found on platform 1 that are still unclaimed."

Mr. Das pulls every black bag, from any platform. He adds the blue bags found on platform 1.

The traveller gets a black bag from platform 4 that was claimed last week. The traveller misses the train.

A <span style="color:#D9660B">**table**</span> means a grid where each row is one record and each column is one fact about it.

In this course, you will ask tables of 120 rows or more for exactly the rows you need.

> <span style="color:#2F7DDE">**Think about it:**</span> Which words in the traveller's request did Mr. Das read in the wrong order?

---

### <span style="color:#2F7DDE">The Lost-and-Found Puzzle</span>

Mr. Das keeps one row for each found item. Here are five of them.

| Item | Colour | Platform | Status |
|:----------:|:----------:|:----------:|:----------:|
| Backpack | Black | 4 | Claimed |
| Duffel bag | Blue | 1 | Unclaimed |
| Handbag | Black | 1 | Unclaimed |
| Umbrella | Red | 2 | Unclaimed |
| Backpack | Blue | 3 | Unclaimed |

<span style="color:#D9660B">**What you want to happen:**</span>

- The list shows only the columns the traveller needs.
- Only unclaimed black or blue bags from platform 1 remain.
- The list is sorted by colour, then by platform.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Which items remain if "and" is read before "or"?
> - Which two items start with the word Back?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which of the five items are black or blue, from platform 1 and unclaimed?**
Hint: Check each item against all three tests.

**2. Does the backpack from platform 3 pass "between platform 1 and 2"?**
Hint: Look at both ends of the range.

**3. Two items have the same colour. How would you decide which comes first?**
Hint: Pick a second column to break the tie.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you write a request so the list has exactly the rows you meant?**</span>
>
> Which tests would you group in brackets for the traveller's request?
