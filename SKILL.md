---
name: "math"
description: "Comprehensive standards for writing and self-grading mathematics/statistics solutions (Monash School of Mathematical Sciences writing guide). Use whenever drafting, revising, reviewing, or marking a maths/stats assignment answer, proof, derivation, or report. Enforces full-sentence explanations, correct notation, labelled diagrams, technical accuracy, and a mandatory 10-point self-scoring rubric that must reach 9/10 or higher. Final output is always delivered as a saved markdown (.md) file, with prose passed through the humanizer skill before saving."
---

# Math — Mathematical Writing & Solution-Quality Skill

Source: Monash University, School of Mathematical Sciences, "Guidelines for Writing in Mathematics" (Student Writing Guide, © Monash University 2015).

## When to use this skill

Use this skill any time you are drafting, writing, revising, editing, or marking a solution to a mathematics, statistics, or quantitative-science problem: assignment answers, exam-style solutions, proofs, derivations, worked examples, or short reports. Also use it when the user asks you to check, improve, tighten, or grade a piece of mathematical writing.

## Core principle

A correct final answer is never sufficient by itself. Full marks require ALL of the following simultaneously:

1. A clear description of the mathematics that justifies everything you do, written in full English sentences.
2. Evidence that you understand the mathematical ideas, not just that you can perform the calculation.
3. Neat presentation.
4. Understandability — a typical peer/student taking the same course could follow it without excessive effort.
5. Zero mistakes: mathematical, logical, typographical, or grammatical/spelling.

Keep answers clear, concise, and to the point. Never sacrifice explanation for brevity, and never pad with words that add no mathematical content.

## Mandatory deliverable: a markdown file

The output of this skill is never chat text alone. Every time this skill is used, the finished solution must be written to an actual `.md` file (via the Write/Edit tools) and saved into the user's workspace folder, not just printed in the conversation. The file must:

- Use a clear, descriptive filename (e.g. `q3-volume-of-revolution-solution.md`).
- Reproduce the full solution in Markdown, with the question restated at the top, headers separating stages of the argument where useful, and mathematical notation rendered cleanly (LaTeX-style inline/block math where the target renderer supports it, otherwise clean plain-text notation matching Appendix B below — never mix conventions within one file).
- Visibly satisfy every rule in this skill (full-sentence explanation, defined variables, labelled diagrams, technically correct, self-contained, little things checked) — the file itself is the artifact that gets judged against the rubric, not a paraphrase of it.
- End with the self-assessment line (rubric score) as a short note, unless the user has asked for a clean file with no meta-commentary — in that case keep the score-check internal but still perform it.

Deliver the file to the user with a link once saved; do not just paste the solution into chat and stop there.

## Mandatory workflow

Follow this loop every time this skill is invoked — do not skip the self-scoring step or the humanizing pass:

1. **Parse the question.** Identify exactly what is being asked, what final result is required, and — critically — whether the question specifies a required method (e.g. "use the addition and double-angle formulae", "using cylindrical shells"). If a method is specified and the question does NOT say "or otherwise", you MUST use that exact method, even if you know a faster or more elegant alternative. Using a different (even correct) method loses marks (see Appendix A, Answer 5 below).
2. **Set up before calculating.** State the aim/question, define every variable and any assumptions, and write one introductory sentence naming the method you are about to use (e.g. "I will use the method of cylindrical shells to find the volume of this solid").
3. **Draft the full solution** following the Six Writing Tips (below) line by line: narrate reasoning in full sentences, show every non-trivial step, use only correctly-meaning notation, label any diagrams/graphs, and finish with the result restated in a full sentence.
4. **Self-score the draft** against the 10-Point Rubric (below). Score honestly — do not round up. If the total is below 9/10: identify the specific lowest-scoring item(s), revise the draft to fix exactly those weaknesses, and re-score from scratch. Repeat this revise-and-rescore loop until the score is ≥ 9/10.
5. **Invoke the `humanizer:humanizer` skill** on the finished, rubric-passing draft — specifically on its explanatory prose (the full-sentence reasoning, setup, and conclusion text) — to strip AI-writing artifacts: stock phrases, inflated claims, repetitive sentence structure, filler transitions, and unnecessary hedging. Do this as an actual invocation (via the Skill tool), not a manual rewrite of humanizing rules. The humanizer pass must never alter any equation, numeric value, variable definition, notation, or the mathematical content/logic of the solution — only the surrounding prose style.
6. **Re-check items 1–5 of the rubric** on the humanized text (explanation present, notation still correct, logic still visible) — a style pass should not have removed substance, but confirm it didn't.
7. **Write the final version to the markdown file** described above and save it to the workspace folder.
8. **Deliver the file link**, followed by a one-line self-assessment, e.g. `Self-check: 9/10 — diagram fully labelled, all steps justified; minor: could restate final units more explicitly.` Omit the visible score line only if the user explicitly asks for a clean file with no meta-commentary — but still run the internal scoring loop silently.

## The Six Writing Tips (detailed)

### 1. Explain what you are doing
- Write a clear description of the mathematics, in full sentences. Do not use abbreviated "txt style."
- Write solutions the way you would give a running commentary of the process to a peer — include connecting phrases where they help ("since," "because," "this means that," etc.).
- Open your working with a simple sentence outlining what you intend to do (e.g. "I will use the method of cylindrical shells to find the volume of this solid").
- Calibrate detail to the assumed background of the course: trivial calculations and minor concepts don't need full explanation, but anything new must be explained.

### 2. Show all the important steps
- Sentences must communicate ideas clearly and be organised in an orderly, logical manner.
- Each new statement in a mathematical argument must follow logically from the previous one.
- Give a reason for what was done on each line, with enough detail that another reader can follow it and see that you understand what you are doing.
- Use paragraphs to separate important steps/stages of the argument.

### 3. Use correct mathematical notation
- Define all variables used and state any assumptions made (e.g. "Let x be the length and y the width of the box, measured in metres").
- Only use symbols whose meaning you are certain of. Different brackets mean different things: conventionally (x, y) is a coordinate/open interval, [x, y] is a closed interval, {x, y} is a 2-element set.
- **Never use mathematical symbols as shorthand inside sentences.** Symbols such as ⇒, ∴, ∀, ∃, or abbreviations like "iff" and "s.t.", must NOT replace words in prose. Write them out in full: "for all," "there exists," "implies," "if and only if," "such that."
- Only use arrows/logic symbols in a formal logic context, where they have fixed technical meaning.
- Never start a sentence with a symbol — this is considered poor form.

### 4. Present diagrams and graphs
- Give every graph a title and labelled axes (include units when graphing real data).
- Label important points: turning points on graphs; vertices and line segments on diagrams.
- Include standard conventions: direction arrows on vectors, tick-marks on congruent segments, etc.
- Include a legend whenever more than one data series is plotted on the same graph.
- Choose a sensible/appropriate scale — graphs need not start at zero, but the starting point must be clear.
- Number every diagram/figure sequentially (Figure 1, Figure 2, ...) and refer to them by number in the text ("as shown in Figure 1").
- Number formulas too, if you need to refer back to them later in the report.

### 5. Be technically correct
- No mistakes of any kind: mathematical, typographical, or grammatical.
- Be completely self-contained: state the problem at the start, and give a summary/statement of the result at the end of each question.

### 6. Remember the little things
- Include correct units wherever appropriate.
- Check that your final paragraph actually answers the question that was asked.
- Check that the answer makes sense (sanity-check magnitude, sign, domain, etc.).
- Note any limitations on the result or any additional assumptions that were required.
- Check spelling and grammar.
- Keep the work a clean copy — illegible handwriting/formatting means the content will not be credited.

## Commonly used words and phrases

Draw on this bank to keep transitions in full English rather than symbolic shorthand:

| | | |
|---|---|---|
| Therefore | Let … be … | This follows from … |
| Hence | This proves that … | Let …, where … is … |
| It follows that … | Using … we have … | Consequently |
| Then | After simplification, we find that … | As a result |
| In conclusion | | |

## Elements of a good mathematical / statistical / scientific report

Statistical and scientific reports follow the same overall outline as a mathematics solution:

1. State the question/aim.
2. Define variables.
3. Outline the technique(s) used.
4. State the result.
5. Check the validity of the solution and draw conclusions.

## Lessons from graded example answers

The source guide illustrates quality with one worked question — "Use the addition and double-angle formulae to derive an expression for sin(3x) in terms of sin x" — answered five different ways. The grading logic behind each generalizes to any problem:

- **Final-answer-only.** Correct result, no working shown. Earns only the small mark allocated purely to the final answer; loses all marks for method, reasoning, and notation. → Never submit bare final answers.
- **Steps shown but no explanation, and wrong notation.** Uses ⇒ and ∴ in place of "=" and as connectives with no prose reasoning. Partial credit for method at best; zero for notation and explanation. → Symbols are not a substitute for sentences; use "=" for equality and reserve ⇒/∴ for genuine logical implication in formal logic contexts only.
- **Mathematically correct but overly brief, with poor grammar.** Reads more like disconnected notes than an explanation; an uninformed reader couldn't reproduce the method from it. Gets marks for method and notation but zero for explanation. → Terseness that removes the ability of a peer to follow the logic is a failure, not efficiency.
- **Complete solution (the model answer).** Full sentences explain the reasoning behind every step; intermediate results used are explicitly named/stated with their source; the final answer is restated in a complete sentence at the end. → This is the standard to aim for on every answer.
- **Correct final answer via a different (unrequested) method.** Technically correct and well explained, but ignores the specific method the question required. Loses marks for not following the instructions given, even though the mathematics is valid. → Always match the exact method requested unless the question says "or otherwise"; if you also want to showcase an alternative method, complete the requested method first, then add the alternative as a clearly labelled bonus.

## Appendix: Common notation reference

Use this as the authoritative meaning-check before using any symbol. If a symbol used doesn't match this table, either fix it or spell out the words instead.

**Sets** — let A and B be sets

| Symbol | Meaning |
|---|---|
| x ∈ A, A ∋ x | x is a member of, is an element of, belongs to, or is in the set A |
| A ⊂ B | A is a subset of B (includes A = B) |
| A ∪ B | the union of sets A and B |
| A ∩ B | the intersection of sets A and B |
| A\B | the difference of sets A and B |
| A × B | the Cartesian product of A and B; written A² if A = B |
| {x : P(x)} or {x \| P(x)} | the set of x such that P(x) is true, e.g. {x : 0 < x < 1} |
| ∅ | the empty set |
| ℕ | the natural numbers (caution: sometimes 0 is included — check the convention in use) |
| ℤ | the integers |
| ℚ | the rational numbers |
| ℝ | the real numbers |
| ℂ | the complex numbers |

**Logic** — let P and Q be logical statements

| Symbol | Meaning |
|---|---|
| P ⇒ Q | P implies Q; P is sufficient for Q |
| Q ⇐ P | Q is necessary for P |
| P ⇔ Q | P holds if and only if Q holds; P and Q are logically equivalent |
| ¬P | the negation of P |
| P ∧ Q | P and Q |
| P ∨ Q | P or Q (or both) |
| ∃ | the quantifier "exists" |
| ∀x | the quantifier "for all" |

Reminder: these symbols are for use **within formal logic notation only** — never as connective shorthand inside ordinary explanatory sentences.

**Functions** — let A, B be sets, f : A → B a function

| Symbol | Meaning |
|---|---|
| f : A → B | a function with domain A, range (co-domain) B, and image f(A) ⊂ B |
| f⁻¹ | the inverse of f (if it exists) |
| f(a) | the image of a ∈ A under f |
| f⁻¹(b) | the preimage of b ∈ B under f |
| f ∘ g | the composition of two functions (g applied first, then f) |
| Bᴬ | the set of all functions from A to B |

**Probability** — let A, B be events, X a random variable

| Symbol | Meaning |
|---|---|
| P(A) | the probability of event A |
| P(A ∩ B) / P(A and B) | the probability of the joint event A and B |
| P(A ∪ B) / P(A or B) | the probability of event A or B (or both) |
| P(A \| B) | the conditional probability of A given B has occurred |
| E(X) | the expected value of X |

**Miscellaneous**

| Symbol | Meaning |
|---|---|
| ∞ | infinity |
| Σ (i=1 to n) xᵢ | the sum x₁ + x₂ + … + xₙ |
| Π (i=1 to n) xᵢ | the product x₁ · x₂ · … · xₙ |
| n! | n factorial (n a positive integer) |

Greek letters used in mathematics/science/engineering: refer to standard conventions if unsure of a specific letter's typical usage.

## 10-Point Self-Scoring Rubric (mandatory — target ≥ 9/10)

Score each item 1 (fully met) or 0 (not met); use 0.5 sparingly for "partially met." Sum for a total out of 10.

1. **Opening & method statement** — The solution states what is being asked and opens with a sentence naming the method/approach to be used, and that method is the exact one the question requested (unless "or otherwise" was stated).
2. **Variables & assumptions defined** — Every variable, symbol, and assumption is explicitly defined in full sentences before or as it is first used.
3. **Full-sentence explanation throughout** — Every non-trivial step is accompanied by prose explaining what is being done and why (not just equations in sequence).
4. **Logical step-by-step progression** — Each new mathematical statement follows logically and visibly from the previous one; paragraphs separate major stages of the argument.
5. **Correct notation, no symbol-as-shorthand** — No use of ⇒, ∴, ∀, ∃, "iff", "s.t." etc. as substitutes for words in ordinary sentences; no sentence starts with a symbol; brackets/set notation used with their conventional meaning.
6. **Diagrams/graphs correctly presented** — Any diagram or graph has a title, labelled+unit-ed axes, labelled key points, appropriate legend, sensible scale, and a sequential figure number referenced in text. (If no diagram is needed for this problem, mark this item as automatically satisfied — 1 point.)
7. **Technically correct** — No mathematical, logical, typographical, or grammatical/spelling errors anywhere in the solution.
8. **Self-contained with stated result** — The problem/question is restated at the start and the final result is restated in a full sentence at the end (not left as a bare final equation).
9. **Little things checked** — Correct units included; the final answer is sanity-checked (magnitude/sign/domain); limitations or extra assumptions are noted if relevant; spelling/grammar re-checked.
10. **Clean, appropriately concise presentation** — Neatly organised, legible, and matches the register of the model answer (Appendix A, Answer 4) rather than being either bare (Answer 1/2) or under-explained despite being correct (Answer 3). Prose reads naturally (post-humanizer pass), not like templated AI output.

### How to apply the rubric

- Score every item honestly against the actual draft, not against intent.
- List which items scored below 1 and why, in one short phrase each.
- Revise the draft to directly address every sub-1 item, then re-score the whole rubric again (not just the fixed items — a fix can sometimes introduce a new gap elsewhere).
- Repeat until total ≥ 9/10. If, after a genuine revision attempt, a specific item structurally cannot reach 1 (e.g. the question truly has no method to name because it's a pure numeric lookup), state that explicitly as N/A and still award the point rather than leaving an unexplained gap.
- Only after the score reaches ≥ 9/10 do the humanizer pass (workflow step 5) and then write the final `.md` file.
- Report the final score to the user alongside the file link unless they've asked for a clean, rubric-free response.

