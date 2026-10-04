# natural-writing

A skill for Claude Code and other agents that read `SKILL.md`. It edits, writes, or reviews text so it reads like a real person wrote it, not like generic chatbot output. Works for Vietnamese and English.

Most humanizer tools target English only. natural-writing also covers Vietnamese AI signatures (*"Trong bối cảnh hiện nay"*, *"đóng vai trò quan trọng"*, *"Không chỉ X mà còn Y"*, *"Có thể thấy rằng"*, *"bức tranh toàn cảnh"*, *"hành trình kiến tạo"*), while removing universal LLM tics.

---

## What makes it different

1. Covers Vietnamese AI patterns as well as English ones.
2. Rebuilds sentences from facts and concrete details instead of swapping synonyms.
3. Three modes: rewrite a draft, review without editing, co-write by interview.
4. Never invents facts, quotes, or experiences. Gaps are marked `[add: real detail]` (or `[bổ sung: chi tiết thật]`).
5. One portable `SKILL.md`, no other files.

---

## Modes

| Mode | When to Use | How to Trigger |
|---|---|---|
| **Rewrite (Default)** | Rewrite text or files to sound human while keeping facts intact. | `"Viết tự nhiên hơn đoạn này"`, `"humanize this draft"` |
| **Review / Audit** | Critique text without modifying files. Pinpoint exact tells and suggest fixes. | `"Review văn phong bài này"`, `"audit this text for AI tells"` |
| **Interview / Co-write** | Draft new content from scratch without inventing generic corporate filler. | `"Hỏi tôi trước rồi viết bài về..."`, `"co-write with me"` |

---

## Before / After

### Vietnamese

> **Trước (AI):**
> Trong bối cảnh công nghệ không ngừng phát triển, việc học lập trình đóng vai trò quan trọng và mang lại nhiều cơ hội đa dạng và phong phú. Không chỉ giúp rèn luyện tư duy logic, lập trình còn mở ra một tương lai đầy hứa hẹn. Tóm lại, đây là một hành trình đáng giá.
>
> **Sau (Tự nhiên):**
> Mình bắt đầu học lập trình năm 2021, lúc đó chỉ muốn tự làm cái web bán hàng cho mẹ. Ba tháng đầu toàn lỗi cú pháp. Nhưng web chạy được, và mẹ mình có đơn đầu tiên.

*Chi tiết chỉ để minh họa. Khi dùng thật, skill hỏi chi tiết của bạn thay vì tự bịa.*

### English

> **Before (AI):**
> Remote work isn't just a trend, it's a transformative shift that fosters flexibility, collaboration, and productivity, highlighting the importance of work-life balance in today's fast-paced world. In summary, it stands as a testament to modern innovation.
>
> **After (Natural):**
> I went remote in 2020 and saved two hours a day on the commute. I also stopped seeing my team in person, and that trade-off cost more than I expected.

---

## Install

### For Claude Code
Clone or copy `SKILL.md` into your Claude skills directory:
```bash
git clone https://github.com/vophuthinh/natural-writing.git ~/.claude/skills/natural-writing
```

Or copy `SKILL.md` directly into `~/.claude/skills/natural-writing/`.

### For other agents
If your agent loads `SKILL.md` from a skills directory, copy it there. Example path (adjust to your agent):
```bash
mkdir -p ~/.gemini/config/skills/natural-writing
cp SKILL.md ~/.gemini/config/skills/natural-writing/
```

---

## Use

Ask your AI assistant:
- "Viết tự nhiên hơn đoạn này: ..."
- "Review văn phong bài này xem có bị sáo rỗng hay giống AI không"
- "Remove the AI-isms from this draft"
- "Humanize this, keep my voice"
- "Hỏi tôi vài câu trước rồi viết giúp bài chia sẻ về..."

---

## Safeguards

- Detector scores are not treated as proof either way. Detectors give many false positives, especially for non-native writers.
- If a sentence needs a fact or number you did not give, the skill asks for it or leaves `[add: real detail]`.
- It will not help hide AI use where it is banned (exams, graded work).

---

## Sources & Credits

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (WikiProject AI Cleanup)
- [blader/humanizer](https://github.com/blader/humanizer)
- [addyosmani/clarity](https://github.com/addyosmani/clarity)
- [jpeggdev/humanize-writing](https://github.com/jpeggdev/humanize-writing)
- [timolabs-ai/claude-humanize-skill](https://github.com/timolabs-ai/claude-humanize-skill)

---

## License

MIT © [Vo Phu Thinh](https://github.com/vophuthinh)
