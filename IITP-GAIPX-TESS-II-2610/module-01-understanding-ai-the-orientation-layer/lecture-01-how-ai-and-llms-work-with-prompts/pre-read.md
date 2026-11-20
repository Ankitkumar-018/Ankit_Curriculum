## <span style="color:#2F7DDE">How AI and LLMs Work with Prompts</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>How AI and LLMs Work with Prompts"]
  Q["<b>The Big Question</b><br/><i>How can a computer finish your sentence so smoothly, and why can it still be wrong?</i>"]
  CV["<b>Course use case</b><br/>Writing a 4-part request for a free chat tool and checking 3 facts in its reply"]
  RL["<b>Real-world example</b><br/>A cousin who sings the next line of a song you hum"]

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

Have you ever wondered how your cousin knows the next word after you hum one line?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Name**</span> the 4 parts of a clear request to a helper.
- <span style="color:#D9660B">**Describe**</span> how your cousin sings one word at a time, and how a long word gets cut into pieces.
- <span style="color:#D9660B">**Explain**</span> why your cousin can hold only the last 3 or 4 lines in mind.
- <span style="color:#D9660B">**Predict**</span> how a bolder guess changes the next word he picks.
- <span style="color:#D9660B">**Compare**</span> a fixed rulebook, a learner and a composer by what each one covers.
- <span style="color:#D9660B">**Justify**</span> why a confident singer can still sing a wrong line.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> AI vs ML vs GenAI, next-token prediction, tokens, context and temperature, hallucination, four elements of a prompt.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Neha and her cousin Arjun play a song game on a long train ride. Neha hums one line. Arjun sings the next word, then the next, until the verse ends.

For old songs, he is right 3 times out of 3. For a song Neha made up, he sings a confident line she never wrote.

A <span style="color:#D9660B">**token**</span> means one small piece of text, such as a short word or part of a long word.

Chat tools in this course continue text in a similar way, one token at a time.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did Arjun sound as sure about the made-up song as about the old ones?

---

### <span style="color:#2F7DDE">The Song Game Puzzle</span>

Here are 4 rounds from the train ride.

| Line Neha hums | Next word Arjun sings | Matches the real song? |
|:----------:|:----------:|:----------:|
| Twinkle, twinkle, little | star | Yes |
| Happy birthday to | you | Yes |
| Row, row, row your | boat | Yes |
| Neha's new song: Blue moon over the | river | No, she wrote "tower" |

<span style="color:#D9660B">**What you want to happen:**</span>

- Arjun sings the right word for every round.
- Arjun says "I do not know this one" when he has never heard it.
- Neha asks in a way that leaves him no room to guess.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What would change if Neha hummed 10 lines instead of 1 before pausing?
> - What would change if she asked him to sing only songs she names?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. In round 4, Arjun picked "river". Why might it feel like a safe guess to him?**
Hint: Think about which words usually follow "Blue moon over the".

**2. If Arjun can remember only the last 4 lines, what happens when Neha sings line 5?**
Hint: Count the lines that fit in his head.

**3. Neha says: "Sing the next 2 lines. Say 'unknown' if you have not heard it." What 2 parts did she add?**
Hint: One part limits what he may do. One part shapes the answer.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How does a helper that only continues patterns end up sounding certain about something it never knew?**</span>
>
> What would you tell the helper before the first word to stop that?
