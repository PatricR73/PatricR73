I write Python that reads documents and produces other documents. Retrieval systems, caption pipelines, compliance tooling. Based in Romania, working with clients anywhere in European hours.

The thing I care about most is what a tool does when it doesn't know the answer.

Most document automation guesses. Ask a retrieval system whether a company runs quarterly penetration tests and it will usually say yes, because that is what security questionnaires normally say. That answer then goes to a prospective customer in writing, and sometimes into a contract. An honest "we haven't documented that" costs someone twenty minutes. A confident wrong answer costs considerably more, and nobody finds out until it's already been relied on.

So the tools I build abstain, and I measure whether they actually do.

## Work

**[Questionnaire-Responder](https://github.com/PatricR73/Questionnaire-Responder)**

Drafts answers to vendor security questionnaires from a company's own policy documents. On 20 CAIQ v4.0.2 questions: 13 usable as drafted, 7 that correctly refused to answer, 0 fabricated.

Those 7 refusals score as *wrong* against my own rubric. I left the rubric alone, because adjusting the scoring after seeing the results is how numbers like these stop meaning anything.

**[Anchor-Align](https://github.com/PatricR73/Anchor-Align)**

Speech-to-text hands you timing for every word. Then an editor cleans up the transcript and the timing no longer lines up with the text anyone wants to caption. This puts the two back together, including when whole sentences have been moved.

Error on words the editor never touched: 4 ms, against 371 ms for the obvious difflib approach. That's all on a synthetic corpus though, and I haven't validated it against a genuinely human-edited transcript yet. It's issue #3 and it's still open.

**[eu-ai-newsletter](https://github.com/PatricR73/eu-ai-newsletter)**

Weekly EU AI Act tracking for people who have to follow it professionally. RSS in, deduplication against the five outlets covering the same story, relevance scoring, summaries out. Built and verified end to end on n8n with a FastAPI sidecar. Not published yet, which I know is the entire difference between a pipeline and a newsletter.

## What I take on

Document-grounded retrieval where every claim has to trace back to a source. Questionnaire and RFP drafting for teams who get handed a 200-row spreadsheet and a deadline. Caption and transcript work for accessibility obligations, which since June 2025 is a legal requirement for anything sold into the EU rather than a nice-to-have. Automation plumbing on n8n and FastAPI.

## One thing that explains the rest

Anchor-Align has a phonetic matching mode. It ships turned off, because when I benchmarked it the results got worse: short words like "and" and "end" share a phonetic key, and the aligner started gluing them together across long distances. On real transcripts with actual homophone errors it might well pay for itself. I can't demonstrate that yet, so it stays off and the reasoning is written down in DESIGN.md.

I'd rather hand you a smaller tool I can defend than a longer feature list I can't.

## Contact

[hello@patricf.com](mailto:hello@patricf.com) · [patricf.com](https://patricf.com) · [LinkedIn](https://www.linkedin.com/in/patric-rg-b395a9408/) · [Upwork](https://www.upwork.com/freelancers/~011c4532b0fb560f78)

Currently taking on contract work.
