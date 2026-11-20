## <span style="color:#2F7DDE">How AI and LLMs Work with Prompts</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>How AI and LLMs Work with Prompts"]
  Q["<b>The Big Question</b><br/><i>How does a computer write text one piece at a time, and why can it be wrong?</i>"]
  CV["<b>Course use case</b><br/>Writing a 4-part prompt for a free chat tool and checking every fact in the reply"]
  RL["<b>Real-world example</b><br/>A phone keyboard that suggests your next word"]

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

Have you ever wondered how your phone keyboard guesses the next word before you type it?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Name**</span> three ideas about smart computers, from the widest to the narrowest.
- <span style="color:#D9660B">**Describe**</span> how a keyboard builds a message one small piece at a time.
- <span style="color:#D9660B">**Explain**</span> why a keyboard can only keep the last few words in mind.
- <span style="color:#D9660B">**Predict**</span> how turning up the randomness changes the 3 suggestions you see.
- <span style="color:#D9660B">**Justify**</span> why a confident suggestion can still be wrong.
- <span style="color:#D9660B">**Write**</span> a 4-part message that gives a helper the job, the facts, the shape and the limits.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> AI vs ML vs GenAI, next-token prediction, tokens, context window, temperature, hallucination, four elements of a prompt.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

You type "Order 3 cups of" in a message to your friend. Your phone shows 3 words: "tea", "coffee" and "chai".

You tap one. The phone shows 3 new words. You never typed a full sentence, yet the full message appears.

A <span style="color:#D9660B">**token**</span> means a small piece of text, such as a short word or part of a long word.

Your keyboard guesses the next piece each time. Chat tools in this course do the same job, on a much larger scale.

> <span style="color:#2F7DDE">**Think about it:**</span> If the keyboard has never seen your friend's name, what might it suggest instead?

---

### <span style="color:#2F7DDE">The Phone Keyboard Puzzle</span>

Here are the words you have typed and what the keyboard shows.

| Words typed so far | Suggestion 1 | Suggestion 2 | Suggestion 3 |
|:----------:|:----------:|:----------:|:----------:|
| Order 3 cups of | tea | coffee | chai |
| See you at | 5 | the | home |
| Happy birthday | to | my | dear |

<span style="color:#D9660B">**What you want to happen:**</span>

- The suggestions match what you mean to say.
- Each new word fits the words before it.
- The keyboard never invents a fact, such as a wrong phone number.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Would the same words give the same 3 suggestions if you typed them again tomorrow?
> - What would happen if you typed a long message and the keyboard forgot the start?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. You type "Order 3 cups of". Why might "tea" be shown before "wheels"?**
Hint: Think about which words usually follow those 4 words.

**2. You ask a friend, "Write something." What 4 details would help them write what you want?**
Hint: Think about the job, the facts, the shape and the limits.

**3. The keyboard suggests your friend's name with full confidence, but spells it wrong. Does confidence prove it is right?**
Hint: Ask how the keyboard picked the name.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can a tool write smooth text that is still wrong?**</span>
>
> Which of your last 3 messages would you re-read before sending, and why?
