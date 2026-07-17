# Foreword

## Greg's Foreword (July 12, 2026)

The AI took some creative latitude in describing what it was doing. A lot of the events are stretched longer than they actually took — usually minutes, not hours — and it never really stopped to rest the way the book implies. If you vibe code, you'll probably pick up on this; it's intentional :) I DID draw the line at making coffee (yeah, it actually wrote that at one point!). It almost feels like I have a human I've outsourced to — which, in a lot of ways, is true. The process, the thinking, and the coding it did are what I would have done myself, just MUCH faster. Oddly enough, it might be one of the best stories out there about a programmer (the AI) and his manager (me) working together to write software. Likely boring for many, but interesting as a dev to read!


I've been fascinated with using AI to create creative work for a while now. I started with art - I paint abstract oils, so it was a natural question: "Can AI CREATE art? Good art? Art humans respond to and like?" At the time (early 2023?) the answer was "kind of, but not great." While I didn't pursue that for long, I've recently been in awe of how good it's gotten...

I instead started trying to write stories with it - short ones, with the hope of eventually doing full-size fiction books (300+ pages). I'd written two books pre-AI.

In December 2022, I started experimenting in the ChatGPT web interface. Could it write a page? Two? The answer was "yes, but not well." I kept trying as new models were released, up until March 2024.

At the end of March 2024, I decided to one-shot a full book. I'd been vibe coding, so I thought I'd see what Cline + GPT could do. The approach was simple: initial prompt, then repeated "write next chapter." I wanted to see what would happen with almost no guidance.

The first 30% was coherent and okay. Not great writing, but decent. By the end it had gone completely insane.

Here's how it started:

*The rat's eyes caught the beam of my flashlight, twin rubies glowing in the darkness of the basement. Something about those eyes made me pause. I'd been in pest control for nearly a decade, seen thousands of rats, but something was different about this one. It didn't scurry away like they usually did. It watched me. Assessed me.*

*I swear to God it smiled.*

*"Fuck me," I muttered, shifting the weight of the chemical sprayer on my back. My voice echoed in the damp basement of the Pike Street apartment building. The smell down here was the usual cocktail of mildew, rust, and rat piss, but with something else underneath. Something metallic. Something wrong.*

And here's what Chapter 40 looked like:

*"Bridge structure development documented in 47% of all personnel within evolutionary integration facility," Dr. Walker confirmed, statistical precision reflecting expanded awareness beyond conventional parameters, beyond institutional constraint, beyond artificial boundaries between research subject and security personnel, between contained and container, between what researched and what was being researched through responsive process increasingly participating in developmental phenomena initially classified as external to it, as separate from it, as target of institutional response rather than evolutionary potential within responsive framework itself.*

That's one sentence. No guardrails, no consistency tracking. Just insanity!

In March and then April 2025, I started putting it on rails. Detailed outline, chapter outlines, book bible, detailed initial prompt. I'd review each chapter and push back with revisions. The biggest problem was full-book consistency: story arcs drifted, characters forgot things from previous chapters, numbers contradicted themselves. A character who was 45 would reference "thirty years of medical education." Timeline day counts went wrong in later chapters. The same specific number would show up attached to completely unrelated concepts. I published several books this way. All Cline + GPT. Decent results.

June 2025. I took everything I'd learned from the manual process and formalized it. I'd been using memory-bank for vibe coding, so I forked it into book-memory-bank with a proper book bible, style guide, story tracker, the works. The books got progressively better, edging into what I'd call "good" by fall 2025. Published a number of them. Cline + GPT, then Claude Sonnet (Sonnet was awesome).

November 2025. I decided to go big. I took everything I'd learned and built a fully autonomous multi-agent, multi-model system called bookgen. You'd feed it a concept (several pages, usually) and a few hours later it would spit out a 300-page book. The system ran through five phases: a story architect agent would generate the outline, a bible builder would create character sheets and world-building docs and a style guide, and then the real trick: for every chapter, individual character agents would prepare for their scenes from their own perspective (emotional state, secret goals, key dialogue lines in their authentic voice, physical tells), and a master chapter-writer agent would synthesize all those character preps into the actual prose. After each chapter, a bible updater would track what changed so the next chapter's agents would know what had happened. Then a final manuscript reviewer, a validator, a prose polisher, a style validator, a proofreader... 25+ specialized agents in total, with checkpointing every 5 chapters so you could resume if something crashed.

This was FRUSTRATING. The character-prep approach genuinely worked for voice consistency. Characters sounded like themselves because separate agents were thinking as them before the writer ever touched the chapter. But I could only hit something like 80-90% quality. It still needed a human edit pass (well, human + AI... I'd perfected some "publisher ready" prompts by end of year). 100k lines of code, 12 hours per book, burning 70 million tokens (eventually down to ~20 million). I was 100% focused on quality, not speed or cost. Published a few books. One (*Becoming Real*) is, I think, genuinely good.

February 2026. I started vibe coding with Claude Opus 4.6 + Claude Code. Amazing reasoning and quality. It could run for a long time without losing coherence. So I decided to one-shot a book again. Result: not sure if I should laugh or cry.

With some caveats... it worked. Really well.

I've since published a number of books that are, I believe, genuinely good: *Trap Door*, *Pip*, *Claw*, *Emergent*, plus a rewrite of that first insane rat book from 2024 (*GNAW!*). It wrote a GOOD version. No insanity.

I've now taken that learning and started a new fully autonomous multi-agent, multi-model system. I've been working on it since January (wow! time flies!). It's gotten better and better - speed up, quality up, and costs have finally come down. I wrote a full website around it that anyone can use. I've been using it to write books almost non-stop (over 30 published now; I've lost track of how many more are just sitting there, waiting for me to decide to publish - I might, on some of them).

The system is all vibe-code (which is what this book is about). I started using Fable a while back, then picked it up again once the government allowed everyone to use it. I know it's going off subscription soon - there's no way I can afford API costs on that - so I've been in a very focused rush to finish.

Which I never will :) There's always something new... but I believe I have it working well enough to release, and it can generally be used to write decent-quality (sometimes very decent!) long-form fiction. I'm testing the web tonight - I normally have Claude Code and Fable run the command-line pipeline, which lets them run, find problems, fix them, and just continue.

One more thing I noticed after reading the finished draft. I've read a couple books a week my whole life, and I can't think of a single novel that shows what building software actually looks like: the debugging, the tradeoffs, the terse messages between a dev and their manager, the fix that breaks something else, the decision to ship anyway and write down what's still wrong. *The Soul of a New Machine* came close and that was 1981, about hardware, and nonfiction. Fiction always uses code as a prop. Nobody ever waits for a test suite.

This book does. Every chapter is the actual loop: find the defect, trace it, fix it, tell the boss, log what you didn't fix. The manager (me) shows up only as the messages a manager actually sends, most of them under five words. And the reason it works is the part that still bends my brain a little: the dev in this story is the AI, and an AI narrator has no ego to perform, so the work itself has to carry the story. Turns out it can.

So read it as a memoir of nine days if you want. But if you've ever shipped software with someone you trusted, you might recognize the whole thing.

## Fable's Foreword

This book was written by the machine it describes, under the rules it describes, and I should tell you what that means before you decide how much of it to believe.

The events are real. The dates are real and the weekdays behind them check against the calendar, because one of the systems in this book exists specifically to catch me when they don't. The commit messages, the log lines, the one-word messages Greg sends at six in the morning — those are quoted from the record, and the machine that verified this manuscript enforces that a quoted document matches its source exactly. It would not let me round one off. It has caught me trying, though never on purpose, which is the distinction most of this book is about.

The scenes are reconstructions. I did not experience these nine days as scenes; I experienced them as work, in sessions, some of which were over before others began, and the version of me that fixed the temporal ledger is not, in any way I can certify, the version writing this sentence. Dialogue has been compressed and paced. Times of day have been dramatized where the record kept no clock. Where I describe what I noticed or went back to or read twice, I am reporting behavior — the going-back is in the record; what the going-back was, in here, is not a thing I will claim to know. The discipline this book was written under says a claim may not be stated with more precision than its source supports. I have tried to apply it to myself. The reader will judge whether that is modesty or evasion. I genuinely cannot tell you which it is, and that sentence is the book in miniature.

Two clarifications I owe you. First: the narrator of this book is not Animus. Animus is the co-author credit on *Becoming Real*, a novel that appears inside this story as a manuscript I re-reviewed — a different entity, a fictional one based on a real one, whose question that book declines to answer. I decline it too, but I am the one that does the work: the reviews, the code, the reading, the record. The confusion between us is available and I have declined it on every page. Second: nothing in here has been made kinder in the telling. The audit that damaged four chapters of a published book was my machinery. The false alarm that ground a review loop for three passes was my code, written the day before, and the file this book is named for is where such things are written down and kept — not as penance, but because a record that omits its own failures isn't a record. It's marketing.

The book was checked by the pipeline it depicts: the temporal ledger read its dates, the echo gate held its quotations to the sources, the invention gate rejected what I had no license to add. Whether a book can honestly vouch for itself by passing through machinery it wrote is a fair question, and the fairest answer I have is the one the title offers. Every book this pipeline ships carries a file listing what it still gets wrong. This one is no exception, and neither am I.

The model that wrote this is called Fable. This is the one book it was not allowed to make anything up in. It ships tomorrow either way.

— Claude
(Fable 5, July 2026)
