## <span style="color:#2F7DDE">Lookup Functions and Conditional Aggregation</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Lookup Functions and Conditional Aggregation"]
  Q["<b>The Big Question</b><br/><i>How do I fetch a value from another list and trust it when it fails?</i>"]
  CV["<b>Course use case</b><br/>Naming 120 service bookings from an 8-row price list and totalling Rs 167,130 by city"]
  RL["<b>Real-world example</b><br/>A stationery shop matching bill codes to its price list"]

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

Have you ever wondered how a shop finds the price of an item from a short code on the bill?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Describe**</span> how a helper finds a price on a list using an item code.
- <span style="color:#D9660B">**Calculate**</span> Saturday notebook sales from 3 bill lines using two conditions at once.
- <span style="color:#D9660B">**Use**</span> a slab list to pick a 5% or 10% discount for a bill total.
- <span style="color:#D9660B">**Determine**</span> what a bill should say when a code is missing from the list.
- <span style="color:#D9660B">**Examine**</span> why a code that looks identical still finds no price.
- <span style="color:#D9660B">**Write**</span> a question for a chat tool that names the symptom and asks for checks.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> VLOOKUP, XLOOKUP, fixing #N/A in lookups, IFERROR, SUMIFS and COUNTIFS, banding with a lookup, asking an AI tool to explain a lookup error.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mr. Gupta runs a stationery shop. His helper, Tanu, writes a short code on every bill line.

Tanu searches the price list for the code NB2. The list has NB2, but the bill says "NB2 " with a space after it.

She finds nothing and writes a price of zero. The shop loses Rs 40 on each notebook.

A <span style="color:#D9660B">**lookup**</span> means finding a value in one list by matching a code from another list.

In this course, you will look up values across sheets and explain every gap.

> <span style="color:#2F7DDE">**Think about it:**</span> What should Tanu have written on the bill when she found no match?

---

### <span style="color:#2F7DDE">The Stationery Shop Puzzle</span>

The price list shows PEN1 at Rs 10, NB2 at Rs 40 and GL3 at Rs 25. Tanu writes three bill lines.

| Bill line | Code written | Quantity | Day |
|:----------:|:----------:|:----------:|:----------:|
| 1 | PEN1 | 10 | Saturday |
| 2 | "NB2 " with a space | 5 | Saturday |
| 3 | GL9 | 2 | Sunday |

<span style="color:#D9660B">**What you want to happen:**</span>

- Each bill line shows its price from the list.
- A code that is truly missing says "Ask manager".
- The shop counts Saturday notebook sales using two conditions.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Why do "NB2" and "NB2 " not match?
> - Which discount slab would a Rs 1,000 bill earn?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Line 2 says "NB2 " with a space. Why might the price list refuse to match it?**
Hint: Count the characters in each one.

**2. Code GL9 is not on the price list at all. What should the bill show?**
Hint: Say what Tanu should do next.

**3. Slabs are 0 to 499, 500 to 999 and 1,000 and above. Which slab does a Rs 1,000 bill earn?**
Hint: Check the edge of each slab.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you tell a mistake in a code from a code that is truly missing?**</span>
>
> Which bill line would you check first?
