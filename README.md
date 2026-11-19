# AttemptSafe

An independent, synthetic demo of a safer review step before a Mains answer is submitted for evaluation.

**Not connected to SuperKalam.** All pages and reading text are fictional fixtures. There is no OCR, no evaluator and no real allowance.

## Why this exists

I tested the public Mains evaluation flow with my own free account (November 2026). Reading was accurate and word counts matched. At the review step before the final Submit I saw:

1. The back arrow and Cancel both discarded the whole upload.
2. A one page upload of a two page answer was evaluated with no warning I could see.
3. A nonsense question with the wrong paper selected was accepted and scored 0/10, although the upload window had suggested the correct question.

These come from a few tests on one account. They show nothing about how often learners hit them, what Cancel does to an allowance, or how the evaluator reads an answer.

## What the demo does

1. **Files:** choose paper, question and an optional expected page count. Add, remove, replace and reorder fictional pages. Going back keeps the draft.
2. **Review:** shows a check before submit list (paper, question, pages), the word count and the read only text. It flags a page count that differs from the expected count, a question that does not match the text, and a paper that does not fit the topic. It has three separate actions: Back to files (draft saved), Discard draft (with a second confirmation), Submit for evaluation.
3. **Receipt:** shows exactly what was submitted, with a timestamp. Submitting the same version again returns the same receipt and records no second unit.

Any change to the files creates a new draft version and clears the confirmation.

## Demo rules (my assumptions, not SuperKalam policy)

1. Three fictional units. One is recorded when a simulated submission is accepted.
2. The paper and question checks are simple keyword rules, written for this demo.
3. State is kept in the browser's localStorage. Use Reset demo to clear it.

## Try these

1. **Declared 2 pages, supplied 1:** leave expected at 2 with only Page 1, then open Review.
2. **Replace one page:** click Replace on Page 2 and check that Page 1 is untouched.
3. **Back versus discard:** go back from Review and confirm the draft is still there, then discard and confirm it is gone.
4. **Unrelated question:** type random letters as the question and open Review.
5. **Same version twice:** submit, then use Submit same version again.

## Look and feel

Light colours and rounded controls, chosen to sit close to the public SuperKalam site. No SuperKalam logo, text or assets are used.

## Run it

Open `index.html` in a browser. There is no build step.

## Deploy on Vercel

1. Create a GitHub repository and upload `index.html` and `README.md`.
2. In Vercel, choose Add New, then Project, and import the repository.
3. Framework preset: Other. Leave build settings empty. Deploy.

## Limits

No live OCR, no real submission, no accounts or server. A real version would need server side drafts, versions, receipts and accounting.

## How it was made

AI tools helped generate the first version of this code. The findings, scope decisions and testing are mine. (Edit this section to say what you personally changed.)

## My changes

(Write the exact change you made and why, for example: I renamed Back to "Back to files (draft saved)" because I worried Back would delete my work.)

I have not put SuperKalam screenshots in this repository.
