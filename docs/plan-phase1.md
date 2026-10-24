# Brew & Build: Cubbie Hackathon plan (Phase 1 focus)

Team (all ASU emails; Shreyas owns all entries and lists all 4 members):

| Dev | Name | Email | Role / share |
| --- | --- | --- | --- |
| A | Shreyas Jagannath Revankar | srevank2@asu.edu | Backend, integrations, deployment, repo setup; 30%; entry owner |
| B | Rohan Shirish Waghode | rwaghode@asu.edu | Core logic, frontend, integration; 30% |
| C | Bhavisha Rajubhai Sondagar | bsondaga@asu.edu | Leads Track 1 Skill, pitch deck and story; 20% |
| D | Shravani Kishor Kulkarni | skulk119@asu.edu | Testing, polish, README, video, social, vote push, demo; 20% |
 Main repo: github.com/brew-and-build/brew-and-build (final work, `skills/<skill-name>/`); each member tests in their own repo in the org. Strongest skills: pending team confirmation (Python, JavaScript, React, Node was only an example).

Sources: kit `skills/cubbie-hackathon/references/{rules,ideas}.md` (R), `SKILL.md` (S), skill-creator references (C), organizers' guide `docs/event/cubbie-skill-guide.md` (G), tracks screenshot (SS), live `status` output and https://hackathon.cubbie.ai (site). Kit and live site win over the screenshot and guide. Anything marked **[Judgment]** or **[Assumption]** is ours, not the organizers'.

## 0. Deadlines (from the team lead, 2026-10-24; Discord confirmation pending)

| Event | Time (Arizona, MST, UTC-7) | Status |
| --- | --- | --- |
| Hacking started | Sat Oct 24, 10:30 AM (17:30 UTC) | Given by team lead |
| Track 1 close (first 10 hours) | Sat Oct 24, **8:30 PM** | **[Assumption]** 10:30 AM + 10 h; team lead is confirming on Discord |
| Our Track 1 submit target | Sat Oct 24, **5:30 PM** (3 h before close) | Our rule |
| Tracks 2/3 final submissions close | Sun Oct 25, **12:00 PM** | From the event schedule per team lead; confirming on Discord |
| Our Tracks 2/3 final submit | Sun Oct 25, **11:15 AM** (45 min before close) | Our rule |

- `status` (kit) still shows **no closing time set** for Track 1, Tracks 2/3 or voting; it only shows the windows opened Thu Oct 22, 03:55 MST (10:55 UTC), and that voting allows up to 5 votes per person. The kit and live site win over our assumed times, so re-run `python3 scripts/hackathon.py status` (in `cubbie-hackathon-kit/skills/cubbie-hackathon`) before submitting, and again at every phase start.
- The site says dates are "still being finalized" and that the Track 1 cutoff "is confirmed with the organizers before kickoff". Voting close is not announced. Organizers' Discord: https://discord.gg/7eJADTbQMT.
- If Discord changes either time, rescale section 5; keep the "3 h before" and "45 min before" margins.

## 1. Rules check

| Topic | Rule (quoted) | File |
| --- | --- | --- |
| Track 1 done | "Track 1 is complete when Cubbie can install your Skill from its GitHub link and run its main flow on a real account; it must be done within the first 10 hours. Submit the link to your Skill folder at a specific commit." | G |
| What the kit submits | Repository link "installs the newest commit of the default branch. Submit this one to the hackathon." Pinned link: "Use it only to share one fixed version." Field accepts "the repository link, or a folder inside it". **Guide says folder at a commit; kit says repository link. Kit wins, but ask Discord (see Missing info).** | R, C `cubbie-testing.md`, G |
| Unlocks | "Only teams that submit Track 1 unlock Tracks 2 and 3." The database refuses Track 2/3 otherwise; "submit Track 1 first, from any teammate's account". | SS, S |
| Track 1 deliverables | Working Skill running on Cubbie, clear student use case, optional short public video. | R |
| Track 1 judging | "Judges mainly look at public votes on this site and your video's engagement on social media." Site reads views, likes, comments, shares automatically. | R |
| Video | TikTok or Instagram only. Length, hashtags, tags "haven't been announced; don't make them up". Optional, but counts toward the social score. | S, R |
| Extra posts | Up to 5 more posts besides the main one, via `posts`, until voting closes. | R |
| Fields | Team name and project name ≤ 60 chars; one-liner ≤ 140; 1 to 4 members, distinct emails; every link `https://`. Track 1 link must be GitHub (repo or folder in it). Post optional, must match the platform picked. | R |
| Tracks 2/3 fields | GitHub repo required; website (one link) and demo video optional. Repo must be public for the preview card. | R |
| Who submits | "One entry per person per track. Whoever sends it owns it; the members listed on it see it but can't start a second entry, and only the owner can edit it." List **all 4 members** on every entry. | R |
| Identity | One email = one account. A different address (school alias, personal Gmail, dots, `+tag`) is a different account and can't edit the owner's entry. Run `whoami` before submitting. | R, S |
| Public vs private | Public: team name, project name, one-liner, links. Private: members and emails. Entry is live the moment it is sent, no review gate. | R |
| Editing | Free edits while the track's window is open; closing the window locks entries. | R, `status` |
| Voting | Track 1 only. School email required (`*.edu` or known school domain; `+tag` refused). One vote per project; not for an entry you own or are listed on; can take a vote back; up to 5 votes per person. | R, `status` |
| Sent back / taken down | Organizers can "send an entry back with a note (it leaves the gallery until the team edits it, which is allowed even after the window closes) or take it down (the team can't bring it back)." Reasons are not listed. | R |
| Tracks 2/3 judging | "Judged privately on what you show us. Full criteria are announced before kickoff." Criteria not in the kit. | R, SS |
| Skill limits | Guide: ≤ 5 MiB, 300 files, 10 hosts, 5 keys, 20 Skills per student. Kit testing doc says Cubbie has no such limits. Kit wins; stay small anyway. | G, C |
| Prizes | Track 1: monitor / Anker headphones, plus "priority for a Cubbie internship". T2: Fitbit Charge 6 / Anker speaker. T3: Google Home speaker / gaming mouse. | R |
| Our own rule | Show the exact submission and get an explicit "yes" before any submit, edit, or `posts` call (publishing is public once sent). | S, CLAUDE.md |

**Things that could get an entry sent back or taken down** (the kit lists no criteria, so these are our reading **[Judgment]**): a Skill that cannot install from the link; a private repo; a different name or contact than the real team; sending or paying without the student's yes (G: "A Skill cannot grant that approval"); asking for passwords or keys in chat; fake votes or `+tag` school emails; a video with made-up claims.

## 2. Track 1 plan

### 2.1 Three Skill ideas

All three use only abilities in `cubbie-capabilities.md` and sign-in approach 1 or 2 (nothing extra for students). Ratings are **[Judgment]**, 1 to 5.

| | A. Exam Sprint ("Midterm Mode") | B. Late-Night Food Run | C. Internship Radar |
| --- | --- | --- | --- |
| Moment | "Midterm in 3 days. Syllabus: 14 pages." | "It's 1 AM. Nothing's open." | "3 postings close Friday. You found out Thursday." |
| Does | Reads Canvas exam dates and course materials, builds a countdown plan, short practice quizzes from the materials (cited), nightly check-ins, and a **phone call** wake-up on exam morning | Finds what is open, reads the dining/menu page, uses remembered diet and budget, reminds | Finds postings for the student's major, tracks deadlines, drafts cover letters (Gmail drafts, never sent) |
| Abilities | Canvas, course-material search, reminders, phone call, documents | Web, memory, reminders (browser optional) | Web, reminders, documents, Gmail drafts |
| Sign-in | 2 (Canvas connected) | 1 | 1 (2 for Gmail) |
| Student vote appeal | 5: every student has felt it | 4 | 4 |
| Buildable fast (instructions only) | 5: no scripts | 4: needs reliable open-hours data; per-campus specifics unverified | 3: job-board data quality is the risk |
| TikTok/Instagram look | 5: phone rings at 7 am, text thread shows the plan | 4: late-night relatable | 3: mostly text lists |
| Risks | Cubbie already ships `study-plan-builder` (C); we must add something it does not (quiz + call + course-material citations + countdown). Needs Canvas connected on a real account. Do not do graded work. | Cubbie never pays; student does checkout. Campus-specific data must be checked, not guessed. | Weak differentiation; applying or emailing needs the student's yes. |

**Recommendation [Judgment]: A. Exam Sprint (team is still reviewing; not confirmed).** Instructions only (fastest to build and test), the phone-call wake-up is the one thing built-in plans do not do and it films well, and it matches the kit's own "Studying" starter. Name the Skill `exam-sprint` (not a built-in name). Fallback if Canvas access fails on a test account: B.

### 2.2 Build, test, publish (full owners in `docs/tasks/track1.md`)

| # | Step | Owner |
| --- | --- | --- |
| 1 | Run `status`, confirm times on Discord; confirm each member's school email and sign-in works (`whoami`) | Dev A (Shreyas) |
| 2 | Interview via `cubbie-skill-creator`; settle moment, abilities, failure messages | Dev C (Bhavisha, lead) with Dev B (Rohan) |
| 3 | Install the kit example `canvas-deadline-nudge` on a real Cubbie once, to see the install flow | Dev D |
| 4 | Write `skills/exam-sprint/SKILL.md` (+ `references/` if needed); iMessage-style Replies section | Dev C |
| 5 | Run `validate_cubbie_skill.py`; fix every FAIL, read every warning | Dev B |
| 6 | Own test repo `Shreyas_Phase_1` in the brew-and-build org: public repo, push, run `github_link.py`, get branch link | Dev A |
| 7 | Text branch link to Cubbie; walk the 12-row on-Cubbie checklist (`cubbie-testing.md` §4) on a real Canvas account | Dev D, then Dev C |
| 8 | Fix, push, text branch link again; repeat until main flow works | Dev C + Dev B |
| 9 | Move folder to main repo `github.com/brew-and-build/brew-and-build` `skills/exam-sprint/`; rerun validator and `github_link.py` | Dev A |
| 10 | **Re-test from the main repo link** (texting it fresh to a Cubbie that does not already have the Skill, or after "remove exam-sprint") | Dev D (Shravani) + Dev C (Bhavisha) |
| 11 | Preview submission, show to the user, wait for "yes", then submit (owner only) | Dev A |

### 2.3 Submission checklist (target: submitted by Sat 5:30 PM MST, 3 h before the assumed 8:30 PM close)

- [ ] Close times confirmed on Discord (or still assumed, noted in section 0)
- [ ] Validator: no FAIL, warnings read
- [ ] Works on a real Cubbie account from the **main repo** link (row 4 to 8 of the checklist pass)
- [ ] Repo is public; clone works without sign-in (`github_link.py` confirms)
- [ ] No secrets in the repo
- [ ] Owner decided; `whoami` shows the school email the team uses
- [ ] Team name ≤ 60, project name ≤ 60, one-liner ≤ 140, all 4 members with distinct school emails, all links `https://`
- [ ] Exact preview shown to the user and an explicit "yes" received
- [ ] After sending: gallery link opened and entry looks right; link shared with team
- [ ] Demo post URL added if ready (optional)

### 2.4 Video and vote plan

**Video concept (≈20 to 30 s; length is not announced, so keep it short).**

| Time | Shot |
| --- | --- |
| 0 to 2 s (hook) | Phone buzzing at 6:58 am, caller "Cubbie", on-screen text "my midterm is at 8" |
| 2 to 8 s | Flashback text: "Midterm in 3 days, syllabus 14 pages" → Cubbie's 3-line plan |
| 8 to 18 s | Real iMessage screen recording: quiz question, student answers, Cubbie cites the lecture |
| 18 to 25 s | Exam morning call, student wakes up: "Good luck. Your first topic is…" |
| 25 to 30 s | Text: "Text Cubbie this link" + vote link + team name |

Use a real exchange only (no staged fake results). No hashtags or tags are announced; do not invent a required one.

**Vote plan.**

| Action | Detail | Owner |
| --- | --- | --- |
| Main post | TikTok or Instagram; add the post to the entry | Dev D |
| Extra posts | Up to 5 more via `posts` (each needs approval first) | Dev D |
| Reach ASU students | Class group chats, club Discords/GroupMe, roommate chats, ASU subreddit where allowed (check each venue's rules), friends in lines and labs | All, Dev D leads |
| School email reminder | Say in every post: "vote on hackathon.cubbie.ai with your ASU email (not a +alias)"; up to 5 votes each | Dev D |
| Do not | Vote for our own entry (members cannot), ask people to use `+tag` or fake accounts | All |

## 3. Track 2 vs Track 3

Comparison **[Judgment]**; judging criteria for both are "announced before kickoff" and not in the kit.

| | Track 2: Agent-to-Agent | Track 3: Group Chat Assistant |
| --- | --- | --- |
| Feasibility after Track 1 | Lower: two or more agents, shared state, confirmations, conflict logic. Needs a visible multi-agent story. | Higher: one bot in one group chat; the demo is a real chat |
| Demo impact | High if the conflict and confirmations show clearly; risky if it reads as a script | High and easy to film: friends actually chatting with it |
| Likely competition | Likely fewer teams (harder) | Likely more teams (easier, familiar) |
| Fit with our skills | Strong backend/integration (Dev A, B). Team strongest skills are still pending | Pitch/story/demo strengths (Dev C, D) shine |
| Prizes | Fitbit Charge 6 / Anker speaker | Google Home speaker / gaming mouse |

Both tracks require showing "how agents handle conflicting constraints, what they share, and when they ask their students to confirm" when multi-agent (R), and "a clear reason students would say We need this".

| Idea | Campus scenario (campus details are **[Assumption]**, verify) | Conflicting constraints | Shared | Confirms with student |
| --- | --- | --- | --- | --- |
| T2-a Study Match | Three students want a group-study slot before a shared midterm | Class times, a work shift, one student's no-late rule, room availability | Only free/busy windows and a "preferred place" tag, not full calendars | Before booking/proposing a time and before anything is sent to others |
| T2-b Split-the-Ride | Four students heading to the same off-campus event or airport trip | Departure times vs. class end times, budget cap, who can arrive early | Departure window, budget range, pickup area (not addresses) | Before joining the group, before sharing a pickup point, before any payment (student pays) |
| T3-a Plan-It Pal | Friend group chat deciding Friday plans | Study load, budget, who is free | Poll results and times, via the chat itself | Asks the group before booking; DMs one person for a private conflict |
| T3-b Project Wrangler | Group-project chat: splits tasks, tracks deadlines | Deadlines, workload, absences | Task list and due dates in the chat | Asks the assignee before reassigning or posting reminders |

**Recommendation [Judgment]: Track 3, idea T3-a (Plan-It Pal), possibly with a light multi-agent twist (each member's private preferences stay private).** Reason: higher feasibility after Track 1, strongest demo-to-effort ratio, and Dev C/D's strengths are story and demo. Switch to Track 2 only if Dev A and Dev B have clear capacity and the skills field shows an agent-framework strength. Decision is the team's.

## 4. Tech for Tracks 2/3

The kit says only "any messaging app, any open-source framework". The picks below are **our general knowledge, not from the kit [Assumption]; verify before relying**.

| Question | Pick | Why / flags |
| --- | --- | --- |
| Fastest messaging app | **Discord** (or Telegram as backup) | Bot token is self-serve, no approval wait, groups and DMs built in. WhatsApp business API and iMessage need approval or a Mac relay: slow or fragile. |
| Open-source framework | `discord.py` or `discord.js` for the bot, with LangGraph or a plain tool-calling loop for agent logic | Keep it minimal: plain loop first. |
| Model API | One hosted model API behind env variable keys | **Claude Pro is a chat subscription and does not include API credit [Assumption: verify]**; API use likely needs paid credits or a free tier with rate limits. Decide who funds it before building. |
| Needs approval/wait/paid | Discord app creation: instant, free. Hosting: Dev A picks a free tier. API credits: possibly paid. Kiro credits: use only for architecture (as you said). | Keys never in the repo. |

## 5. Timeline (Arizona time, MST)

Based on hacking start Sat 10:30 AM, Track 1 close 8:30 PM (assumed), Tracks 2/3 close Sun 12:00 PM (assumed). Sleep shifts keep one 30% dev and one 20% dev awake together at all times: **Shift A = Shreyas (30%) + Shravani (20%)** sleeps 9:30 PM to 2:30 AM; **Shift B = Rohan (30%) + Bhavisha (20%)** sleeps 2:30 AM to 7:00 AM. If it is already past a block when you read this, compress the later Track 1 blocks and keep the 5:30 PM submit.

| Time | Work | Sleeping |
| --- | --- | --- |
| Sat 10:30 to 11:30 AM | Discord confirmation; school-email sign-in check (`whoami`); confirm idea; install kit example on Cubbie | none |
| 11:00 AM to 1:30 PM | **Shreyas, between Track 1 setup tasks:** Track 2/3 groundwork (bot that connects and replies, model API connection; useful for either track) | none |
| 11:30 AM to 1:30 PM | Skill interview and draft (Bhavisha), validator (Rohan), test checklist (Shravani) | none |
| 1:30 to 3:30 PM | On-Cubbie testing in member repos; fix and re-text branch link. Shreyas: test repo + links first, then more groundwork when idle | none |
| **3:00 PM** | **Track 2 vs 3 decision** (team) | none |
| 3:30 to 4:30 PM | Move to `github.com/brew-and-build/brew-and-build` `skills/<name>/`; **re-test from the main repo link** | none |
| 4:30 to 5:30 PM | Submission preview shown to the user; explicit "yes"; **Shreyas submits Track 1 by 5:30 PM** | none |
| 4:00 to 7:00 PM | Shravani shoots/edits video in parallel; post after submit (approval first) | none |
| 5:30 to 8:30 PM | Track 1 buffer until close: fixes only (edits allowed until close); vote push starts | none |
| 3:30 to 9:30 PM | Build Track 2/3 core on the groundwork; Track 1 tasks take priority for Shreyas until 5:30 PM | none |
| 9:30 PM to 2:30 AM | Build continues (Rohan + Bhavisha) | **Shreyas + Shravani sleep** |
| Sun 2:30 to 7:00 AM | Build continues (Shreyas + Shravani) | **Rohan + Bhavisha sleep** |
| 7:00 to 7:30 AM | Everyone up; integrate | none |
| **7:30 AM** | **Feature freeze**; bug fixes and README only | none |
| 8:00 to 9:30 AM | Demo rehearsal x2 | none |
| 9:30 to 10:30 AM | Record demo video; finish README; final repo public check | none |
| 10:30 to 11:15 AM | Show exact submission to the user; explicit "yes" | none |
| **11:15 AM** | **Final Tracks 2/3 submission (Shreyas)** | none |
| 11:15 AM to 12:00 PM | Buffer; fix only if the submission fails | none |

Notes: Shreyas's groundwork must not delay Track 1 steps 9, 12, 13, 16 and 17 (his Track 1 tasks win any conflict). The model API key lives in an environment variable (Dev A edits `.env`), never in the repo; who pays for API use is still undecided (section 4). Cut order if behind is in section 7.

## 6. Missing info and assumptions

| # | Item | Status / action |
| --- | --- | --- |
| 1 | Track 1 close 8:30 PM and Tracks 2/3 close Sun 12:00 PM MST | Assumed from team lead; `status` shows no close time; confirming on Discord |
| 2 | Voting close, video length/tags, how reach is counted | Not announced; ask Discord |
| 3 | Submit repository link or folder at a pinned commit (kit vs guide) | Ask Discord; default: repository or folder link per kit |
| 4 | Test accounts for teams; whether Skills are reviewed before students see them | Ask Discord |
| 5 | Tracks 2/3 judging criteria | Not in the kit; ask Discord |
| 6 | Skill idea (Exam Sprint recommended) | Team still deciding; awaiting confirmation |
| 7 | Team names and emails | Resolved (see team table) |
| 8 | Strongest skills | Pending; affects Track 2 vs 3 |
| 9 | Four ASU emails | Resolved (see team table); `whoami` must show srevank2@asu.edu before submitting |
| 10 | Entry owner | Shreyas owns all entries (confirmed) |
| 11 | ASU campus details in Track 2/3 ideas | **[Assumption]** verify before use |
| 12 | Model API funding for Tracks 2/3 | Decide before build |

## 7. Risks

| # | Risk | Mitigation / cut first |
| --- | --- | --- |
| 1 | Deadlines are assumed (8:30 PM Sat, 12:00 PM Sun), `status` shows none | Submit Track 1 by 5:30 PM; confirm on Discord; recheck `status` every phase |
| 2 | Cubbie or Canvas test account unavailable | Test on a real member account early; fallback idea B |
| 3 | Skill overlaps the built-in `study-plan-builder` or fails install | Differentiate in description; validate; test from clean install |
| 4 | Tracks 2/3 scope too big | Cut multi-agent twist first, then second integration, then polish |
| 5 | Few votes / weak reach | Video on day one; 5 extra posts; ASU-email reminder in every post |

**What to cut first if behind:** (1) Track 2/3 extras, (2) optional website, (3) extra posts, (4) video polish. Never cut: Track 1 submission, re-test from main repo link, explicit "yes" before any submission.
