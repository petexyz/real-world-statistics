# Instructor Notes: Real-World Applications of Statistics
### Last Lecture -- Elementary Statistics

**Estimated total time:** 90-110 minutes
**Format:** Lecture with embedded discussion questions and optional live demos

---

## Pre-Class Setup

- Print one copy of the Quick-Reference formula sheet (last page of main doc) for yourself
- If doing the birthday demo (Section 9), have students ready to participate -- works best with 20+ students
- Recommended: have the GitHub-hosted version open on the projector in a browser so charts render at full size
- Optional: a whiteboard or tablet for sketching the confounding variable diagram live

---

## Overall Pacing Guide

| Section | Recommended Time | Notes |
|---------|-----------------|-------|
| Opening framing | 5 min | Set tone -- this is synthesis, not new material |
| 1. Clever Hans | 15 min | Spend time on the AI angle -- very current |
| 2. Okun's Law | 12 min | Can trim if running long |
| 3. Storks / Spurious Correlation | 12 min | Discussion question usually generates good debate |
| 4. Normal Distribution | 7 min | Fast pass -- they know this; use birthday demo hook |
| 5. Household Income | 10 min | Political discussion tends to ignite -- be ready to facilitate |
| 6. Survivorship Bias | 12 min | WWII story lands well; the investing chart is the gut punch |
| 7. Simpson's Paradox | 12 min | This one usually produces genuine "wait, what?" reactions |
| 8. Bayes / Base Rate | 12 min | Slow down here -- students need time to absorb the arithmetic |
| 9. Birthday Problem | 10 min | End with the live demo -- great closer |
| Closing synthesis | 5 min | Fast -- the 7 questions slide |

---

## Section-by-Section Notes

---

### Opening (5 minutes)

**Goal:** Frame the entire lecture as synthesis and celebration, not new content.

Say something like: *"Everything today you have technically seen before -- correlation, distributions, probability. What we are doing today is connecting the dots between those tools and the world you already live in. By the end of this class you will realize you have been thinking statistically for months without knowing it."*

**Do not** start with housekeeping. Start with the Clever Hans story directly -- it is immediately engaging.

---

### Section 1: Clever Hans (15 minutes)

**The story (4 min):**
Tell this as a narrative before showing any slides. The image works better as a reveal after students have formed a mental picture.

Key beats:
1. Von Osten was completely sincere -- he genuinely believed the horse could reason
2. Public demonstrations, scientific committees, all impressed
3. Pfungst's decisive experiment: vary whether the questioner knows the answer
4. The result: Hans could not answer questions the questioner did not know

Pause and let the implication land before moving on.

**Discussion prompt (optional, 2 min):**
"Before I tell you the explanation -- what is your hypothesis for how Hans was doing it?"

Students usually guess training/conditioning correctly. Then you can explain the micro-cue mechanism.

**Poker application (2 min):**
Brief -- just enough to illustrate that professional players have independently reinvented blinding as a strategic tool. The sunglasses/poker face example connects to something students know.

**AI application (5 min):**
This is the section that will matter most to this generation. Spend time on the feedback loop diagram. The key point: AI models are the most impressionable "subjects" ever created because they have no intrinsic priors -- they learn exactly what they are shown.

The discussion question ("why does ChatGPT confidently give wrong answers?") is worth 2 minutes of student response. The Clever Hans answer: the model learned from human-generated content, and humans have confident-sounding ways of saying wrong things. The model learned the pattern of confidence, not the truth.

**Formulas to mention:** The bias model $Y = \mu + \epsilon_{true} + \epsilon_{bias}$ does not need derivation -- just the concept that blinding tries to drive $\epsilon_{bias}$ to zero.

---

### Section 2: Okun's Law (12 minutes)

**Tone:** This is your cleanest "statistics describes the real world" section. Students have probably heard about GDP and unemployment in the news; most have no idea there is a formula connecting them.

**Lead with the scatter plot.** Let students read it before you explain it. Ask: "What does this shape tell you? What does the slope direction mean?" Let them identify the negative correlation themselves.

**Key teaching points:**
- The correlation is real but imperfect ($-0.9 < r < -0.5$) -- note the scatter. Real economic relationships are never clean.
- The scatter is not error or noise -- it is real variation from recessions of different types, different industries, different eras.
- The lag is the most pedagogically interesting part. This is where you can introduce the concept of time-series modeling without formally teaching it.

**The time-series chart:** Walk through the three recessions. Students recognize 2008 and 2020 viscerally. Ask: "Notice anything about the timing? Does unemployment peak at the same time as GDP hits its low?" (No -- it peaks later.) That is the lag in action.

**Common student question:** "Is Okun's Law a law?" Answer: No, it is an empirical regularity -- a well-supported rule of thumb, not a physical law. The coefficient changes over time and across countries.

---

### Section 3: Storks (12 minutes)

**This is the highlight of the lecture for most students.** The combination of an absurd correlation and a real $p$-value ($p < 0.01$!) reliably produces laughter and genuine engagement.

**Do not reveal the confounding variable immediately.** Show the scatter plot and the correlation coefficient. Ask: "What do we conclude?" Wait for someone to say "more storks cause more babies" or something equivalent. Then ask: "Is there any other possibility?"

**The teaching sequence:**
1. Show the correlation. Let it land.
2. Ask for alternative explanations. Students will usually get to "some third factor" quickly.
3. Reveal the confounding variable diagram.
4. Show why controlling for country size makes the correlation disappear.

**The breakfast grades example** (discussion question) is worth a few minutes. Common confounders students identify: family income, parental involvement, whether the child is hungry/distracted. These are all correct. This bridges to randomized experiments as the gold standard.

**Formula note:** You do not need to show the partial correlation formula. The concept -- "holding Z constant, does the X-Y relationship persist?" -- is sufficient for this level.

---

### Section 4: Normal Distribution (7 minutes -- fast pass)

**Goal:** Rapid but vivid recap, not a full re-teaching.

**Lead with a show of hands:** "How many of you are between 5'4" and 6'4"? [pause] That is the 95% interval -- $\pm 2\sigma$ from the mean. You just experienced a probability distribution."

The Central Limit Theorem explanation is worth 90 seconds: "Why does height follow a bell curve? Because it is the sum of hundreds of genetic and environmental factors. The CLT says that sums of many independent random factors tend toward normal. This is why the normal distribution appears everywhere in nature."

**The key connection:** The CLT is why our $z$-tests and $t$-tests work. Without it, hypothesis testing would require knowing the exact distribution of the population.

**Optional fast fact:** The tallest recorded person was 8'11" (Robert Wadlow). Using our height model, that is about $+9.7\sigma$ -- a probability of roughly $10^{-22}$. Some things are not normally distributed in the tails.

---

### Section 5: Household Income (10 minutes)

**Warning:** This section has political content. Frame it explicitly as statistical literacy, not advocacy.

Opening: "I am going to show you a fact about income statistics that politicians on both sides of the aisle use selectively. My goal is not to tell you what to conclude -- it is to give you the tools to notice when you are being given a number that serves an argument."

**The inequality $\text{Mode} < \text{Median} < \text{Mean}$** is the key formula. Write it on the board. Ask students to name a distribution where this holds (right-skewed). Ask them to name one where it reverses (left-skewed). Confirm their understanding.

**The Gini coefficient** is bonus material if you have time. The key insight: a single number summarizing the entire shape of the distribution -- analogous to $\sigma$ summarizing spread.

**Common student reaction:** "Why do they report the mean at all if it is misleading?" Answer: It is not wrong -- it is the correct mean. The issue is using it as a proxy for "typical," which it is not. The mean of income is very meaningful for calculating total tax revenue, for example.

---

### Section 6: Survivorship Bias (12 minutes)

**The WWII story is the best narrative in the lecture.** Tell it slowly and with drama.

Build-up: "You are an engineer in 1943. Bombers are being shot down. You examine 100 planes that came back. Here is the bullet hole map. Where do you reinforce?"

Wait for student answers. Most will say "reinforce where the holes are." Then deliver the Wald insight.

**The "absence of data is data" principle** is the philosophical core of this section. Spend a sentence on it: "Wald's contribution was realizing that the sample he was looking at was not a random sample of planes flown -- it was a sample conditioned on survival. He had to reason about what the missing data would look like."

**The investing chart:** The contrast between "survivor-only returns" and "all-fund returns" is visually stark. Ask: "If you saw a fund company advertise 8.2% average annual returns, and you knew about survivorship bias, what would you ask them?"

**The publishing/science angle** is important for students who will do research: "The replication crisis you may have heard about is partly a survivorship problem. Studies with significant results get published. Studies that find nothing significant do not. The literature is a biased sample of all experiments run."

---

### Section 7: Simpson's Paradox (12 minutes)

**This reliably produces the strongest "wait, how is that possible?" reaction of the lecture.** Do not rush it.

**Show the aggregate chart first.** Let students see the 44% vs. 35% gap and accept it as evidence of discrimination. Ask: "What do you conclude?" Then show the department-level charts. Watch the reactions.

**The explanation needs time.** The weighted average mechanism is subtle. Consider drawing it on the board:

- Women applied heavily to Dept A (30% acceptance rate for everyone)
- Men applied heavily to Dept B (60% acceptance rate for everyone)
- Aggregate average for women: weighted toward Dept A (low)
- Aggregate average for men: weighted toward Dept B (high)
- Result: women look worse in the aggregate even though they do at least as well everywhere

**The COVID vaccination example** is current and impactful. If students have heard the "more vaccinated people are hospitalized" talking point, this is the moment to address it directly with statistical reasoning.

**Key takeaway sentence:** "Simpson's Paradox is not a paradox at all once you see it. It is just what happens when you mix two groups with different base rates. The aggregate is a weighted average, and the weights are not equal. The lesson: always ask whether there are subgroup differences before interpreting an aggregate comparison."

---

### Section 8: Bayes' Theorem and Base Rate Neglect (12 minutes)

**This is the hardest section cognitively.** Slow down. The arithmetic matters.

**Start with the intuition pump:** "A test for a disease is 95% accurate. You test positive. What is the probability you have the disease?"

Take a few guesses from the class. They will typically be in the 80-95% range. Write them on the board. Then say: "The correct answer, for a disease that affects 1% of the population, is about 16%. Let me show you why."

**Work through the 10,000-person table line by line.** This is more intuitive than the formula for most students.

| | Has disease | No disease |
|---|------------|------------|
| Tests positive | 95 | 495 |
| Tests negative | 5 | 9,405 |

"Of 590 positive tests, only 95 are true positives. 95/590 = 16%."

Then show the Bayes' Theorem formula as the algebraic version of the same calculation.

**The criminal evidence example** often generates strong reactions. The "prosecutor's fallacy" -- confusing $P(\text{match}|\text{innocent})$ with $P(\text{innocent}|\text{match})$ -- has contributed to wrongful convictions.

**Discussion question:** "A news story says an AI cancer detector is 98% accurate. What is the first question you ask?" Answer: "What is the prevalence of the cancer in the population being screened?" A 98% accurate test applied to a condition with 0.1% prevalence will produce mostly false positives.

---

### Section 9: The Birthday Problem (10 minutes + live demo)

**Opening:** "Before I show you this chart -- how many people do you think need to be in a room for there to be a 50-50 chance of a shared birthday?" Take guesses. Write them down.

**Then reveal: 23.** Let the shock land.

**Walk through the logic:**
- The question is NOT "what is the chance someone shares MY birthday"
- The question is "what is the chance ANY two people share A birthday"
- With 30 people: $\binom{30}{2} = 435$ pairs. Each pair has a ~0.27% chance of matching. 435 opportunities compound rapidly.

**The live demo:** Ask students to say their birthdays out loud, one at a time, going around the room. Ask the class to shout "match!" when one is repeated. In a class of 25-30, a match typically occurs in the first 20-25 people. The moment it happens is always memorable.

If a match does not occur, note: "That happens about 30% of the time in a class this size. We beat the odds today -- but if we did this same experiment in ten classes of 30, we would see a match in about seven of them."

**The cryptography connection** is a strong closer for technically-minded students: "The security of hash functions in cryptography depends directly on the birthday problem. This is not a party trick -- it is at the heart of how digital signatures work."

---

## Closing: The 7 Questions (5 minutes)

End with the seven questions, read them slowly, and suggest that students write them down or take a photo.

These questions are the transferable product of the course -- the thing that remains useful after the formulas have faded.

Consider ending with: *"A statistical thinker is not someone who distrusts numbers. It is someone who knows exactly what questions to ask before trusting them. You now know those questions. That is not a small thing."*

---

## Potential Student Questions and Answers

**"Is Okun's Law still valid after COVID?"**
Good question. The 2020 recession and 2021 recovery were exceptional. Unemployment spiked far more sharply than Okun would predict (due to sudden shutdowns) and recovered faster than Okun would predict (due to stimulus and re-opening). Most economists believe Okun's Law still holds over normal business cycles but that COVID was outside the law's domain of applicability.

**"If Simpson's Paradox is always possible, how can we ever trust aggregate statistics?"**
You can trust aggregate statistics when you have accounted for known confounders and when the question you are asking is about the aggregate itself (e.g., total revenue, total admissions). Simpson's Paradox is a warning to disaggregate before making causal claims, not a reason to distrust all data.

**"Can Bayes' Theorem fix the problem with medical tests?"**
Yes -- this is exactly what it does. The solution is either to raise the base rate of people being tested (screen only high-risk populations) or to follow a positive test with a second independent test, which updates the prior probability dramatically.

**"How do we know survivorship bias is actually causing mutual fund returns to look better? Maybe the surviving funds are just better managed."**
This is a good critical question. The response: you can test it by tracking the performance of all funds from a starting date forward and comparing to funds-that-survived-only. The studies that have done this (Elton, Gruber, and Blake, 1996) find a substantial bias. Survivorship is the dominant explanation.

---

## Optional Extensions (if time permits)

- **The Monty Hall Problem:** Similar intuition-defying probability result; connects well after the birthday problem
- **P-hacking / multiple comparisons:** The probability of false discovery when you run many tests -- connects Clever Hans, publication bias, and hypothesis testing
- **The Prosecutor's Fallacy in detail:** More rigorous treatment of the DNA/criminal evidence Bayes application
- **Regression to the mean:** Why exceptional performance tends to be followed by more average performance -- connects to Okun's Law and has wide sports/business applications

---

*Instructor notes by Pete Halbeisen*
*Formatted for GitHub rendering*
