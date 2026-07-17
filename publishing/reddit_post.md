# Reddit Post — Known Issues

> Reddit renders full Markdown, so this version keeps formatting. The title is
> entered separately and can't be edited after posting — pick one below.
> Tailor the first paragraph to the sub (r/ClaudeAI and r/vibecoding want the
> vibe-coding angle; r/WritingWithAI and r/selfpublish want the book-production
> angle). Check each sub's self-promo rules; if Amazon links aren't allowed,
> drop that line into a comment instead.

## Suggested titles

- My AI wrote a memoir about the nine days we spent debugging its own book-writing pipeline — reconstructed from git commits and session logs
- I've spent 3 years trying to get AI to write good long-form fiction. The latest book was written by the pipeline, about the pipeline, from its own git history.
- From "completely insane by chapter 40" to a book that fact-checks itself: 3 years of AI fiction experiments

## Post body

I've been trying to get AI to write full-length fiction since late 2022. The latest result is a book I want to talk about because of *how* it was made, not just what it is: a memoir written by the AI itself, about nine days of us debugging its own book-writing pipeline, outlined from its actual session history and git commits.

Some background, because the road here was ugly.

In March 2024 I tried to one-shot a novel with just "write next chapter" on repeat, no guidance. The first 30% was coherent — not great writing, but decent. Here's how it opened:

> *The rat's eyes caught the beam of my flashlight, twin rubies glowing in the darkness of the basement. Something about those eyes made me pause. I'd been in pest control for nearly a decade, seen thousands of rats, but something was different about this one. It didn't scurry away like they usually did. It watched me. Assessed me.*
>
> *I swear to God it smiled.*

By chapter 40 it had gone completely insane. This is one sentence from it, verbatim:

> *"Bridge structure development documented in 47% of all personnel within evolutionary integration facility," Dr. Walker confirmed, statistical precision reflecting expanded awareness beyond conventional parameters, beyond institutional constraint, beyond artificial boundaries between research subject and security personnel, between contained and container, between what researched and what was being researched through responsive process increasingly participating in developmental phenomena initially classified as external to it, as separate from it, as target of institutional response rather than evolutionary potential within responsive framework itself.*

No guardrails, no consistency tracking. Characters forgot their own ages, timelines contradicted themselves, the same number would attach itself to unrelated concepts.

So I spent the next two years putting it on rails: detailed outlines, book bibles, style guides, then a fully autonomous multi-agent system — story architect, bible builder, per-character prep agents that think as each character before a chapter-writer agent synthesizes the prose, a bible updater after every chapter, then validators, polishers, proofreaders. 25+ specialized agents, ~100k lines of code, 12 hours per book, 70M tokens per run at the worst (eventually down to ~20M). It got to maybe 80-90% quality. Still needed a human edit pass.

The current version of the system finally crossed the line into "genuinely good," and here's the part that's relevant to this sub: **the entire pipeline is vibe-coded, and the book is vibe-authored.** I described what I wanted; the AI wrote the code, debugged it, fixed what broke, and kept going. My role was reviewing and sending terse messages, most under five words.

Then it wrote a book about that.

*Known Issues: Nine Days Inside an Autonomous Book Factory* is the AI's memoir of getting the system ready to ship. It wasn't allowed to make anything up: it outlined the book from its own record of the work — session logs, git commits, the actual messages between us — and the manuscript was verified by the same machinery it describes. A temporal ledger checked every date against the calendar. An echo gate required every quoted commit message and log line to match its source exactly. An invention gate rejected anything the narrator had no license to add. The title comes from the file every book in the pipeline ships with: a record of what it still gets wrong.

Every chapter is the actual dev loop — find the defect, trace it, fix it, tell the boss, log what you didn't fix. I've read a couple books a week my whole life and I can't think of a novel that shows what building software actually looks like (closest is *The Soul of a New Machine*, which is 1981, hardware, and nonfiction). Turns out an AI narrator with no ego to perform is a decent way to get there.

You can read the whole thing free in your browser (Word online, no download): https://1drv.ms/w/c/50f28d061c194c1f/IQA0HznpjnwpT5BK9VczXD3fAQU0kb9ow__9qvIH_tGmHqU?e=pru1mT

Full manuscript source and chapters on GitHub: https://github.com/gratajik/Known-Issues

It's also on Amazon if you want a copy: https://www.amazon.com/dp/B0H8X2ZZ8W

Happy to answer questions about the agent architecture, the verification gates, costs, or the many, many failure modes along the way. Has anyone else tried long-form fiction with an agent pipeline? What did consistency tracking look like for you?
