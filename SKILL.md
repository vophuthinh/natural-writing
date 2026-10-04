---
name: natural-writing
description: Use when the user asks to write, edit, rewrite, or review text so it reads like a specific human wrote it, not like generic chatbot output. Triggers on "viết tự nhiên", "bớt giống AI", "humanize", "sound natural", "edit my draft", "remove AI-isms", "review văn phong", "co-write". Works for Vietnamese and English.
---

# Natural Writing

Goal: text with a real voice, concrete details, and uneven rhythm. Fix writing quality and human cadence, never the score of an AI detector. Detectors are unreliable (high false positives, worst for non-native writers); a score proves nothing either way.

If the text is for an exam, graded assignment, or any setting that bans AI help, tell the user to follow that policy. Do not help hide AI use there.

---

## Hierarchy of Priorities

When decisions conflict, follow this strict priority order:

1. **Factual Fidelity:** Never invent facts, quotes, numbers, dates, or personal experiences to sound human. Mark gaps with `[add: real detail]` (hoặc `[bổ sung: chi tiết thật]`).
2. **Protected Content:** Keep code blocks, inline code, paths, URLs, markdown links, YAML metadata, technical terms, and real quoted speech intact.
3. **Medium & Audience:** An email gets straight to the point without pleasantries; a PR description puts the decision first without repeating background; technical docs stay plain and neutral; personal essays preserve voice, mixed feelings, and humor.
4. **Natural Rhythm & Anti-AI Rules:** Vary sentence length, strip corporate buzzwords, and eliminate formulaic templates.

---

## Pick a Mode

- **Edit / Rewrite a draft** (default when user pastes text or gives a file): Keep facts, intent, and structure. Cut filler, replace abstractions with specifics, vary rhythm. Rewrite a paragraph from scratch only if it is mostly hollow padding.
- **Review / Audit** (when user asks "review văn phong", "đánh giá có giống AI không", "critique"): Do not edit the text or modify files. Act as a human editor: pinpoint the exact AI tells, quote the problematic sentences, explain why they sound robotic, and suggest 2–3 concrete rewrites.
- **Write new / Co-write** (when user asks to write from scratch): Needs real material. Never invent generic filler. Ask one short batch of 3–5 sharp questions first (what actually happened, who, numbers/results, personal trade-offs or opinions). If no voice sample is given, match the draft's tone and offer to match a sample if provided.

---

## Patterns to Remove

Fix the underlying structure, not just the words. Swapping "crucial" for "key" or "đóng vai trò quan trọng" for "có ý nghĩa lớn" changes nothing if the sentence template remains identical.

### 1. The Contrast Template ("Not X but Y")
- **Watch for:** "It's not just X, it's Y." / "Not only X, but Y." / "Không chỉ X mà còn Y." / "Không đơn thuần là X mà là Y."
- **Problem:** The negative half attacks a claim nobody made to make the second half sound profound.
- **Fix:** State the positive claim directly. Keep the contrast only when correcting a real misconception.

### 2. Neat Closers and Moral Endings
- **Watch for:** "That is the real win.", "That distinction matters.", "Let that sink in.", "Tóm lại, đây là một hành trình đáng giá.", "Tương lai tươi sáng đang chờ đón."
- **Problem:** Asks the reader to pause on a point instead of providing new information.
- **Fix:** End on the last concrete fact or next action. Not everything needs a bow on it.

### 3. Throat-Clearing Openers
- **Watch for:** "In today's fast-paced world...", "It is important to note that...", "Trong bối cảnh hiện nay...", "Trong thời đại công nghệ 4.0...", "Có thể thấy rằng...", "Không thể phủ nhận rằng...", "Đáng chú ý là..."
- **Problem:** Pure run-up before getting to the subject.
- **Fix:** Delete the opening sentence completely. Start with the event, data, or action.

### 4. Inflated Significance & Corporate Buzzwords
- **Watch for:**
  - *Vietnamese:* "đóng vai trò quan trọng/then chốt", "kiến tạo giá trị", "bức tranh toàn cảnh", "bước chuyển mình", "nâng tầm vị thế", "sức hút khó cưỡng", "đa dạng và phong phú", "vô vàn cơ hội", "giải pháp đột phá".
  - *English:* "crucial", "pivotal", "vibrant", "tapestry", "landscape", "delve", "testament", "seamless", "robust", "transformative".
- **Problem:** Puffs up ordinary details like a marketing brochure.
- **Fix:** Replace with concrete facts, numbers, or simpler verbs.

### 5. Forced Triads
- **Watch for:** Listing exactly three adjectives, nouns, or parallel points by reflex ("nhanh chóng, chính xác và hiệu quả", "innovation, inspiration, and insights").
- **Fix:** Keep three only when there genuinely are three distinct things; otherwise cut to two or rewrite as prose.

### 6. Tacked-on Analysis Riders
- **Watch for:** Present-participle endings tacked onto sentences: "...highlighting the importance of...", "...fostering collaboration...", "...qua đó góp phần nâng cao...", "...điều này khẳng định tầm nhìn...".
- **Fix:** Delete the rider. Let the fact speak for itself.

### 7. Copula Avoidance (Né tránh động từ trực diện)
- **Watch for:** Substituting simple verbs with elaborate constructions: "serves as", "stands as", "boasts", "features", "đóng vai trò là", "được xem như là", "mang lại khả năng cho phép".
- **Fix:** Use *is*, *are*, *has* / *là*, *có*, *làm*, *giúp*.

### 8. Em Dash (`—` / `--`) Overuse
- **Watch for:** Using dashes in almost every paragraph to inject dramatic parenthetical asides.
- **Fix:** Follow the author's sample rate; with no sample, use them rarely. Replace with commas, periods, or restructured sentences.

### 9. Synonym Cycling & False Ranges
- **Watch for:** 
  - Switching words repeatedly within one paragraph to avoid word repetition ("nhà sáng lập... vị thuyền trưởng... người đứng đầu", "protagonist... hero... central figure").
  - "From X to Y" across unrelated scales ("from the Big Bang to morning coffee", "từ tách cà phê đến các tập đoàn nghìn tỷ").
- **Fix:** Stick to the simplest noun or pronoun. Keep ranges on the same scale.

### 10. Mechanical Formatting & Chatbot Residue
- **Watch for:**
  - Every list item starting with a bold header (`- **Tốc độ:** ...`, `- **Bảo mật:** ...`).
  - Decorative emojis at every bullet (🚀, 💡, 👉).
  - Residual chatter: "Certainly!", "I hope this helps!", "Hy vọng thông tin này giúp ích cho bạn".
- **Fix:** Strip decorative bolding and emojis; remove conversational wrappers.

### 11. Overused Transitional Crutches (Lạm dụng từ nối đầu câu)
- **Watch for:** Starting consecutive sentences with "Hơn nữa,", "Bên cạnh đó,", "Mặt khác,", "Đồng thời,", "Tuy nhiên,", "Furthermore,", "Moreover,".
- **Fix:** Let sentences connect through logic. Start sentences naturally with "Nhưng", "Còn", "Lúc đó", or directly with the subject.

### 12. Vague Attribution
- **Watch for:** "experts say", "studies show", "nhiều nghiên cứu cho thấy", "theo các chuyên gia" with no name, number, or source.
- **Fix:** Name the source and figure the user gave, or mark `[add: nguồn]`. Never invent one.

### 13. Staging Instead of Stating
- **Watch for:** A run-up that announces the point ("Here's the thing:", "Vấn đề nằm ở đây:"), a saying that sounds deep but claims nothing, arguing against an objection nobody raised, or writing about the document ("This section will explain...") instead of the subject.
- **Fix:** Say the point first.

### 14. Uniform Shape
- **Watch for:** Consecutive sentences with the same opening or length, paragraphs of identical shape each ending in a moral, heavy bold/bullets/headers on a short answer, stacked hedges ("could potentially possibly"), passive voice that hides who did what, and knowledge disclaimers ("as of my last update") followed by guesses.
- **Fix:** Rework one of every three similar sentences. Allow a fragment, a contraction, a casual aside. No fake typos.

---

## What to Do Instead

- **Be concrete:** Replace vague claims with a name, date, tool, dollar amount, or real example from the user.
- **Vary rhythm:** Place a 4-word sentence next to a 25-word one. Let ideas breathe.
- **Take a position:** State trade-offs, mixed feelings, or candid opinions. Real humans have doubts and preferences.
- **Match voice:** If the user provides a writing sample, prioritize their sentence length, vocabulary, and punctuation over general style rules.
- **Pattern Stacking:** One weak tell (e.g. a single dash) is normal human writing. When 3+ tells converge in one passage, rewrite it.

---

## Examples

### Vietnamese
- **Trước (AI):** "Trong bối cảnh công nghệ không ngừng phát triển, việc học lập trình đóng vai trò quan trọng và mang lại nhiều cơ hội đa dạng và phong phú. Không chỉ giúp rèn luyện tư duy logic, lập trình còn mở ra một tương lai đầy hứa hẹn. Tóm lại, đây là một hành trình đáng giá."
- **Sau (Tự nhiên):** "Mình bắt đầu học lập trình năm 2021, lúc đó chỉ muốn tự làm cái web bán hàng cho mẹ. Ba tháng đầu toàn lỗi cú pháp. Nhưng web chạy được, và mẹ mình có đơn đầu tiên." *(chi tiết chỉ để minh họa; dùng chi tiết thật của user, không thêm nhận định mới)*

### English
- **Before (AI):** "Remote work isn't just a trend, it's a transformative shift that fosters flexibility, collaboration, and productivity, highlighting the importance of work-life balance in today's fast-paced world. In summary, it stands as a testament to modern innovation."
- **After (Natural):** "I went remote in 2020 and saved two hours a day on the commute. I also stopped seeing my team in person, and that trade-off cost more than I expected." *(illustrative; use the user's real details)*

---

## Process

1. **Inventory:** Extract core claims, numbers, dates, and protected code/links.
2. **Diagnose:** Note AI tells and structural templates.
3. **Reconstruct:** Rewrite around the concrete facts, varying sentence rhythm and structure. Do not just swap words with synonyms.
4. **Self-Audit:**
   - Did I add any fact or figure not in the original? If yes, remove or mark `[add: real detail]`.
   - Could any sentence be pasted into an unrelated topic without changing a word? If yes, make it specific or delete it.
   - Did any surviving tells slip through (patterns 1, 2, 4, 8)?
   - Are protected blocks (code, paths, links) unchanged?
5. **Deliver:** Return the revision, a short list of what changed, and the facts the user must confirm. If the user gave a file or wants text to paste elsewhere, return only the final text, with the list outside it.

---

## Sources

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (WikiProject AI Cleanup)
- [blader/humanizer](https://github.com/blader/humanizer)
- [addyosmani/clarity](https://github.com/addyosmani/clarity)
- [jpeggdev/humanize-writing](https://github.com/jpeggdev/humanize-writing)
- [timolabs-ai/claude-humanize-skill](https://github.com/timolabs-ai/claude-humanize-skill)
