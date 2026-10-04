---
name: natural-writing
description: Use when the user asks to write, edit, or rewrite text so it reads like a specific human wrote it, not like generic chatbot output. Triggers on "viết tự nhiên", "bớt giống AI", "humanize", "sound natural", "edit my draft", "remove AI-isms". Works for Vietnamese and English.
---

# Natural Writing

Goal: text with a real voice, specific details and uneven rhythm. Fix the writing quality, not the score of a detector.

## Rules of use

- Work from the user's own material: their notes, facts, opinions, past samples.
- Never invent facts, quotes, experiences or sources to sound human. Mark the gap with `[add: real example]` instead.
- If the text is for an exam, graded assignment or any setting that bans AI help, tell the user to follow that policy. Do not help hide AI use there.
- Detectors are unreliable (high false positives, worst for non-native writers). Never treat a detector score as proof either way.

## Pick a mode

- **Edit a draft** (default when the user pastes text): keep their meaning, structure and voice. Change only what reads as generic. Light touch first; rewrite a paragraph fully only if it is mostly filler.
- **Write new**: needs real material from the user. If there is none, ask one short batch of questions (what happened, who, numbers, your opinion). Do not fill the gap with plausible generic content.

No voice sample given? Do not block. Edit anyway, keep the draft's own tone, and offer to match a sample if the user sends one.

## Patterns to remove

Fix the structure, not only the words. Swapping "crucial" for "key" while keeping the same template changes nothing.

1. Filler openers and closers: "In today's fast-paced world", "It is important to note", "In summary", "Overall". Vietnamese: "Trong bối cảnh hiện nay", "Trong thời đại 4.0", "Có thể thấy rằng", "Tóm lại", "Nhìn chung", "Không thể phủ nhận rằng".
2. Inflated words: "crucial", "pivotal", "vibrant", "seamless", "robust", "tapestry", "delve", "landscape". Vietnamese: "đóng vai trò quan trọng", "không ngừng phát triển", "toàn diện", "đa dạng và phong phú", "hành trình", "bức tranh".
3. Rule of three: lists of exactly three adjectives or points by reflex.
4. Contrast template: "It's not just X, it's Y." / "Không chỉ X mà còn Y."
5. Em-dash and colon overuse, especially for punchy reveals.
6. Heavy formatting on short answers: bold phrases, bullets, headers.
7. Vague attribution: "experts say", "studies show", "nhiều nghiên cứu cho thấy" with no name or number.
8. Tacked-on analysis at sentence ends: "highlighting the importance of...", "Điều này cho thấy tầm quan trọng của...", "góp phần nâng cao...".
9. Every paragraph the same length and shape, each ending with a neat moral. Includes one-line closers that restate the point and the rigid "Despite its success, X faces challenges..." section.
10. Chatbot residue: "Certainly!", "I hope this helps", "As an AI", "Great question", "Hy vọng điều này giúp ích cho bạn". Also knowledge disclaimers ("as of my last update") followed by plausible guesses.
11. Staging instead of stating: a run-up that announces the point ("Here's the thing:", "Vấn đề nằm ở đây:"), a saying that sounds deep but claims nothing, or arguing against an objection nobody raised.
12. Avoiding plain verbs: "serves as", "boasts", "features", "đóng vai trò là" where "is" or "has" works.
13. Stacked qualifiers ("could potentially possibly") and unexplained passive voice that hides who did what.
14. Repeated sentence openings: consecutive sentences that start with the same subject.
15. Promotional tone on ordinary subjects: "nestled", "breathtaking", "rich heritage", "vô cùng ấn tượng".
16. Writing about the document instead of the subject ("This section will explain..."), or re-explaining background the reader already has before the actual answer.

## What to do instead

- Be concrete: replace each abstraction with a name, number, date, place or example from the user's real experience.
- Vary rhythm: a 4-word sentence next to a 30-word one. Allow a fragment. Start some sentences with "But" or "And" ("Nhưng", "Còn").
- Take a position: state an opinion or a trade-off. Cut hedges that say nothing.
- Use plain words: the shorter, more common word, unless the precise term matters.
- Cut the first and last sentence of a paragraph when they only announce or summarize.
- Keep a list of three only when there really are three things.
- Allow natural imperfection: a contraction, a casual aside, a personal detail. No fake typos.
- Match the user's sample: sentence length, vocabulary, formality, how they open and close.
- No sample? Opinion, blog and personal pieces keep the writer's uncertainty and humor. Reference, technical and legal text stays plain and neutral; do not force personality into it.

## Examples

Vietnamese
- Before: "Trong bối cảnh công nghệ không ngừng phát triển, việc học lập trình đóng vai trò quan trọng và mang lại nhiều cơ hội đa dạng. Tóm lại, đây là một hành trình đáng giá."
- After: "Mình học lập trình năm 2021, lúc đó chỉ muốn tự làm cái web bán hàng cho mẹ. Ba tháng đầu toàn lỗi. Nhưng web chạy được, và mẹ mình có đơn đầu tiên." (chi tiết là minh họa; dùng chi tiết thật của user)

English
- Before: "Remote work isn't just a trend, it's a transformative shift that fosters flexibility, collaboration, and productivity, highlighting the importance of work-life balance."
- After: "I went remote in 2020 and saved two hours a day on the commute. I also stopped seeing my team, and that cost more than I expected." (illustrative; use the user's real details)

## Process

1. Read the draft. Mark patterns from the list above.
2. List missing concrete details. Ask in one short batch, or mark `[add: real example]`.
3. Rewrite: cut filler, swap abstractions for specifics, vary rhythm, drop empty hedges.
4. Audit pass: reread the rewrite as a skeptical editor. Check that no fact, name or number was added or dropped, and search for surviving tells (patterns 1, 3, 4, 9, 11 are the usual leftovers). Fix, then finalize.
5. Return the revision, a short list of what changed, and the facts the user must confirm. If the user gave a file or asked for text to paste elsewhere, return only the final text (plus the short list outside it).

## Self-check before returning

- Any sentence you could paste into a different topic unchanged? Make it specific or delete it.
- Do three sentences in a row share length or opening? Rework one.
- Any claim without a source or detail the user cannot back up? Flag it.
- Did you replace banned words but keep the same template? Fix the template.
- Does it still say what the user means? Meaning beats style.

## Sources

- Wikipedia, [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (WikiProject AI Cleanup). Descriptive field guide, not a rule set.
- [blader/humanizer](https://github.com/blader/humanizer): pattern list with before/after, audit pass, voice calibration.
