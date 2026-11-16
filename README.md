# linkedin-post-system

A Claude skill that runs a recurring LinkedIn routine for one person: it researches, writes and designs a post, drafts replies and comments, and publishes only after the person approves.

## Install
Copy this folder to `~/.claude/skills/linkedin-post-system/` and ask Claude to "set up my LinkedIn post system".

## Requirements
The skill is only instructions. To do the work, Claude needs:

| What | Why |
|---|---|
| Claude desktop app or Claude Code | runs the sessions and the scheduled routine |
| Claude in Chrome extension, with LinkedIn signed in | reads your profile and publishes after you approve |
| Web search | finds and checks recent news |
| Git, and a private repository or local folder | keeps your facts, voice, rotation and metrics |
| A design skill (for example `canvas-design`) | images and PDF carousels |
| A video skill plus Node.js and ffmpeg (for example HyperFrames) | videos and GIFs |

Optional: a "humanizer" skill (the bundled `templates/HUMANIZER.md` is used either way), and a scheduled task to run the routine on fixed days.

## Set up
1. Install the requirements above and sign in to LinkedIn in Chrome.
2. Create a private folder or repository for your data.
3. Ask Claude to "set up my LinkedIn post system". It copies `templates/` into your folder and interviews you, one role at a time.
4. Run one round by hand and approve it before scheduling anything.
5. Schedule the routine (for example Monday, Wednesday and Friday).

## Privacy
The skill holds no personal data. Everything about you goes into a working folder that you should keep private.

## A note on automation
LinkedIn's terms restrict automated activity. This skill keeps volumes low and never publishes without your approval, but the risk is yours to weigh.

---

Uma skill do Claude que roda uma rotina de LinkedIn para uma pessoa: pesquisa, escreve e cria a arte do post, rascunha respostas e comentários, e só publica depois da aprovação. Não contém dados pessoais.

## Related work
Some ideas here (a story bank, a hook library, an audit before publishing, following up when an author replies) were informed by reading other open skills, especially [sergebulaev/linkedin-skills](https://github.com/sergebulaev/linkedin-skills) and [blader/humanizer](https://github.com/blader/humanizer), both MIT. No text was copied. If you want a deeper humanizer, install blader/humanizer and this skill will use it.

## License
MIT. See [LICENSE](LICENSE).
