## <span style="color:#2F7DDE">Window Functions and Ranking</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Window Functions and Ranking"]
  Q["<b>The Big Question</b><br/><i>How can every student keep a row and still get a total and a rank?</i>"]
  CV["<b>Course use case</b><br/>A fantasy cricket league where one player showed 4.6 percent instead of 20.0 percent of team points"]
  RL["<b>Real-world example</b><br/>A school sports day board with house points, tied racers and the top 2 in each house"]

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

Have you ever wondered how a sports day board shows each student's points and the house total on one line?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Describe**</span> how the board keeps all 3 Red house rows and still shows the house total of 250.
- <span style="color:#D9660B">**Predict**</span> the rank of Chitra when Asha and Bilal tie at 90 points.
- <span style="color:#D9660B">**Calculate**</span> the Red house share for Chitra, who scored 70 of 250 points.
- <span style="color:#D9660B">**Determine**</span> the top 2 students in each house from one ranked list.
- <span style="color:#D9660B">**Compare**</span> three ways to number tied students: 1, 2, 3 or 1, 1, 3 or 1, 1, 2.
- <span style="color:#D9660B">**Check**</span> why a share of 18 percent is wrong when 28 percent is the right figure.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> OVER vs GROUP BY, window aggregate, ROW_NUMBER RANK and DENSE_RANK, ties in ranking, top N per group, PARTITION BY errors.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

Mr. Thomas keeps the sports day board. Each student has a row with a house and race points. He wants each row to show the house total too. A totals list gave one line per house, and the student rows vanished. Two racers tied on 90 points. The board gave them different places, and a parent complained.

A <span style="color:#D9660B">**window**</span> means a group of rows that you can total or rank while every row stays on the list.

In this course, you will add totals and ranks beside each row and pick the top students in each group.

> <span style="color:#2F7DDE">**Think about it:**</span> Why did the student rows vanish when Mr. Thomas asked for house totals?

---

### <span style="color:#2F7DDE">Sports Day Board Puzzle</span>

Here is part of the board.

| Student | House | Race points |
|:----------:|:----------:|:----------:|
| Asha | Red | 90 |
| Bilal | Red | 90 |
| Chitra | Red | 70 |
| Dev | Blue | 80 |
| Esha | Blue | 60 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Each student row shows the house total beside it.
- Tied racers get a place that Mr. Thomas can explain.
- The board lists the top 2 students in each house.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - What place should Chitra get if Asha and Bilal both take first?
> - What happens to a share if you divide by the points of both houses?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. The Red house has 90, 90 and 70 points. What is the Red total?**
Hint: Add the three scores.

**2. Chitra scored 70. What share of the Red total is that, in percent?**
Hint: Divide 70 by the house total, then multiply by 100.

**3. Asha and Bilal tie in first place. What are two fair places for Chitra?**
Hint: One answer skips a number and one does not.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How can a list keep every row and still tell each row where it stands?**</span>
>
> Which rule for tied students would you explain to the parents?
