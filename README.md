# goldman sachs coding interview questions: what the OA, CoderPad screen and Superday actually ask, and how to prep by pattern instead of grinding

Goldman Sachs doesn't ask exotic questions. That's the part most candidates get wrong. They go looking for a secret Goldman question bank, and what they find instead is a loop that runs on a fairly narrow band of patterns — arrays, hash maps, string DP, tree traversal, sliding window — plus a second layer of design and process questions that has nothing to do with LeetCode.

The difficulty isn't the algorithm. It's the format: a proctored assessment under time pressure, a live CoderPad screen where someone is watching you debug, and a Superday that stacks three to five interviews into one day and compares your answers across all of them.

Here's what the process looks like, what's actually been reported by candidates, and where the prep time is best spent.

## The loop, stage by stage

Goldman's engineering pipeline is roughly consistent across reports, though the exact number of rounds shifts by role and office.

| Stage | Format | Reported length | What it measures |
| --- | --- | --- | --- |
| Online assessment | HackerRank, 2–3 problems | 60–120 minutes | Data structures, basic algorithms |
| HireVue (mostly campus) | Recorded video, ~5 questions | Around 2 minutes per answer | Motivation, communication |
| Technical screen | Live coding on CoderPad | 45–75 minutes | Working code, testing, explanation |
| Superday | 3–5 interviews back to back | 45–60 minutes each | Coding, low-level design, SDLC, behavioral |
| Team fit / MD | Conversation | 30–45 minutes | Fit, judgement, career narrative |

Goldman's own campus hiring FAQ describes the technical test as a one-hour, proctored assessment run through HackerRank and Zoom, with cameras required for the full duration. Experienced-hire reports put the assessment closer to two hours with two medium problems. Either way, the content skews easy-to-medium — the pressure comes from hidden test cases, not from problem difficulty.

One scheduling detail worth building around: candidates report Superdays cluster between August and December, with cohorts of roughly 24 to 32 people interviewing on the same day. That means you're evaluated relative to the room, and your prep needs to be finished before the earliest cohort dates, not in the week you get the invite.

## The online assessment: partial credit is your friend

Two or three problems, arrays and strings and hash maps, occasionally a light dynamic programming question. The commonly reported failure mode isn't "couldn't solve it" — it's a correct solution that dies on an edge case.

A Q2 2025 breakdown cited by one interview-prep analysis put a third of assessment failures on missing null or empty-input checks. Whatever the exact number, the pattern matches what candidates write in their own debriefs: passed most cases, failed the empty array. Submit a working slow version for every problem, handle the empty input, and you keep partial credit even when you don't finish the optimal solution.

## The CoderPad screen is a conversation with code attached

The live screen typically runs like this: brief introductions, a resume walkthrough, then one or two problems where you write code in the shared editor, run it against test cases, and explain the tradeoffs.

Reports from candidates who cleared it emphasize the explanation more than the code. A typical accepted experience describes two easy problems — a hash map counting question and reversing a linked list — solved and run with a few test cases. A rejected one describes solving the main problem but leaving the empty-array case unhandled because time ran out.

Two things recur in the successful write-ups:

- Interviewers ask whether your code is production-ready, then push on what would break it.
- Follow-ups land on complexity and on why your approach beats the obvious one.

Goldman interviewers are working engineers, and the round format rewards someone who can narrate what they're doing while doing it.

## Superday: one day, four different evaluations

Superday is where the loop widens. Candidates consistently report three to five rounds covering:

- **DSA** — usually two problems, medium difficulty, occasionally hard (a long-path tree question with LCA follow-ups shows up in accepted write-ups)
- **Low-level design** — LRU cache, Splitwise-style expense splitting, a bus ticketing system, a document snapshot design
- **Software engineering practice** — testing strategy, code review, deployment risk, concurrency questions
- **Behavioral** — projects, ownership, why this firm

The rounds are graded by different people who compare notes afterward. Candidates who passed describe keeping the same stories and the same numbers consistent across every room. Changing details between interviewers is one of the clearer ways to create doubt.

After Superday there's a stage most candidates don't know about until it's happening: individual teams assess fit independently. If one desk passes, another can still pick you up without restarting the process. That's why two or three weeks of silence after Superday isn't the same as rejection — a point several candidates have made specifically because they misread it.

## The questions that keep showing up

These are problems named in candidate debriefs and public interview write-ups. None of this is a leaked question bank; it's what people reported being asked.

| Reported question | Pattern it actually tests |
| --- | --- |
| Decode Ways | 1-D DP with counting |
| Minimum Path Sum, reversed to find the maximum path | Grid DP |
| Sliding Window Maximum | Monotonic deque |
| Target Sum | Subset DP / memoization |
| Maximal Square | 2-D DP |
| Maze II | BFS with a priority queue |
| Distinct Subsequences | String DP |
| Trapping Rain Water | Two pointers or monotonic stack |
| LRU cache with a TTL eviction policy | Hash map + doubly linked list, plus design |
| Sort a 2 GB file with 250 MB of RAM | External sort, merging k sorted lists |
| First non-repeating character | Hash map counting |
| Run-length string compression | Two pointers |
| Unique substrings of a fixed length | Sliding window with a set |
| Most frequent log entry or IP | Hash map counting |
| Maximum rocks on a grid path | Grid DP |
| k toys, n students in a circle | Arithmetic and modular indexing |
| Design a HashMap from scratch | Hash table internals, collision handling |

Read that list as a syllabus and something becomes obvious: it's maybe six or seven underlying patterns wearing different costumes. Grid DP, 1-D DP, sliding window, monotonic stack, hash map counting, BFS/DFS, and linked-list-plus-map design. Nine of the seventeen entries map to just four of them.

Most candidates discover this after they've already burned three weeks on 150 random problems.

## What a pattern-first approach changes

This is where the structure of the prep matters more than the volume. [AlgoMonster](https://algo.monster?fpr=li69) is built around that idea — the curriculum is organized by pattern rather than by problem number, so each problem you solve is attached to a reusable template and a set of decisions about when to apply it.

What a Pro subscription currently unlocks, per the subscribe page:

- All patterns, lessons and problems
- Unlimited AI assistant usage for Q&A and debugging help
- Unlimited Speedrun sessions — timed practice rather than casual solving
- Interview questions tagged by company, refreshed monthly
- 500+ lessons across 6 courses, 1,000+ illustrations, 3,000+ editorials
- A member discount on live bootcamps
- Two included bonus courses: a CS fundamentals course and a "build an LLM" course

The format is text and interactive diagrams, not video. If you learn by watching someone else code, this will feel like the wrong tool. If you retain better by reading a template, seeing the diagram, then applying it under a timer, the format is doing the work most video courses skip.

👉 [See the current pattern library and plan pricing](https://algo.monster/subscribe?fpr=li69)

## AlgoMonster plans and prices

The subscribe page currently shows four options, including the free tier:

| Plan | Price | Billing | What you get | Get it |
| --- | --- | --- | --- | --- |
| Free | $0 | — | Limited access to a subset of patterns and problems | [Start with the free tier](https://algo.monster?fpr=li69) |
| Pro — Monthly | $18.99/month | Billed monthly, cancel anytime | Full pattern library, unlimited AI assistant, unlimited Speedrun, company-tagged questions | [Choose Pro Monthly](https://algo.monster/subscribe?fpr=li69) |
| Pro — Yearly | $99/year ($8.25/month) | Billed annually, 12 months of access | Everything in monthly, plus 12 months of full access and a bootcamp member discount | [Choose Pro Yearly](https://algo.monster/subscribe?fpr=li69) |
| Pro — Lifetime | $189 | One-time payment | Everything in the annual plan, plus lifetime updates | [Choose Pro Lifetime](https://algo.monster/subscribe?fpr=li69) |

A few honest notes on those numbers, because pricing pages for prep platforms move around:

The annual plan works out to roughly $8.25 a month, which is about half of what a single month costs at the monthly rate. AlgoMonster runs promotions periodically and the displayed price fluctuates with them, so check the page rather than trusting a number from a blog post — including this one.

There's no team or enterprise tier. It's an individual prep product, and the free tier is small enough to evaluate the teaching style but not enough to interview with.

## Which plan fits a Goldman timeline

Goldman's Superday window is the variable that matters here.

If you're targeting a campus or internship pipeline — assessment in the fall, Superday between August and December — a monthly plan covering your actual prep window is often the cheapest honest option. Six weeks of study at $18.99 is under $120, and you can cancel when the loop ends.

If you're an experienced hire running a job search across several months, the yearly plan at $99 is straightforwardly cheaper than five months of monthly billing. That math isn't close.

Lifetime at $189 is a different question. Two years of annual billing costs $198, so if you expect to interview again within a couple of years — which is normal for engineers who change jobs every two to three years — the one-time payment pays for itself. If this is a single focused push before a job you intend to keep for a decade, the yearly plan is the better use of the money.

👉 [Compare the monthly, yearly and lifetime options](https://algo.monster/subscribe?fpr=li69)

## A prep schedule that matches Goldman's calendar

Reports consistently describe candidates finishing a structured pattern course in four to eight weeks at one to two hours a day. Working backward from an August Superday, here's a schedule that fits:

**Weeks 1–2 — patterns, not volume.** Work through array, string, hash map and two-pointer material. For each pattern, write the template down in your own words. You're building recognition speed, not problem count.

**Weeks 3–4 — the DP and tree blocks.** This is where Goldman problems actually cluster. Grid DP, 1-D DP, string DP, then tree traversal with LCA and path questions. Use Speedrun sessions to force yourself to solve under a timer instead of drifting.

**Week 5 — assessment simulation.** Two problems in 60 minutes, submitted with edge cases handled. This is closer to the real pressure than untimed practice, and the failure mode you're training out is the empty input.

**Week 6 — the non-DSA half.** Low-level design practice with class boundaries and extension points: LRU cache, expense splitting, ticketing. Then SDLC conversations — how you test, how you think about deployment risk, how you'd approach a production incident. Candidates who only did algorithm prep report noticing this gap in the room.

Throughout: behavioral stories with numbers, written down once and reused verbatim across every round.

## Where candidates actually lose the offer

The debriefs are unusually consistent about failure points, and almost none of them are "the problem was too hard."

- **Edge cases over optimal solutions.** Working code with handled empties beats a clever solution that crashes.
- **Ignoring the engineering-practice half of Superday.** Testing strategy, code review, concurrency. Candidates who walked in expecting pure DSA got caught by it.
- **Inconsistent stories across rounds.** Interviewers compare notes. Keep your numbers the same.
- **Misreading silence as rejection.** Team matching after Superday can take weeks, and one team passing doesn't end the process.
- **Starting too late.** If your prep isn't done before the earliest cohort dates in August, you're studying during the loop.

## FAQ

**Are Goldman Sachs coding questions hard?**
Mostly no. Easy-to-medium difficulty dominates the assessment and the technical screens, with occasional hard problems in Superday tree rounds. The bar is breadth — coding plus design plus process questions — rather than peak difficulty.

**What language should I use?**
Reports describe Java as common, with requests to switch to C++ or Python generally accommodated in the live rounds. Use whatever you can write bug-free under a timer.

**How long does the whole process take?**
Reports range from about three weeks to a month end to end, with the caveat that gaps between stages can stretch. Ask the recruiter for the timeline instead of assuming one.

**Is AlgoMonster enough on its own for Goldman?**
It covers the coding half well and includes introductory system design and behavioral material. For an experienced-hire loop with dedicated design rounds, most candidates pair a pattern course with separate system design prep.

**Do I need the paid plan?**
The free tier is enough to see whether the text-and-diagram teaching style clicks. It isn't enough to cover the pattern list before an assessment.

The honest summary for anyone searching these questions: the list of Goldman problems is shorter than it looks, and the pipeline rewards people who've drilled the patterns behind it plus the engineering-practice questions nobody expects. Pick six patterns, learn them properly, and spend the last week on design and process instead of a hundred more problems.

👉 [Start with AlgoMonster's free tier and see the full curriculum](https://algo.monster?fpr=li69)
