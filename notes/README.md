# DSA Revision Notes — how they are prepared

These notes follow the GeeksforGeeks **DSA Self Paced** course (batch `dsa-5`), in the course's own track and video order.

- **Notes page:** [`dsa-notes.html`](dsa-notes.html) (open in any browser, works offline)
- **Private link (phone):** https://claude.ai/artifact/XStbsSAnGcAdMa1AU9CBmL (Track 1 only; it belongs to another Claude account, so from Track 2 on the notes are kept local only)
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
3. **Read the full transcript** from the course's own Transcript button (start to end), when the video has one. Only some videos do (in Track 2, only videos 8 and 10). If a video has no Transcript button and no captions, write the notes from the frames and the video's course Description only, and say so at the top of that video's notes. Spoken slips can't be checked for those videos.
4. **Step through the whole video while paused:** jump to a frame **every 5 seconds** from 0:00 to the end, and take extra **close-ups wherever the board changes** (new code, working, diagrams, examples). Match each frame to the transcript at that timestamp.
5. **Write the collapsible** from the transcript and frames only (rules above).
6. **Restore the resume position** recorded in step 1 before leaving the page.
7. **Republish** the page after each video so progress is visible (Track 1 only; see the private link note above).

Technical note: the frames are drawn onto a canvas overlay on the page (12 frames per contact sheet, 5 s apart), plus a full-size canvas for close-ups. This avoids playing the video and hides the player controls and captions so the board is readable.

## 4. Articles

- Open each item in the track's **Articles** tab and read it.
- **Never click "Mark as Read".** Just viewing the article doesn't change progress.
- Put the article's points in a blue "From the article" box under the video it matches, with a link to the article. Article-only content stays in that box.

## 5. Practice problems

When a track has a **Problems** tab, add each problem with its course link. Problems solved in a video go in that video's Practice part. Problems not solved in any video go in a final "Track practice set" collapsible for the track (a `<template id="<trackId>-practice">` in the page).

## 6. After each track

Report back with:
- what was covered (videos, articles, problems)
- confirmation that resume positions were restored and nothing was marked as watched or read
- every teacher slip (timestamp, what was said, what the board shows)
- any uncertainties (unreadable board, ambiguous working)

**Wait for Vinod's go before starting the next track.** Commit and push only when he asks:
- Author and committer: **Vinod Kumar <vinodkgupta.1996@gmail.com>**, set per commit with `git -c user.name=... -c user.email=...` (global git config is never changed)
- **No** `Co-Authored-By` or other Claude trailer lines in commit messages

## 7. Progress (as of 2026-11-09)

**Notes written: 2 of 24 tracks · 27 of 470 videos · 19 of 342 articles · 11 of 367 problems listed.** All work is on branch `claude/project-thread-8jxc30`. Track 1 is also in the private artifact.

| # | Track | Videos | Articles | Problems | Notes status |
|---|-------|-------:|---------:|---------:|--------------|
| 1 | Analysis of Algorithms | 15 | 6 | – | ✅ Done: 15/15 videos, 6/6 articles |
| 2 | Mathematics | 12 | 13 | 11 | ✅ Done: 12/12 videos, 13/13 articles, 11 problems |
| 3 | Bit Magic | 12 | 11 | 12 | ⏭ Next |
| 4 | Recursion | 17 | 12 | 12 | Not started |
| 5 | Arrays | 31 | 27 | 27 | Not started |
| 6 | Searching | 18 | 13 | 18 | Not started |
| 7 | Sorting | 39 | 29 | 20 | Not started |
| 8 | Matrix | 12 | 11 | 15 | Not started |
| 9 | Hashing | 29 | 23 | 22 | Not started |
| 10 | Strings | 19 | 12 | 26 | Not started |
| 11 | Linked List | 54 | 40 | 25 | Not started |
| 12 | Stack | 27 | 19 | 17 | Not started |
| 13 | Queue | 9 | 5 | 9 | Not started |
| 14 | Deque | 8 | 7 | 6 | Not started |
| 15 | Tree | 30 | 24 | 32 | Not started |
| 16 | Binary Search Tree | 28 | 16 | 23 | Not started |
| 17 | Heap | 14 | 11 | 11 | Not started |
| 18 | Graph | 30 | 20 | 24 | Not started |
| 19 | Greedy | 12 | 5 | 6 | Not started |
| 20 | Backtracking | 4 | 4 | 7 | Not started |
| 21 | Dynamic Programming | 31 | 25 | 28 | Not started |
| 22 | Trie | 4 | 3 | 6 | Not started |
| 23 | Segment and Binary Indexed Trees | 10 | 3 | 6 | Not started |
| 24 | Disjoint Set | 5 | 3 | 4 | Not started |

### Track 1: Analysis of Algorithms, per video

| # | Video | Duration | Articles folded in |
|---|-------|---------:|--------------------|
| 1 | Analysis of Algorithms (Background) | 6:20 | Analysis of Algorithms (Background) |
| 2 | Asymptotic Analysis | 13:10 | |
| 3 | Order of Growth | 9:41 | |
| 4 | Best, Average and Worst cases | 6:54 | Worst, Average and Best Case Time Complexities |
| 5 | Asymptotic Notation | 7:05 | Asymptotic Notations |
| 6 | Big O Notation | 13:10 | Big O Notation |
| 7 | Omega Notation | 8:56 | Omega Notation |
| 8 | Theta Notation | 8:33 | Theta Notation |
| 9 | Analysis of Common loops | 9:16 | |
| 10 | Analysis of multiple loops | 5:03 | |
| 11 | Analysis of Recursion (Introduction) | 4:06 | |
| 12 | Recursion Tree Method for Solving Recurrences | 6:34 | |
| 13 | More Example Recurrences | 5:23 | |
| 14 | Upper Bounds Using Recursion Tree Method | 7:06 | |
| 15 | Space Complexity | 22:37 | |

Method notes for track 1: video 1 was first done from a few frames, then redone with a full pass (a frame at least every 10 s). Videos 2–15 used a frame every 5 s plus close-ups. Course progress was unchanged throughout (12/15 videos watched, 68%), and every resume position was restored.

### Track 2: Mathematics, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Count Digits | 3:00 | Board + description | Count Digits |
| 2 | Palindrome Numbers | 7:25 | Board + description | Palindrome Numbers |
| 3 | Factorial of a Number | 5:30 | Board + description | Factorial of a Number |
| 4 | Trailing Zeros in Factorial | 8:57 | Board + description | Trailing Zeros in Factorial |
| 5 | GCD or HCF of two Numbers | 10:22 | Board + description | GCD or HCF of two Numbers |
| 6 | LCM of Two Numbers | 3:56 | Board + description | LCM of Two Numbers |
| 7 | Check for Prime | 14:16 | Board + description | Check for Prime |
| 8 | Prime Factors | 17:31 | **Transcript** + board | Prime Factors |
| 9 | All Divisors of a Number | 9:34 | Board + description | All Divisors of a Number |
| 10 | Sieve of Eratosthenes | 13:51 | **Transcript** + board | Sieve of Eratosthenes |
| 11 | Computing Power | 6:08 | Board + description | Computing Power |
| 12 | Iterative Power | 9:25 | Board + description | Iterative Power, Modular Arithmetic |

Method notes for track 2: 10 of the 12 videos have no Transcript button and no captions (checked on each page), so they were done from the frames and the course description. Ways tried to get the speech for those, all dropped: downloading the audio for offline transcription (the video server refuses direct requests), Chrome Live Caption (not visible in screenshots), and recording the audio in the page (couldn't be copied out). The 11 problems are in a "Track practice set" at the end of the tab. Course progress was unchanged throughout (12/12 videos watched, 50%, 0/13 articles read), and every resume position was restored.

### Open uncertainties
- V9, example 5: the boxed final answer on the board is hard to read (the bases look swapped). The notes use the derivation as written (k < log_c log₂ n + 1) and Θ(log log n), as the teacher says.
- Some board code is C/C++-style (`bool`, `print`, `pow`, `int f[n+1]`). It's kept as written, with Java differences noted only where relevant.
- Maths V8: the naive solution's board complexity is O(n log n). The description says O(n·√n·log n). With an O(n) isPrime it would be O(n² log n). The notes keep the board's value and flag it.
- Maths V11: the final answer of the T(n) recursion tree isn't legible. Θ(log n) is taken from the description.
- Maths V12: the labels under "5 : 0101" look like 4⁴ 4³ 4² 4¹ (they should be 4⁸ 4⁴ 4² 4¹). The result, 4⁴ × 4¹ = 1024, is right either way.
- Maths V1 (`res` variable name), V5 (an erased note) and V7 (a line hidden by the teacher's hand) are minor board-reading doubts.

### Commits so far (branch `claude/project-thread-8jxc30`)
- `8b14d49`: Add DSA revision notes: Analysis of Algorithms track (15 videos + articles)
- `6e573a4`: Document how the DSA revision notes are prepared
- `660bdd5`: Notes playbook: wait for go before next track
- `4e205f8`: Notes: add progress log
- (this commit): Add Mathematics track notes (12 videos, 13 articles, 11 problems)

### What's next
- **Track 3: Bit Magic** (12 videos, 11 articles, 12 problems), using the same method. **Waiting for the go.**

### History
- **2026-11-10:**
  - Agreed the format (track tabs, per-video Theory + Practice) and the strict "course content only" rule.
  - Did a trial on video 1.
  - Completed all of track 1, and folded in the 6 articles.
  - Committed the notes and this playbook.
- **2026-11-09:**
  - Completed all of track 2 (Mathematics): 12 videos, 13 articles, 11 problems.
  - Found that only some videos have the Transcript button. The rest were done from the board and course description, which is now part of the method.
  - The private artifact is on another account, so Track 2 is kept local only.

### Analysis of Algorithms: teacher slips flagged
- V2 10:56: "fun1 takes more time than fun2"; the board shows fun2, after n = 999.
- V6 3:52: "2n+3 ≥ 3n"; the board has ≤. 10:26: "i ≥ √n"; the loop means i ≤ √n.
- V7: "Big O of log n" where Ω(log n) is meant; "c equal to n" is c = 1; "−3 ≥ n" is −3 ≤ n.
- V8 2:50: calls c₂ the "Theta" constant; it is the Big O (upper) side.
- V10 3:48: "Θ(n) times" for the m-loop; the board gives Θ(m²).
- V15: `c` is undeclared in the board's Fibonacci code; `int f[n+1]` is C++ (Java: `int[] f = new int[n + 1];`).

### Mathematics: teacher slips flagged
- V10 ~7:27 (board): "Mark 3, 6 and 9 as False" for i = 3. It should be 6 and 9, as the teacher says and the array on the board shows.
- V8 (auto-generated transcript vs. board): 0:50 "write only 30" (board: 13); 2:03 "x equal to Y … x divides I" (board: `int x = i; while (n % x == 0)`); 3:37 "2 to 3" (output 2 2 3); 9:33 "250" (450); 14:13 "57" (5, 7); 17:27 "√M" (√n).
- V10 (transcript): 0:24 "And equal to 23" (n = 23); 9:51 "up to 60" (16); 10:52 "We need to buy now" ("But now").
- Board vs. description examples: V2 uses 367 where the description has 837. V9 uses 15 and 7 where the description has 10 and 125.
- Videos without a transcript (1–7, 9, 11, 12): spoken slips couldn't be checked.
