# DSA Revision Notes — how they are prepared

These notes follow the GeeksforGeeks **DSA Self Paced** course (batch `dsa-5`), in the course's own track and video order.

- **Notes page:** [`dsa-notes.html`](dsa-notes.html) (open in any browser, works offline)
- **Private link (phone):** https://claude.ai/artifact/XStbsSAnGcAdMa1AU9CBmL
- **Course:** https://www.geeksforgeeks.org/batch/dsa-5 (Resources tab)

This file is the playbook for preparing every remaining track the same way.

---

## 1. Page format

- **One HTML page.** A row of tabs at the top, one per track, in course order. Tracks not covered yet show "Not written yet".
- **Inside a tab:** one collapsible per course video, in course order, titled with the video name and duration. Each has a "Done" tick (saved in the browser only).
- **Each collapsible has two parts, the way a teacher runs a class:**
  1. **Theory:** what the video teaches, in the course's own terms.
  2. **Practice:** the problems and examples the teacher solves: problem, example input/output, code as written on the board, the dry run or working shown, and the time/space result.
- **Three kinds of box** mark where content comes from:

| Box | Meaning |
|-----|---------|
| No box | Straight from the video (transcript + board). |
| Blue **"From the article"** | From the track's Articles tab, placed under the video it matches, with a link. |
| Dashed **"Added · not in the video"** | Anything not from the course. Used only for teacher slips (where speech and board disagree) and Java notes on C/C++ board code. |

## 2. Strict content rule

Everything outside a dashed "Added" box must come from the video's transcript or board, or from a course article (in a blue box). No extra theory, complexity labels, tips or examples of my own.

- Code is copied **exactly as written on the board** (names, types, style), even if it's C/C++-style.
- If the teacher says something that contradicts the board, **follow the board** and note the slip, with its timestamp, in the "Added" box.
- If a board line can't be read clearly, write what the teacher says and list it as an uncertainty in the report.

## 3. How each video is covered

Done in Vinod's logged-in Chrome (Claude in Chrome extension), read-only.

1. **Open the video page** and record the current playback time (the resume position).
2. **Pause the video** immediately. It is never played, so course progress is not changed.
3. **Read the full transcript** from the course's own Transcript button (start to end).
4. **Step through the whole video while paused:** jump to a frame **every 5 seconds** from 0:00 to the end, and take extra **close-ups wherever the board changes** (new code, working, diagrams, examples). Match each frame to the transcript at that timestamp.
5. **Write the collapsible** from the transcript and frames only (rules above).
6. **Restore the resume position** recorded in step 1 before leaving the page.
7. **Republish** the page after each video so progress is visible.

Technical note: the frames are drawn onto a canvas overlay on the page (12 frames per contact sheet, 5 s apart), plus a full-size canvas for close-ups. This avoids playing the video and hides the player controls and captions so the board is readable.

## 4. Articles

- Open each item in the track's **Articles** tab and read it.
- **Never click "Mark as Read".** Just viewing the article doesn't change progress.
- Put the article's points in a blue "From the article" box under the video it matches, with a link to the article. Article-only content stays in that box.

## 5. Practice problems

When a track has a **Problems** tab, add each problem with its course link. Problems solved in a video go in that video's Practice part. Problems not solved in any video go in a final "Track practice set" collapsible for the track.

## 6. After each track

Report back with:
- what was covered (videos, articles, problems)
- confirmation that resume positions were restored and nothing was marked as watched or read
- every teacher slip (timestamp, what was said, what the board shows)
- any uncertainties (unreadable board, ambiguous working)

**Wait for Vinod's go before starting the next track.** Commit and push only when he asks:
- Author and committer: **Vinod Kumar <vinodkgupta.1996@gmail.com>**, set per commit with `git -c user.name=... -c user.email=...` (global git config is never changed)
- **No** `Co-Authored-By` or other Claude trailer lines in commit messages

## 7. Progress

| # | Track | Videos | Articles | Status |
|---|-------|-------:|---------:|--------|
| 1 | Analysis of Algorithms | 15 | 6 | Done (no Problems tab in this track) |
| 2 | Mathematics | 12 | 13 | Next |
| 3–24 | Bit Magic … Disjoint Set | | | Not started |

### Analysis of Algorithms: teacher slips flagged
- V2 10:56: "fun1 takes more time than fun2"; the board shows fun2, after n = 999.
- V6 3:52: "2n+3 ≥ 3n"; the board has ≤. 10:26: "i ≥ √n"; the loop means i ≤ √n.
- V7: "Big O of log n" where Ω(log n) is meant; "c equal to n" is c = 1; "−3 ≥ n" is −3 ≤ n.
- V8 2:50: calls c₂ the "Theta" constant; it is the Big O (upper) side.
- V10 3:48: "Θ(n) times" for the m-loop; the board gives Θ(m²).
- V15: `c` is undeclared in the board's Fibonacci code; `int f[n+1]` is C++ (Java: `int[] f = new int[n + 1];`).
