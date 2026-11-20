## <span style="color:#2F7DDE">How AI and LLMs Work with Prompts</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>How AI and LLMs Work with Prompts"]
  Q["<b>The Big Question</b><br/><i>Why can a smooth answer be wrong, and how do I ask so I can check it?</i>"]
  CV["<b>Course use case</b><br/>Asking a chat tool for a 3-sentence refund reply that uses a 5 to 7 day policy"]
  RL["<b>Real-world example</b><br/>A new tailor's apprentice who guesses a sleeve length from past orders"]

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

Have you ever wondered how an apprentice can sound sure about a measurement he never took?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Describe**</span> how a reply gets built one small piece at a time.
- <span style="color:#D9660B">**Explain**</span> why a confident answer, like a 24-inch sleeve guess, can still be wrong.
- <span style="color:#D9660B">**Predict**</span> what happens to the variety of replies when a boldness dial goes up.
- <span style="color:#D9660B">**Calculate**</span> how much room is left when a helper keeps only 5 notes in mind.
- <span style="color:#D9660B">**Compare**</span> a rule book, a helper who learns from orders and a helper who invents new designs.
- <span style="color:#D9660B">**Write**</span> a request with 4 parts, so a helper has less to guess.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> AI vs ML vs GenAI, next-token prediction, tokens, context and temperature, hallucination, four elements of a prompt, trying the four prompt elements in a free chat tool.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mr. Qureshi runs a tailor shop in a lane near the station. His new apprentice, Bilal, has watched 500 orders.

A customer asks for a kurta "like last time". Bilal guesses a 24-inch sleeve, the usual length. He sounds sure.

The customer's real sleeve is 26 inches. Bilal never opened the measurement card.

A <span style="color:#D9660B">**prompt**</span> means the written request you give an AI tool to say what you want.

In this course, you will write prompts for free chat tools and check each reply.

> <span style="color:#2F7DDE">**Think about it:**</span> If Bilal had read the customer's card first, would he still need to guess?

---

### <span style="color:#2F7DDE">The Tailor Shop Puzzle</span>

Mr. Qureshi chalks four facts on the shop board.

| Fact | Value |
|:----------:|:----------:|
| Orders Bilal has watched | 500 |
| Usual kurta sleeve length | 24 inches |
| This customer's real sleeve length | 26 inches |
| Notes Bilal can hold in his head at once | 5 orders |

<span style="color:#D9660B">**What you want to happen:**</span>

- Bilal asks for the card before he guesses.
- Bilal keeps the right 5 notes in mind.
- Bilal gives a reply that Mr. Qureshi can check.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Why did Bilal sound sure when the card was never read?
> - What happens to the first note when a sixth order arrives?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Bilal holds 5 notes. A sixth order arrives. What happens to the first note?**
Hint: Picture a notepad with room for 5 lines.

**2. Which request gives Bilal more to work with: "Make it quick" or "Make a cotton kurta, 26-inch sleeve, ready Friday"?**
Hint: Count the facts each one gives.

**3. On a bold day, Bilal tries a new collar. On a careful day, he copies the usual. Which day gives you the same shirt twice?**
Hint: Think about which day repeats the past.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**What makes an answer sound sure, and what makes it right?**</span>
>
> Which fact would you hand Bilal before he starts to stitch?
