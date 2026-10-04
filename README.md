# natural-writing

A Claude Code skill that edits or writes text so it reads like a specific person wrote it, not like generic chatbot output. Works for Vietnamese and English.

Most humanizer skills target English only. This one also covers Vietnamese AI tells ("Trong bối cảnh hiện nay", "đóng vai trò quan trọng", "Không chỉ X mà còn Y", "Có thể thấy rằng").

It removes common AI writing patterns (filler openers, inflated words, forced triads, "not just X but Y", chatbot residue), asks for real details instead of inventing them, and matches the writer's own voice.

## Before / after

Illustrative examples. In real use the skill asks for your own details instead of inventing them.

**Vietnamese**

> Trong bối cảnh công nghệ không ngừng phát triển, việc học lập trình đóng vai trò quan trọng và mang lại nhiều cơ hội đa dạng. Tóm lại, đây là một hành trình đáng giá.

becomes

> Mình học lập trình năm 2021, lúc đó chỉ muốn tự làm cái web bán hàng cho mẹ. Ba tháng đầu toàn lỗi. Nhưng web chạy được, và mẹ mình có đơn đầu tiên.

**English**

> Remote work isn't just a trend, it's a transformative shift that fosters flexibility, collaboration, and productivity, highlighting the importance of work-life balance.

becomes

> I went remote in 2020 and saved two hours a day on the commute. I also stopped seeing my team, and that cost more than I expected.

## Install

```sh
git clone https://github.com/vophuthinh/natural-writing.git ~/.claude/skills/natural-writing
```

Or copy `SKILL.md` into `~/.claude/skills/natural-writing/`.

## Use

Ask Claude Code things like:

- "Viết tự nhiên hơn đoạn này: ..."
- "Remove the AI-isms from this draft"
- "Humanize this, keep my tone"

## Notes

- It never invents facts or experiences. Gaps are marked `[add: real example]`.
- It will not help hide AI use where that is banned (exams, graded work).
- Detector scores are not treated as proof either way.

## Sources

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [blader/humanizer](https://github.com/blader/humanizer)

## License

MIT
