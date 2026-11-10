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
4. **Step through the whole video while paused:** first check every video in the track for the Transcript button. Videos **with** a transcript get a frame **every 10 seconds** (sheets of 20). Videos **without** one get a frame **every 5 seconds**. Both get **close-ups wherever the board changes** (new code, working, diagrams, examples), skipped when a sheet already shows the board clearly. Match each frame to the transcript at that timestamp. Close the transcript panel before clicking the sidebar, because clicking a transcript row seeks the video.
5. **Write the collapsible** from the transcript and frames only (rules above).
6. **Restore the resume position** recorded in step 1 before leaving the page.
7. **Republish** the page after each video so progress is visible (Track 1 only; see the private link note above).

Technical note: the frames are drawn onto a canvas overlay on the page (12 frames per contact sheet, 5 s apart), plus a full-size canvas for close-ups. This avoids playing the video and hides the player controls and captions so the board is readable.

## 4. Articles

- Open each item in the track's **Articles** tab and read it (from the page text, not by scrolling screenshots).
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

**Commit once each track is finished, then go straight on to the next track** (instruction of 2026-11-09; no need to wait for a go). Push only when asked:
- Author and committer: **Vinod Kumar <vinodkgupta.1996@gmail.com>**, set per commit with `git -c user.name=... -c user.email=...` (global git config is never changed)
- **No** `Co-Authored-By` or other Claude trailer lines in commit messages

## 7. Progress (as of 2026-11-09)

**Notes written: 6 of 24 tracks · 105 of 470 videos · 82 of 342 articles · 80 of 367 problems listed.** All work is on branch `claude/project-thread-8jxc30`. Track 1 is also in the private artifact.

| # | Track | Videos | Articles | Problems | Notes status |
|---|-------|-------:|---------:|---------:|--------------|
| 1 | Analysis of Algorithms | 15 | 6 | – | ✅ Done: 15/15 videos, 6/6 articles |
| 2 | Mathematics | 12 | 13 | 11 | ✅ Done: 12/12 videos, 13/13 articles, 11 problems |
| 3 | Bit Magic | 12 | 11 | 12 | ✅ Done: 12/12 videos, 11/11 articles, 12 problems |
| 4 | Recursion | 17 | 12 | 12 | ✅ Done: 17/17 videos, 12/12 articles, 12 problems |
| 5 | Arrays | 31 | 27 | 27 | ✅ Done: 31/31 videos, 27/27 articles, 27 problems |
| 6 | Searching | 18 | 13 | 18 | ✅ Done: 18/18 videos, 13/13 articles, 18 problems |
| 7 | Sorting | 39 | 29 | 20 | ⏭ Next |
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

### Track 3: Bit Magic, per video

All 12 videos have the course transcript. Frames every 10 s plus close-ups.

| # | Video | Duration | Articles folded in |
|---|-------|---------:|--------------------|
| 1 | Bitwise Operators in CPP (Part 1) | 4:59 | Bitwise Algorithms Basics |
| 2 | Bitwise Operators in CPP (Part 2) | 11:09 | Bit Algorithms, Important Tactics |
| 3 | Bitwise Operator in Java (Part 1) | 3:14 | |
| 4 | Bitwise Operators in Java (Part 2) | 7:43 | |
| 5 | Bitwise Operators in Java (Part 3) | 5:35 | |
| 6 | Binary Representation of Negative Numbers | 10:21 | |
| 7 | Check if Kth bit is set or not | 7:48 | Check if Kth bit is set or not |
| 8 | Count Set Bits | 17:12 | Count Set Bits |
| 9 | Power of Two | 6:30 | Power of Two, Basic Problems on Bit Manipulation |
| 10 | One Odd Occurring | 7:35 | One Odd Occurring |
| 11 | Two Odd Occurring | 11:15 | Two Odd Occurring |
| 12 | Power Set using Bitwise | 6:34 | Power Set using Bitwise |

The two "Maximum AND value" articles match no video, so they're in the Track practice set with the 12 problems. Course progress was unchanged (2/12 videos watched, 32%, 0/11 articles read). Resume positions: V1 0:06, the rest 0:00, all restored. Once, a click landed on a transcript row and moved the paused V12 to 6:01. It didn't play and was set back to 0:00.

### Track 4: Recursion, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Recursion Introduction | 11:49 | Transcript + board | Recursion Introduction |
| 2 | Applications of Recursion | 5:24 | Transcript + board | |
| 3 | Recursion Output Practice - Part 1 | 6:25 | Transcript + board | |
| 4 | Recursion Output Practice - Part 2 | 10:52 | Transcript + board | |
| 5 | Print N to 1 Using Recursion | 4:07 | Board + description | Print N to 1 |
| 6 | Print 1 to N Using Recursion | 4:53 | Transcript + board | Print 1 to N |
| 7 | Tail Recursion | 10:22 | Transcript + board | Tail Recursion |
| 8 | Writing Base Cases in Recursion | 7:28 | Transcript + board | |
| 9 | Natural Number Sum using Recursion | 5:48 | Transcript + board | Natural Number Sum |
| 10 | Palindrome Check using Recursion | 8:39 | Board + description | Palindrome Check |
| 11 | Sum of Digits Using Recursion | 5:17 | Transcript + board | Sum of Digits |
| 12 | Rope Cutting Problem | 10:18 | Transcript + board | Rope Cutting Problem |
| 13 | Generate Subsets | 8:21 | Board + description | Generate Subsets |
| 14 | Tower of Hanoi | 19:20 | Transcript + board | Tower of Hanoi |
| 15 | Josephus Problem | 22:36 | Board + description | Josephus Problem |
| 16 | Subset Sum Problem (Recursive Solution) | 10:53 | Transcript + board | |
| 17 | Printing all Permutations | 11:10 | Transcript + board | Printing all Permutations |

Course progress was unchanged (9/17 videos watched, 57%, 0/12 articles read). All resume positions were 0:00 and were restored.

### Track 5: Arrays, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Introduction to Arrays | 6:03 | Transcript + board | Introduction to Arrays |
| 2 | Array Types | 6:10 | Transcript + board |  |
| 3 | Vector in C++ | 7:11 | Transcript + board | Implementing Arrays in C++ using STL; Iterators in C++ STL |
| 4 | ArrayList in Java | 4:59 | Transcript + board | Implementing Arrays in Java |
| 5 | Operations on Arrays (Part 1) | 11:21 | Transcript + board | Operations on Arrays |
| 6 | Operations on Arrays (Part 2) | 5:51 | Transcript + board | Insertion and Deletion in Arrays |
| 7 | Largest Element in an Array | 9:44 | Transcript + board | Largest Element in an Array |
| 8 | Second Largest Element in Array | 12:42 | Transcript + board | Second Largest Element in Array |
| 9 | Check if an Array is Sorted | 7:30 | Transcript + board | Check if an Array is Sorted |
| 10 | Reverse an Array | 5:14 | Transcript + board | Reverse an Array |
| 11 | Remove duplicates from a sorted array | 8:57 | Transcript + board | Remove duplicates from a sorted array |
| 12 | Move Zeros to End | 7:56 | Transcript + board | Move Zeros to End |
| 13 | Left Rotate an Array by One | 2:50 | Transcript + board |  |
| 14 | Left Rotate an Array by D places | 9:49 | Transcript + board | Left Rotate an Array by D places |
| 15 | Leaders in an Array problem | 9:52 | Transcript + board | Leaders in an Array problem |
| 16 | Maximum Difference Problem with Order | 8:04 | Transcript + board | Maximum Difference Problem with Order |
| 17 | Frequencies in a Sorted Array | 6:59 | Transcript + board | Frequencies in a Sorted Array |
| 18 | Stock Buy and Sell Problem (Part 1) | 6:57 | Transcript + board |  |
| 19 | Stock Buy and Sell problem (Part 2) | 4:43 | Transcript + board | Stock Buy and Sell Problem |
| 20 | Trapping Raining Water | 23:20 | Transcript to 2:10 + board | Trapping Rain Water |
| 21 | Maximum consecutive 1s | 4:58 | Transcript + board |  |
| 22 | Maximum subarray sum | 11:18 | Board + description | Maximum Subarray Sum |
| 23 | Longest Even Odd Subarray | 8:28 | Transcript + board | Longest Even Odd Subarray |
| 24 | Maximum Circular Sum Subarray | 18:31 | Transcript + board | Maximum Circular Sum Subarray |
| 25 | Majority Element | 13:43 | Transcript + board | Majority Element |
| 26 | Minimum Consecutive Flips | 14:42 | Transcript + board | Minimum Consecutive Flips |
| 27 | Sliding Window Technique | 8:20 | Transcript + board | Sliding Window Technique |
| 28 | Subarray with Given Sum | 9:01 | Transcript + board |  |
| 29 | Prefix Sum | 9:35 | Transcript + board | Prefix Sum Technique |
| 30 | Equilibrium Point | 8:20 | Transcript + board |  |
| 31 | Maximum Appearing Element | 10:09 | Board + description | Maximum Appearing Element |

The "Sample Problems on Array" article matches no single video, so it's in the Track practice set with the 27 problems (the Problems tab shows a level for each, so the table lists it). V20's course transcript stops at 2:10 of 23:20 and its description is empty, so the rest was done from 5 s frames; V22 and V31 have no Transcript button and were done from 5 s frames and the description. From V21 on, each transcript grab also checks the last timestamp, to catch a cut-off transcript like V20's. Course progress was unchanged (20/31 videos watched, 52%, no article marked as read). All resume positions were 0:00 and were restored.

### Track 6: Searching, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Binary Search (Iterative) | 11:12 | Transcript + board | Binary Search Functions in C++ STL; BinarySearch using Built-in Methods in Java |
| 2 | Binary Search (Recursive) | 9:17 | Transcript + board | Binary Search (Recursive) |
| 3 | Analysis of Binary Search | 9:10 | Transcript + board |  |
| 4 | Index of first Occurrence in Sorted | 8:58 | Transcript + board | Index of first Occurrence and last Occurrence in Sorted |
| 5 | Index of last Occurrence in Sorted | 8:48 | Transcript + board |  |
| 6 | Count Occurrences in Sorted | 5:14 | Transcript + board | Count Occurrences in Sorted |
| 7 | Count 1s in a Sorted Binary Array | 6:09 | Transcript + board | Count 1s in a Sorted Binary Array |
| 8 | Square root | 8:29 | Transcript + board | Square root |
| 9 | Search in Infinite Sized Array | 10:19 | Transcript + board | Search in an Infinite Sized Array |
| 10 | Search in Sorted Rotated Array | 15:44 | Board + description |  |
| 11 | Find a Peak Element | 10:54 | Transcript + board | Find a Peak Element |
| 12 | Two Pointers Approach | 11:06 | Transcript + board |  |
| 13 | Triplet in a Sorted Array | 8:26 | Transcript + board |  |
| 14 | Median of two sorted arrays | 25:52 | Transcript + board | Median of Two Sorted Arrays |
| 15 | Repeating Elements Part (1) | 6:19 | Board + description |  |
| 16 | Repeating Elements Part (2) | 13:47 | Board + description |  |
| 17 | Allocate Minimum Pages (Naive Method) | 8:54 | Board + description |  |
| 18 | Allocate Minimum Pages (Binary Search) | 11:30 | Transcript + board | Allocate Minimum Pages |

"Ternary Search" and "Sample Problems on Searching" match no video, so they're in the Track practice set with the 18 problems. The first/last occurrence article covers both V4 and V5 and sits under V4. V10, V15, V16 and V17 have no Transcript button and were done from 5 s frames and the description. Course progress was unchanged (4/18 videos watched, 42%, no article marked as read). All resume positions were 0:00 and were restored. The built-in browser could no longer open the local page (about 600 KB), so the render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 18 Searching videos.

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
- `bffb328`: Add DSA revision notes: Mathematics track (12 videos, 13 articles, 11 problems)
- `002a7e3`: Add DSA revision notes: Bit Magic track (12 videos, 11 articles, 12 problems)
- `e864134`: Add Recursion track notes (17 videos, 12 articles, 12 problems)
- `f9e9cf3`: Add Arrays track notes (31 videos, 27 articles, 27 problems)
- (this commit): Add Searching track notes (18 videos, 13 articles, 18 problems)

### What's next
- **Track 7: Sorting** (39 videos, 29 articles, 20 problems), starting straight away.

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
  - Switched to the faster method (10 s frames for videos with a transcript, page-text article reading).
  - Completed track 3 (Bit Magic): 12 videos, 11 articles, 12 problems. Commit after each track and continue without waiting.
  - Completed track 4 (Recursion): 17 videos, 12 articles, 12 problems.
- **2026-11-10:**
  - Completed track 5 (Arrays): 31 videos, 27 articles, 27 problems.
  - Completed track 6 (Searching): 18 videos, 13 articles, 18 problems.

### Analysis of Algorithms: teacher slips flagged
- V2 10:56: "fun1 takes more time than fun2"; the board shows fun2, after n = 999.
- V6 3:52: "2n+3 ≥ 3n"; the board has ≤. 10:26: "i ≥ √n"; the loop means i ≤ √n.
- V7: "Big O of log n" where Ω(log n) is meant; "c equal to n" is c = 1; "−3 ≥ n" is −3 ≤ n.
- V8 2:50: calls c₂ the "Theta" constant; it is the Big O (upper) side.
- V10 3:48: "Θ(n) times" for the m-loop; the board gives Θ(m²).
- V15: `c` is undeclared in the board's Fibonacci code; `int f[n+1]` is C++ (Java: `int[] f = new int[n + 1];`).

### Recursion: teacher slips flagged
- V11 (board): the iterative sum-of-digits loop is `while (n >= 0)`, which never ends once n is 0. It should be `n > 0`.
- V9 ~4:50: "at most n − 1 functions in the call stack". The teacher then says n + 1.
- V7: the board's "Equivalent Tail Recursive" print-1-to-n uses an extra parameter k (start at 1). The left-hand factorial on the last board is partly hidden.
- V14: the board's print strings have no spaces ("Move 1 from" + A + "to" + C).
- V15 (no transcript): the course's Josephus uses 0-based positions (n = 7, k = 3 → 3). The article uses 1-based (n = 7, k = 3 → 4), with `myJos` = jos + 1 bridging the two.
- Videos without a transcript (5, 10, 13, 15): spoken slips couldn't be checked.

### Searching: teacher slips flagged
- V3: "high is 15" and "an array of size 16"; the board array is a0 … a14 (15 elements). The board's edge label "x > a15" means x > a13.
- V4: "initialize low 0 and high as −1"; the board has `high = n-1`.
- V5 (board): the recursive calls leave out x (`lastOcc(arr, low, mid-1, n)`), and the iterative condition is written `mid != n-1` where `mid == n-1` is meant. "We return 10" means index 4.
- V8: "while i·i is more than equal to x" (board `<=`); "log x … is greater than x^½" (it's smaller).
- V9: the walkthrough uses a different array from the board; "10 is more than a hundred" means smaller. The binary search range is spoken as i/2 + 1 to i − 1 but the dry run writes (4, 8).
- V12/V13: in V13 the board calls `isPair(arr, x - arr[i], i+1)` without n.
- V14 (board): Java's odd case writes `max` without `Math.`, and neither version returns after the loop.
- V10, V15, V16, V17 (no transcript): spoken slips couldn't be checked.
- Board notation: `&&` is handwritten like "$$" and `||` like "¦¦" throughout.

### Arrays: teacher slips flagged
- V9: the transcript calls "5, 20, 100, 80" sorted, then walks it as 5, 20, 80, 100.
- V11: "if it is same as the last copied element, we … copy". The board copies only when it differs (`!=`).
- V12 (board): the naive inner loop has no `break` after the swap, though the teacher describes swapping with the first non-zero only. The Java line is written `arr.length()`.
- V14 (board): the naive `leftRotate(arr, n, d)` calls `leftRotate(arr, n)` instead of `leftRotateOne`. Spoken: "n is 5 and D is 3" (d is 2). "Subtract n from d" only covers n < d < 2n.
- V18: "keeping the profit as 30"; the profit kept is 13.
- V21: the C++ efficient code declares only `res`. The Java takes `boolean arr[]` but compares with `== 1`.
- V22 (no transcript): the efficient `maxSum(int arr[], int sum)` loops on `n`.
- V23 (board): `arr[i-1] == 0` should be `arr[i-1] % 2 == 0`.
- V24 (board): the last example is written {−5, −3}; its working uses {−8, −3}.
- V29 (board): `int arr = {…};` needs `[]`; the dry run "getSum(6, 2)" computes getSum(2, 6).
- V30: the first example array differs from the dry-run array (flagged as an example mismatch).
- V31 (no transcript, board): the naive inner loop increments `i++` instead of `j++`.
- Board notation: `&&` is handwritten like "$$" (V17, V23).

### Bit Magic: teacher slips flagged
- V6 ~6:37 and 7:41: says Python has `unsigned` ints, alongside C/C++. Python has no unsigned type.
- V12 (board): `if (i & (1 << j) != 0)`. `!=` binds tighter than `&`, so it needs brackets: `(i & (1 << j)) != 0`.
- V8: the board spells "Brian Kerningam's", and the transcript says "Cunningham". The usual spelling is Kernighan.
- V2: the unsigned `~` outputs (4294967294, 4294967290) are only seen in 10 s sheets, but they match the speech.
- All videos: the auto-generated transcripts mishear numbers often ("to" for 2, "it" for 8, "60" for 16). Each video's notes list these.
- Board notation: `&` is handwritten like "$" throughout the track.

### Mathematics: teacher slips flagged
- V10 ~7:27 (board): "Mark 3, 6 and 9 as False" for i = 3. It should be 6 and 9, as the teacher says and the array on the board shows.
- V8 (auto-generated transcript vs. board): 0:50 "write only 30" (board: 13); 2:03 "x equal to Y … x divides I" (board: `int x = i; while (n % x == 0)`); 3:37 "2 to 3" (output 2 2 3); 9:33 "250" (450); 14:13 "57" (5, 7); 17:27 "√M" (√n).
- V10 (transcript): 0:24 "And equal to 23" (n = 23); 9:51 "up to 60" (16); 10:52 "We need to buy now" ("But now").
- Board vs. description examples: V2 uses 367 where the description has 837. V9 uses 15 and 7 where the description has 10 and 125.
- Videos without a transcript (1–7, 9, 11, 12): spoken slips couldn't be checked.
