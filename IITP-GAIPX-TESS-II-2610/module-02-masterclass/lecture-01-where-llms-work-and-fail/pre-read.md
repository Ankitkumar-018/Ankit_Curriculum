## <span style="color:#2F7DDE">Where LLMs Work and Fail</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Where LLMs Work and Fail"]
  Q["<b>The Big Question</b><br/><i>Which helper should I pick for which job, and when should I not trust any helper?</i>"]
  CV["<b>Course use case</b><br/>Choosing a model for 5 support jobs, one of which cost Rs 1.20 an answer"]
  RL["<b>Real-world example</b><br/>Choosing helpers and a truck for moving house"]

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

Have you ever wondered why a confident helper can still give you a wrong address?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Describe**</span> the 3 ways a helper can take in a job: written notes, photos and voice notes.
- <span style="color:#D9660B">**Explain**</span> why a helper who sounds sure can still send you to the wrong floor.
- <span style="color:#D9660B">**Classify**</span> 6 moving-day jobs as safe to hand over or in need of a check.
- <span style="color:#D9660B">**Compare**</span> renting a truck for Rs 3,000 a trip with owning one for Rs 20,000 a month.
- <span style="color:#D9660B">**Differentiate**</span> a careful packer from a quick packer by time, cost and the job.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> Hosted vs open models, reasoning models, multimodal inputs, fluent but wrong answers, reliable vs unreliable tasks.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Nikhil is moving to a new flat on Saturday. He needs a truck, packers and someone to give directions.

His helper Ravi says, "The flat is on the 3rd floor." He sounds sure. The flat is on the 5th, and the movers carry boxes up the wrong stairs.

A <span style="color:#D9660B">**fluent but wrong answer**</span> means a reply that sounds smooth and sure but is false.

You will learn to match a model to a job. You will also spot jobs it should not do alone.

> <span style="color:#2F7DDE">**Think about it:**</span> What could Nikhil have asked Ravi before trusting "3rd floor"?

---

### <span style="color:#2F7DDE">The Moving Day Puzzle</span>

Here are Nikhil's choices for Saturday.

| Choice | Option A | Option B |
|:----------:|:----------:|:----------:|
| Truck | Rent: Rs 3,000 a trip | Own: Rs 20,000 a month |
| Packer | Careful: 4 hours, Rs 800 | Quick: 1 hour, Rs 200 |
| Directions | Ravi from memory: "3rd floor" | Photo of the building board |

<span style="color:#D9660B">**What you want to happen:**</span>

- The truck choice depends on the number of trips you make.
- The packer choice depends on the job: fragile glass or old books.
- Directions come from a photo, not from memory.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - At what number of trips a month does owning the truck cost less?
> - Which job on moving day would you never leave to Ravi's memory?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Nikhil makes 2 trips this month. Which truck option costs less?**
Hint: Compare 2 × 3,000 with 20,000.

**2. Which packer should wrap the glass, and which should pack the old books?**
Hint: Match the care needed to the time and cost.

**3. Ravi quotes the rent of the new flat from memory. How could Nikhil check it?**
Hint: Look for a paper or a photo that holds the number.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you decide which jobs a smooth-talking helper can do alone?**</span>
>
> What would you ask the helper to show before you trust it?
