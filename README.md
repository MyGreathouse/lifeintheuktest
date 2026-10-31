# Life in the UK Practice Test

Free practice for the Life in the UK Test: **15 mock exams, 608 questions with explanations**, study guides for all five handbook chapters, and instant results. No sign-up required.

**Live site:** https://www.youruklifetest.co.uk

---

## What it offers

- **15 timed mock tests.** Each has 24 questions and a 45-minute timer, like the real test. The pass mark is 18 out of 24 (75%).
- **608 original questions** across seven topics: values, What is the UK, early history, modern history, society, government, and law and your role. Every answer has a short explanation.
- **Study Centre.** Lessons with exam traps, memory anchors and cheat-sheet tables.
- **Progress tracking.** Scores, weak topics and a Mistake Bank, saved only on the visitor's own device.
- **Written guides.** A test guide, FAQ, study guide and topic question pages.

## How it works

This is a static website with no build step, no backend and no accounts.

| File | Purpose |
|---|---|
| `index.html` | The practice app (tests, study lessons, progress). |
| `mock-test.html`, `study-guide.html`, `test-guide.html`, `test-revision.html` | Guide and revision pages. |
| `history-questions.html`, `government-questions.html`, `questions-and-answers.html` | Topic question pages. |
| `faq.html`, `editorial-policy.html` | Help and content policy. |
| `privacy-policy.html`, `contact.html` | Privacy policy and About and Contact. |
| `sitemap.xml`, `robots.txt`, `ads.txt` | Search and advertising files. |

Progress is stored in the visitor's browser (localStorage) and is never sent to a server.

## Updating the questions

The question bank and mock tests are stored inside `index.html`:

- `const Q` holds all questions. Each has an `id`, a chapter (`ch`), the question `text`, four options (`A` to `D`), the `correct` letter, a short `why`, and a difficulty (`EASY`, `MEDIUM` or `HARD`).
- `const SETS` lists the 15 mock tests as 24 question positions each.
- Question IDs run in order (`q0`, `q1`, and so on), and a question's ID number matches its position in `Q`. When adding questions, add them at the end.

After changing the file, commit it to `main`. Vercel then redeploys automatically.

## Content and accuracy

All questions and lessons are written in our own words, based on the official Life in the UK handbook. Always check current test rules and fees on GOV.UK before you book. See the [Editorial Policy](https://www.youruklifetest.co.uk/editorial-policy.html).

## Hosting

The site is deployed on Vercel from the `main` branch of this repository. The domain and DNS are managed through Cloudflare.

## Corrections and contact

Found a mistake or have a suggestion? Email **admin@risten.co.uk** with the page and what you found, or use the [Contact page](https://www.youruklifetest.co.uk/contact.html).

## Disclaimer

Produced by Risten Global Ltd (YourUKHelpDesk). This is an independent revision resource. It is not affiliated with, endorsed by or connected to the Home Office or the UK Government.
