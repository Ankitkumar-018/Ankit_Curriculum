# <font color='#1d4ed8'>Lecture Script: How AI and LLMs Work with Prompts</font>

---

## <font color='blue'>Agenda</font>

The lecture runs as four topics. Each topic ends with a quiz.

| Topic | What we do | Learning objectives covered | Minutes |
|:-:|:--|:--|:-:|
| 1 | Place AI, ML and GenAI, then see how a reply is built word by word | Compare AI, machine learning and generative AI by what each term covers<br>Describe next-token prediction as the mechanism that produces an LLM response | 25 |
| 2 | Split text into tokens and count what the model can hold | Describe how a tokenizer splits text into subword tokens<br>Explain what a context window limits and what counts against it | 25 |
| 3 | Turn the temperature dial and catch a confident wrong answer | Predict how raising temperature changes the variability of an output<br>Explain why a model can produce fluent text that is factually wrong | 30 |
| 4 | Write a prompt with four elements and try it live | State the four elements of a well-formed prompt: task, context, format and constraints | 25 |
| — | Closing: Outcome & Summary | | 15 |
| | **Total** | | **120** |

> <font color="red">**🎯 Instructor Note**</font> Pace: keep the AI, ML and GenAI comparison in Topic 1 brisk. Spend the extra minutes on temperature and on the live prompt in Topic 4.
> Topic 4 runs live in a free chat tool (ChatGPT, Claude or Gemini). Replies differ on every run, so learners fill the tables from what they see.

---

## <font color='blue'>Scenario</font>

**A single risk.** A Myntra-style fashion app in Bengaluru lets its support team use a free chat tool to draft replies. The risk sits in one sentence the tool might write.

> "Your refund will be credited within 2 hours."

The app's real rule is 5 to 7 working days. A customer who reads "2 hours" will wait two hours, then call, then post a complaint.

> <font color="red">**🎯 Instructor Note**</font> The company is only the setting. Do not claim it uses a chat tool or these rules. The refund rule, the probabilities and the token counts are invented for teaching.

---

## <font color='blue'>Problem Statement</font>

Rhea works in customer support. A customer asks, "When will my refund arrive?" Rhea types the question into a chat tool and pastes the reply without reading it. The reply sounds polished and says "within 2 hours". The real rule is 5 to 7 working days. Two days later the customer is angry, and Rhea cannot explain why a tool that sounds so sure was wrong.

> <font color='purple'>**How does a chat tool build its reply, why can that reply be fluent and wrong, and how do we write a prompt that gets a reply we can check?**</font>

> <font color="red">**🎯 Instructor Note**</font> Poll: "If a reply is well written, is it more likely to be correct?" Give learners 30 seconds to respond in chat. Reveal the answer in the Closing.

---

## <font color='blue'>What We Will Use</font>

Three free chat tools: ChatGPT, Claude and Gemini. The mentor runs each prompt live. Learners compare what they see with the tables below.

| Topic | Ideas | In one line |
|:-:|:--|:--|
| 1 | AI, ML, GenAI, next-token prediction | Three nested terms, and a model that picks the next piece of text |
| 2 | Token, tokenizer, context window | Text is cut into pieces, and a fixed number of pieces fit at once |
| 3 | Temperature, hallucination | A dial for variety, and the reason a fluent answer can be false |
| 4 | Task, context, format, constraints | Four parts that make a prompt clear |

---

## <font color='blue'>How: Walking Through Rhea's Refund Reply</font>

```mermaid
flowchart LR
    A["Topic 1<br>AI, ML, GenAI and next token"] --> B["Topic 2<br>Tokens and context window"]
    B --> C["Topic 3<br>Temperature and hallucination"]
    C --> D["Topic 4<br>Four-element prompt"]
    D --> E["Closing<br>A refund reply Rhea can check"]
    style A fill:#dbeafe,stroke:#2563eb
    style B fill:#dcfce7,stroke:#16a34a
    style C fill:#fef3c7,stroke:#d97706
    style D fill:#ede9fe,stroke:#7c3aed
    style E fill:#fee2e2,stroke:#dc2626
```

---

## <font color='blue'>Topic 1: Place AI, ML and GenAI, then see how a reply is built word by word</font> `25 min`

> <font color='purple'>**What exactly is the tool that wrote "within 2 hours"?**</font>

### <font color='green'>Example: Three nested terms</font>

> <font color='purple'>**How do AI, machine learning and generative AI relate to each other?**</font>

**Artificial intelligence (AI)** is any software that does a task that normally needs human judgment. **Machine learning (ML)** is AI that learns its rules from data instead of being given every rule. **Generative AI (GenAI)** is ML that creates new content such as text, images or code. Each term sits inside the one before it.

```mermaid
flowchart TB
    A["AI: software doing a task that needs judgment"] --> B["ML: AI whose rules are learned from data"]
    B --> C["GenAI: ML that creates new text, images or code"]
    C --> D["LLM: GenAI that works on text"]
    style A fill:#dbeafe,stroke:#2563eb
    style B fill:#dcfce7,stroke:#16a34a
    style C fill:#fef3c7,stroke:#d97706
    style D fill:#ede9fe,stroke:#7c3aed
```

| Example at the app | AI | ML | GenAI |
|:--|:-:|:-:|:-:|
| A rule: "if order value is above Rs 5,000, flag for check" | Yes | No | No |
| A model that learned from past returns which orders are likely to be returned | Yes | Yes | No |
| A chat tool that writes a new reply to a customer | Yes | Yes | Yes |

> <font color='green'>**Result**</font> The first row is AI without learning. The second row learns from data but does not create text. Only the third row is GenAI, and it is the kind Rhea used.

> <font color="red">**🎯 Instructor Note**</font> Ask learners to type where "a spam filter that learned from past emails" fits. Expected: AI and ML, not GenAI.

### <font color='green'>Example: A reply is built one token at a time</font>

> <font color='purple'>**How does a chat tool decide what to write next?**</font>

A **large language model (LLM)** is a GenAI model trained on very large amounts of text. It works by **next-token prediction**: given the text so far, it scores every possible next piece of text, picks one, adds it and repeats. It does not look up a fact. It continues the pattern.

The scores below are invented for teaching. The text so far is "Your refund will be credited in".

| Next piece of text | Probability |
|:--|:-:|
| 5 days | 47.4% |
| 7 days | 28.7% |
| 3 days | 17.4% |
| 10 days | 6.4% |

#### <font color='#c2410c'>Logic Explanation</font>

- The model picks one row, adds it to the text, and asks the same question again for the next piece.
- Nothing in this table says what the real refund rule is. The probabilities only say which continuation is common.

> <font color='green'>**Result**</font> A reply is a chain of small choices. A fluent chain can still land on a wrong number.

<p align="center"><img src="images/01_next_token.png" alt="Bar chart of the next-piece probabilities for the text so far: 5 days 47.4 percent, 7 days 28.7, 3 days 17.4 and 10 days 6.4" width="900"></p>

### <font color='purple'>Quiz 1</font>

**Question:** Which statement describes next-token prediction?

**Options:**
- A) The model searches a database and copies the matching answer
- B) The model scores possible next pieces of text, picks one and repeats
- C) The model asks a human to check each sentence
- D) The model writes the whole reply at once, then checks it

**Correct Answer:** B

**Explanation:**
- **A)** An LLM does not copy from a lookup table. It builds text from learned patterns.
- **B)** Correct. It scores the candidates, picks one, adds it and asks again.
- **C)** No human is involved while the reply is generated.
- **D)** The reply is built piece by piece. There is no separate full draft and check.

---

## <font color='blue'>Topic 2: Split text into tokens and count what the model can hold</font> `25 min`

> <font color='purple'>**What is a "piece of text", and how many pieces can the tool keep in view?**</font>

### <font color='green'>Example: How a tokenizer cuts a sentence</font>

> <font color='purple'>**How is "Refundable orders get refunds" cut into pieces?**</font>

A **token** is a piece of text the model reads as one unit. A **tokenizer** cuts text into tokens, often as whole words, parts of words ("subwords") or punctuation. Rare or long words split into smaller known parts.

The split below is an illustration invented for teaching. Each real tool has its own tokenizer, so the exact cuts and counts differ.

| Text | Illustrative tokens | Count |
|:--|:--|:-:|
| Refundable | Refund + able | 2 |
| orders | orders | 1 |
| get | get | 1 |
| refunds | refund + s | 2 |
| **Whole sentence** | | **6** |

> <font color='green'>**Result**</font> Six tokens for four words. A word is not a token. Common words are often one token. Long or rare words split into parts.

> <font color="red">**🎯 Instructor Note**</font> Ask learners to guess the count for "Unrefundable". Expected: more than one token, likely 3 (un + refund + able). Say again that real splits differ by tool.

### <font color='green'>Example: What fills the context window</font>

> <font color='purple'>**What counts against the model's memory for one chat?**</font>

The **context window** is the maximum number of tokens the model can use at once. It counts everything: your instructions, the earlier messages in the chat and the reply being written. Anything beyond the limit is cut or ignored.

Invented for teaching: a window of 1,000 tokens.

| Part of the chat | Tokens |
|:--|:-:|
| Support policy pasted by Rhea | 450 |
| Earlier messages in the chat | 300 |
| Rhea's new question | 50 |
| Left for the reply | 200 |
| **Window** | **1,000** |

$$\boxed{ \text{space left for the reply} = \text{window} - \text{policy} - \text{earlier messages} - \text{new question} }$$

$$1000 - 450 - 300 - 50 = 200$$

> <font color='green'>**Result**</font> Only 200 tokens are left for the answer. Pasting a longer policy would leave less room for the reply.

<p align="center"><img src="images/02_context_window.png" alt="Single stacked bar of a 1,000 token window split into policy 450, earlier messages 300, new question 50 and reply space 200" width="900"></p>

### <font color='green'>Extending it: Paste a longer policy</font>

> <font color='purple'>**If the pasted policy grows to 700 tokens, how much room is left?**</font>

> <font color="red">**🎯 Instructor Note**</font> Ask learners to type the number in chat. Expected: $1000 - 700 - 300 - 50 = -50$, so the policy no longer fits and something is cut.

> <font color='green'>**Result**</font> The total would be 1,050 tokens, which is 50 over the window. The tool must drop text, so older parts of the chat may be forgotten.

> <font color='#b45309'>**Common mistake**</font> Thinking the window only counts the question. Fix: count the whole chat and the reply too.

### <font color='purple'>Quiz 2</font>

**Question:** A window is 1,000 tokens. The chat holds 600 tokens and the new question is 100 tokens. How many tokens are left for the reply?

**Options:**
- A) 400
- B) 900
- C) 1,700
- D) 300

**Correct Answer:** D

**Explanation:**
- **A)** 400 ignores the 100-token question. $1000 - 600 = 400$ leaves out one part.
- **B)** 900 subtracts only the question and forgets the 600-token chat.
- **C)** 1,700 adds the numbers. A window is a limit, so the parts are subtracted from it.
- **D)** Correct. $1000 - 600 - 100 = 300$.

---

## <font color='blue'>Topic 3: Turn the temperature dial and catch a confident wrong answer</font> `30 min`

> <font color='purple'>**Why does the same question give a different reply each time, and why was the "2 hours" reply so sure of itself?**</font>

### <font color='green'>Example: Raising the temperature</font>

> <font color='purple'>**What happens to the next-piece probabilities when temperature goes up?**</font>

**Temperature** is a setting that controls how much the choice varies. Low temperature sharpens the scores, so the top choice wins most of the time. High temperature flattens them, so less likely choices get picked more often.

$$p_i = \frac{e^{s_i / T}}{\sum_j e^{s_j / T}}$$

Here $s_i$ is the invented score of one choice and $T$ is the temperature. We use scores 2.0, 1.5, 1.0 and 0.0 for "5 days", "7 days", "3 days" and "10 days". All values were recomputed in Python.

**Predict before running: What will happen?**

> <font color="red">**🎯 Instructor Note**</font> Expected: at $T = 0.5$ the top choice grows, and at $T = 2$ the four choices come closer. Common wrong guess: higher temperature makes the model "more accurate".

| Next piece | $T = 0.5$ | $T = 1$ | $T = 2$ |
|:--|:-:|:-:|:-:|
| 5 days | 65.7% | 47.4% | 36.3% |
| 7 days | 24.2% | 28.7% | 28.3% |
| 3 days | 8.9% | 17.4% | 22.0% |
| 10 days | 1.2% | 6.4% | 13.4% |

> <font color='green'>**Result**</font> Going from $T = 0.5$ to $T = 2$ cuts the top choice from 65.7% to 36.3%. The unlikely "10 days" grows from 1.2% to 13.4%. Higher temperature means more variety, not more truth.

<p align="center"><img src="images/03_temperature.png" alt="Grouped bar chart of the four next-piece probabilities at temperature 0.5, 1 and 2" width="900"></p>

### <font color='green'>Extending it: Run the same prompt twice, live</font>

> <font color='purple'>**Do two runs of the same question give the same words?**</font>

> <font color="red">**🎯 Instructor Note**</font> Mentor: in a free chat tool, ask "Suggest a subject line for a refund-delay email" twice in two new chats. Learners note which words differ. Do not predict the exact replies.

| Run | Subject line the tool wrote | Same wording as run 1? |
|:-:|:--|:-:|
| 1 | Learners write it here | |
| 2 | Learners write it here | Yes or No |

> <font color='green'>**Result**</font> Differences between runs come from the random pick at each token. A tool with a higher temperature setting would differ more.

### <font color='green'>Example: Why a fluent answer can be wrong</font>

> <font color='purple'>**Why did the tool say "within 2 hours" with no hint of doubt?**</font>

A **hallucination** is a reply that sounds right but states something false or unsupported. The model was trained to continue text in a likely way. It was not built to check facts. If it never saw the app's refund rule, it still writes a smooth sentence in the usual style of refund replies.

| What the model has | What the model lacks |
|:--|:--|
| Patterns of how refund replies read | The app's real refund rule |
| Words like "credited within" | A way to check "2 hours" against a record |
| A confident tone | A signal that tells it when it is guessing |

> <font color='green'>**Result**</font> The reply was fluent because the model is good at style. It was wrong because the rule was never given to it.

> <font color='#b45309'>**Common mistake**</font> Trusting a reply because it reads well. Fix: check every number, date and policy against a source you own.

### <font color='purple'>Quiz 3</font>

**Question:** Rhea raises the temperature from low to high. What is the most likely change?

**Options:**
- A) The replies become more accurate
- B) The replies become identical every time
- C) The replies vary more from run to run
- D) The context window grows

**Correct Answer:** C

**Explanation:**
- **A)** Temperature controls variety, not accuracy.
- **B)** Low temperature moves towards the same reply. High temperature does the opposite.
- **C)** Correct. A flatter distribution means less likely pieces are picked more often.
- **D)** The window is a fixed limit of the model. Temperature does not change it.

---

## <font color='blue'>Topic 4: Write a prompt with four elements and try it live</font> `25 min`

> <font color='purple'>**How should Rhea ask, so the reply uses her policy and can be checked?**</font>

### <font color='green'>Example: Weak prompt and four-element prompt</font>

> <font color='purple'>**What is missing from "When will my refund arrive?"**</font>

A well-formed prompt has four elements.

| Element | What it says | Example for Rhea |
|:--|:--|:--|
| Task | What you want done | Write a reply to a customer asking about a refund |
| Context | The facts the model needs | Policy: refund in 5 to 7 working days after pickup. Return picked up on 12 March 2026 |
| Format | How the answer should look | 3 short sentences, then one line starting "Policy:" |
| Constraints | Limits and rules | Use only the policy given. Do not promise a date outside it. Under 60 words |

> <font color='green'>**Result**</font> The weak prompt has only a task. The four-element prompt gives the model the rule, so it has less need to guess.

### <font color='green'>Extending it: Run both prompts live</font>

> <font color='purple'>**Does the four-element prompt give a reply Rhea can check?**</font>

> <font color="red">**🎯 Instructor Note**</font> Mentor: run both prompts live in ChatGPT, Claude or Gemini. Learners fill the table. Do not predict the wording. Replies differ on every run.

| Check | Weak prompt reply | Four-element reply |
|:--|:-:|:-:|
| Does it say 5 to 7 working days? | Yes or No | Yes or No |
| Does it invent a rule that is not in the policy? | Yes or No | Yes or No |
| Does it fit in 60 words? | Yes or No | Yes or No |
| Does it end with a "Policy:" line? | Yes or No | Yes or No |

> <font color='green'>**Result**</font> Learners compare the two columns. A reply that passes all four checks is one Rhea can verify against the policy line.

> <font color='#b45309'>**Common mistake**</font> Writing a long context but no constraint. Fix: add "use only the policy given" so the model does not add facts.

### <font color='green'>Extending it: Add one element at a time</font>

> <font color='purple'>**Which element changes the reply most?**</font>

> <font color="red">**🎯 Instructor Note**</font> Mentor: start with the task only, then add context, then format, then constraints. Ask learners which step changed the reply most. Answers vary. There is no single correct order.

### <font color='purple'>Quiz 4</font>

**Question:** Which prompt contains all four elements?

**Options:**
- A) "Write a refund reply. Policy: 5 to 7 working days. Use 3 sentences. Use only this policy."
- B) "Write a refund reply. Policy: 5 to 7 working days."
- C) "Write a refund reply."
- D) "You are a helpful assistant. Be nice."

**Correct Answer:** A

**Explanation:**
- **A)** Correct. Task (write a reply), context (the policy), format (3 sentences) and constraints (use only this policy).
- **B)** It has a task and context. Format and constraints are missing.
- **C)** It has a task only.
- **D)** It sets a tone but has no task, no context and no format.

---

## <font color='blue'>Closing: Outcome & Summary</font> `15 min`

Back to Rhea. We answer the Problem Statement using each topic once.

> <font color='purple'>**1. What kind of tool wrote the reply? (Topic 1)**</font>

A GenAI tool, specifically an LLM. It built the reply by next-token prediction, one piece at a time.

> <font color='purple'>**2. How much could it hold? (Topic 2)**</font>

Only what fits in its context window. The policy, the earlier chat and the reply all count against that limit.

> <font color='purple'>**3. Why was the reply fluent and wrong? (Topic 3)**</font>

It chose likely words, not checked facts. Temperature changes how much the picks vary, but it never adds the app's real rule.

> <font color='purple'>**4. How does Rhea ask next time? (Topic 4)**</font>

With a task, the policy as context, a format and constraints. Then she checks the reply against the policy line.

### <font color='green'>Outcome</font>

| | Rhea's first prompt | Rhea's four-element prompt |
|:--|:-:|:-:|
| Task | Yes | Yes |
| Context (the policy) | No | Yes |
| Format | No | Yes |
| Constraints | No | Yes |
| Can she check the reply? | No | Yes |

> <font color='green'>**Therefore,**</font> A chat tool builds replies token by token inside a limited context window. It can sound sure and still be wrong, so Rhea gives it the policy, a format and limits, then checks the answer herself.

> <font color="red">**🎯 Instructor Note**</font> Reveal the poll: no. A well-written reply is not more likely to be correct, because fluency comes from style and not from checking facts.

### <font color='green'>Summary</font>

| Learning objective | Takeaway |
|:--|:--|
| Compare AI, ML and GenAI | AI is the widest term. ML learns from data. GenAI creates new content |
| Next-token prediction | The model scores the next piece, picks one and repeats |
| Tokenizer and tokens | Text is cut into pieces, and one word can be several tokens |
| Context window | A fixed limit that counts the prompt, the chat history and the reply |
| Temperature | Higher temperature gives more varied output, not more accurate output |
| Hallucination | Fluent text can be false because the model continues patterns and does not check facts |
| Four prompt elements | Task, context, format and constraints |
| **Practical value** | Every AI reply you use at work should come from a clear prompt and be checked against a source you trust |

---

# <font color='red'>Launch the Feedback Poll</font>

> <font color="red">**🎯 Instructor Note**</font> Reminder: launch the feedback poll now to collect learner feedback.

