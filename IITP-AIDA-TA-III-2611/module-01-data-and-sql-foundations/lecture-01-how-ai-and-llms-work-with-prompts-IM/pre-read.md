## <span style="color:#2F7DDE">How AI and LLMs Work with Prompts</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>How AI and LLMs Work with Prompts"]
  Q["<b>The Big Question</b><br/><i>How does a chatbot build a notice one piece at a time, and why can a smooth notice be wrong?</i>"]
  CV["<b>Course use case</b><br/>A shop chatbot draft that promised a refund the policy never offered"]
  RL["<b>Real-world example</b><br/>A school trip notice written by a helper who guesses each next word"]

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

Have you ever wondered how a phone keyboard guesses the next word before you type it?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**List**</span> the 4 roles on the school app team and what each role does.
- <span style="color:#D9660B">**Describe**</span> how a helper picks the word after 'Dear' when writing the trip notice.
- <span style="color:#D9660B">**Explain**</span> why a smooth notice can still name the wrong bus time.
- <span style="color:#D9660B">**Predict**</span> how the notice changes when the helper is told to be bold or careful.
- <span style="color:#D9660B">**Compare**</span> a vague request with a request that holds a task, a context, a shape and rules.
- <span style="color:#D9660B">**Write**</span> a 4-part request for the trip notice.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> AI vs ML vs GenAI, next-token prediction, tokens context and temperature, hallucination, four elements of a prompt, roles and use cases across AI ML and GenAI.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mrs. Kapoor needs a notice for the Science Museum trip. A helper writes it in 10 seconds. The notice sounds warm and clear. It says the bus leaves at 8:00 am. The real time is 7:30 am. Twelve students arrived late. The helper never checked the time. The helper wrote the words that sounded most likely.

A <span style="color:#D9660B">**prompt**</span> means the instruction you give an AI helper before it writes.

In this course, you will write clear prompts and check what an AI helper writes against the facts.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did a notice that sounded so sure carry a wrong time?

---

### <span style="color:#2F7DDE">Trip Notice Puzzle</span>

Here are the facts Mrs. Kapoor has.

| Detail | Fact |
|:----------:|:----------:|
| Place | Science Museum |
| Date | 20 March |
| Bus leaves | 7:30 am |
| Fee | Rs 250 |
| Return | 4:00 pm |

<span style="color:#D9660B">**What you want to happen:**</span>

- The notice carries every fact above, exactly as written.
- The notice is 3 short sentences, ready for parents.
- The notice never promises a snack or a refund.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What should Mrs. Kapoor tell the helper before it starts writing?
> - Would the helper write the same notice twice?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Mrs. Kapoor types only 'Write a notice'. Which 2 facts could the helper guess wrong?**
Hint: Look at the table for times and money.

**2. She adds the table above to her request. How does that change what the helper has to guess?**
Hint: Think about what is known and what is missing.

**3. Who else on a school app team would you ask to check the notice before it goes out?**
Hint: Think of someone who tests, someone who owns the facts and someone who builds.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can we ask an AI helper so that a smooth answer is also a true one?**</span>
>
> Which fact in the trip notice would you check first?
