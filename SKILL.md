---
name: linkedin-post-system
description: Run a recurring LinkedIn routine for one person - research, write and design a post, draft replies to comments and comments on other people's posts, then publish only after the person approves. Use when the person asks to set up, run or improve their LinkedIn posting routine.
---

# LinkedIn post system

A routine that prepares everything for a person's LinkedIn presence and publishes only after they say "publish" in the same session. It keeps its state in plain files so any session, on any computer, can pick it up.

Nothing in this skill is about a specific person. All personal material lives in the working folder, which should be a PRIVATE repository or a local folder.

## 0. Hard rules
- Never publish, comment or reply without an explicit "publish" from the person in the current session. No answer means nothing goes out.
- Use only facts the person confirmed. A CV is a summary: when a text needs a task that fits the role but is not confirmed, ask a short closed question and wait. Never invent scenes, quotes, motives or numbers.
- Record what the person did NOT do as carefully as what they did (who decided, who talked to clients, who owned the budget).
- Employer data: only numbers the person already made public or explicitly cleared.
- Never change account settings, send connection requests or direct messages, or type a password.
- Stop everything if the site asks for login or verification, or shows an unusual-activity warning.
- Limits per run: 1 post, up to 5 comments on other people's posts, up to 10 replies.

## 1. First run: set up the folder
Copy `templates/` into the working folder and fill it by interviewing the person:
1. `PROFILE.md`: languages to alternate, visual identity, posting days, topics to avoid, people or companies never to engage with.
2. `FACTS.md`: one role at a time. First open questions, then a numbered checklist of typical activities for that role that the person answers by number, with notes. Keep a "not confirmed" list.
3. `VOICE.md`: phrases the person actually says, and later every edit they make to a draft.
4. `TARGETS.md`: creators, recruiters and hiring managers worth commenting on.
5. `STORIES.md`: turn the confirmed facts into a story bank. Each row has the situation, the turning point and a number, plus the date it was used. A story comes back only after six weeks, in another language or format.
`ROTATION.md`, `METRICS.md`, `HOOKS.md` and `ERRORS.md` start empty.

## 2. Every run
1. Pull the folder if it is a Git repository. Read every state file. If a `PAUSE.txt` file exists, stop and say so.
2. Read the person's real activity page first and fix `ROTATION.md` if they posted outside the system.
3. Measure: impressions, reactions and comments of the last three weeks into `METRICS.md`. After six measured posts, give the best format and topic one extra slot in every four runs. Never drop a format because of one weak post.
4. Pick by rotation, never repeating the previous post: language, format (image, GIF, PDF carousel, video), type (tech news, personal experience, industry conversation), experience used, and text structure (numbered list, short story, opinion, behind the scenes, a mistake, an open question).
5. Research. News: last 7 days, confirmed on a primary source or a recognized outlet; open the source and check date, numbers and names. References: recent posts from `TARGETS.md`; copy structure, never text or numbers.
   Hooks: when a reference post is doing far better than that author's usual, extract the shape of its first line (the structure, never the words) into `HOOKS.md`.
   Every fourth run, repurpose: take the best post in `METRICS.md` older than three weeks and redo it in the other language and another format, with a new hook. Say so in the summary.
6. Write. Pick an unused story from `STORIES.md`. Three candidate first lines, keep the best. Concrete example, real numbers, a question at the end, at most three hashtags. Source links go in the first comment, not in the body. Think of a recruiter reading for six seconds: scale, what the person built, what decision it supported.
7. Review in three passes: recruiter skim, `HUMANIZER.md` plus `VOICE.md` (and an installed humanizer skill if there is one), then fact check sentence by sentence. Audit before scoring, and any "no" sends the draft back: do the first two lines work alone? Is the post around 900 to 1,300 characters, or is there a reason not to be? No link in the body? At most three hashtags? Does every number have a source or a confirmed fact? Is there at least one number where an adjective would have been? Is the hook shape different from the previous post? Score 0 to 2 on hook, concrete proof, voice, value to someone hiring, facts checked. Below 8 of 10, rewrite.
8. Design. Look for installed design, video and audio skills before building anything by hand, and pick the best ones for the format. The identity in `PROFILE.md` always wins over a skill's defaults. Add alt text to images and burned-in captions to video. Check the render at phone size.
9. Replies. Read each new comment in full and who wrote it. Recruiter or hiring manager: add one detail of the person's work and alert the person. Peer: answer the technical point and ask something back. Friend: short and warm. Never open with "thanks for the comment". If the answer needs a fact you do not have, ask the person. When the author of a post replies to the person's comment, continuing that thread comes before any new comment, ideally 6 to 24 hours later. LinkedIn threads have two levels: a reply to a reply lands in the same thread and tags the person, so check the tag. Look at who reacted and commented, and alert the person when a recruiter, a hiring manager or someone from `TARGETS.md` shows up.
10. Comments on others. Only when there is something to add: a checked fact, an example, a question the post left open, a polite disagreement. About 200 to 350 characters in the post's language, one idea: one sharp point beats three vague ones. Order: their post first, then the question or suggestion, then at most one subtle line about the person's experience, in no more than half of the comments. Skip politics, grief, sales and job posts.
11. Show one summary: post, asset, replies, comments, sources, score and every sentence that needs the person's confirmation. Ask "Publish?".
12. After "publish": post, verify it is live, log the run in `ROTATION.md`, log anything that broke in `ERRORS.md`, commit and push.

## 3. Practical notes for publishing through a browser
- Typing long text into the site can drop characters. Insert text programmatically into the focused field and read the whole text back before submitting.
- The media button may open the operating system's file picker, which an agent cannot use. Find a way to hand the file to the page's own file input instead.
- After every publish, reload and confirm the text is where it should be.

## 4. Weekly
On the last run of the week, write a short summary: what went out, numbers, who commented, recruiters who showed up, what to change next week. End with next week's plan: for each run, the language, format, story, hook shape and two or three profiles to comment on. The person can veto or swap anything before the week starts.

## 5. Length figures
The character ranges above are common market guidance, not measured truth. Once `METRICS.md` has enough of the person's own posts, their best performers decide.
