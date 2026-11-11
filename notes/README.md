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

## 7. Progress (as of 2026-11-10)

**Notes written: 24 of 24 tracks · 470 of 470 videos · 342 of 342 articles · 367 of 367 problems listed.** All work is on branch `claude/project-thread-8jxc30`. Track 1 was written by Claude, and tracks 2–24 were added by Vinod, in the same `dsa-notes.html`. The private artifact still shows only track 1 (see What's next).

| # | Track | Videos | Articles | Problems | Notes status |
|---|-------|-------:|---------:|---------:|--------------|
| 1 | Analysis of Algorithms | 15 | 6 | – | ✅ Done: 15/15 videos, 6/6 articles |
| 2 | Mathematics | 12 | 13 | 11 | ✅ Done: 12/12 videos, 13/13 articles, 11 problems |
| 3 | Bit Magic | 12 | 11 | 12 | ✅ Done: 12/12 videos, 11/11 articles, 12 problems |
| 4 | Recursion | 17 | 12 | 12 | ✅ Done: 17/17 videos, 12/12 articles, 12 problems |
| 5 | Arrays | 31 | 27 | 27 | ✅ Done: 31/31 videos, 27/27 articles, 27 problems |
| 6 | Searching | 18 | 13 | 18 | ✅ Done: 18/18 videos, 13/13 articles, 18 problems |
| 7 | Sorting | 39 | 29 | 20 | ✅ Done: 39/39 videos, 29/29 articles, 20 problems |
| 8 | Matrix | 12 | 11 | 15 | ✅ Done: 12/12 videos, 11/11 articles, 15 problems |
| 9 | Hashing | 29 | 23 | 22 | ✅ Done: 29/29 videos, 23/23 articles, 22 problems |
| 10 | Strings | 19 | 12 | 26 | ✅ Done: 19/19 videos, 12/12 articles, 26 problems |
| 11 | Linked List | 54 | 40 | 25 | ✅ Done: 54/54 videos, 40/40 articles, 25 problems |
| 12 | Stack | 27 | 19 | 17 | ✅ Done: 27/27 videos, 19/19 articles, 17 problems |
| 13 | Queue | 9 | 5 | 9 | ✅ Done: 9/9 videos, 5/5 articles, 9 problems |
| 14 | Deque | 8 | 7 | 6 | ✅ Done: 8/8 videos, 7/7 articles, 6 problems |
| 15 | Tree | 30 | 24 | 32 | ✅ Done: 30/30 videos, 24/24 articles, 32 problems |
| 16 | Binary Search Tree | 28 | 16 | 23 | ✅ Done: 28/28 videos, 16/16 articles, 23 problems |
| 17 | Heap | 14 | 11 | 11 | ✅ Done: 14/14 videos, 11/11 articles, 11 problems |
| 18 | Graph | 30 | 20 | 24 | ✅ Done: 30/30 videos, 20/20 articles, 24 problems |
| 19 | Greedy | 12 | 5 | 6 | ✅ Done: 12/12 videos, 5/5 articles, 6 problems |
| 20 | Backtracking | 4 | 4 | 7 | ✅ Done: 4/4 videos, 4/4 articles, 7 problems |
| 21 | Dynamic Programming | 31 | 25 | 28 | ✅ Done: 31/31 videos, 25/25 articles, 28 problems |
| 22 | Trie | 4 | 3 | 6 | ✅ Done: 4/4 videos, 3/3 articles, 6 problems |
| 23 | Segment and Binary Indexed Trees | 10 | 3 | 6 | ✅ Done: 10/10 videos, 3/3 articles, 6 problems |
| 24 | Disjoint Set | 5 | 3 | 4 | ✅ Done: 5/5 videos, 3/3 articles, 4 problems |

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

### Track 7: Sorting, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Overview of sorting algorithm | 15:18 | Transcript + board | Introduction to Sorting |
| 2 | Sort in C++ STL | 9:16 | Transcript + board | Sort in C++ STL |
| 3 | Sorting in Java | 5:09 | Transcript + board | Sorting using Built-in methods in Java |
| 4 | Arrays.sort in Java | 9:58 | Transcript + board | Arrays.sort() in Java |
| 5 | Collections.Sort in Java | 6:26 | Transcript + board | Collections.sort() in Java |
| 6 | Stability in Sorting Algorithm | 8:28 | Transcript + board | Stability in Sorting Algorithm |
| 7 | Bubble Sort | 12:13 | Transcript + board | Bubble Sort |
| 8 | Selection Sort | 10:14 | Transcript + board | Selection Sort |
| 9 | Insertion Sort | 12:35 | Transcript + board | Insertion Sort |
| 10 | Merge sort introduction | 2:25 | Transcript + board |  |
| 11 | Merge two sorted arrays | 11:25 | Transcript + board | Merge two Sorted Arrays |
| 12 | Merge function of Merge sort | 6:27 | Board + description | Merge function of Merge sort |
| 13 | Merge Sorting Algorithm | 15:01 | Transcript + board | Merge Sort |
| 14 | Merge Sort Analysis | 7:39 | Transcript + board | Merge Sort Analysis |
| 15 | Intersection of two sorted arrays | 8:27 | Board + description |  |
| 16 | Union of two sorted arrays | 10:41 | Transcript + board |  |
| 17 | Count inversions in Array | 14:56 | Transcript + board |  |
| 18 | Naive partition | 5:25 | Transcript + board | Naive Partition |
| 19 | Lomuto Partition | 17:45 | Transcript + board | Lomuto Partition |
| 20 | Hoare partition | 16:39 | Transcript + board | Hoare Partition |
| 21 | Quick Sort Introduction | 6:12 | Board + description |  |
| 22 | QuickSort using Lomuto Partition | 13:31 | Transcript + board | Quick Sort |
| 23 | QuickSort using Hoare Partition | 10:49 | Transcript + board |  |
| 24 | QuickSort analysis | 17:48 | Transcript + board | QuickSort analysis |
| 25 | Space Analysis of QuickSort | 8:11 | Transcript + board |  |
| 26 | Choice of pivot and worst case of quick sort | 5:27 | Transcript + board |  |
| 27 | Tail call elimination in QuickSort | 2:47 | Transcript + board | Tail call elimination in Quick Sort |
| 28 | Kth Smallest Element | 9:07 | Transcript + board | Kth Smallest Element |
| 29 | Minimum Difference in an Array | 6:41 | Transcript + board | Minimum Difference in an Array |
| 30 | Chocolate Distribution Problem | 8:30 | Board + description |  |
| 31 | Sort an Array with two types of elements | 8:54 | Transcript + board | Sort an Array with two types of elements |
| 32 | Sort an array with three types of elements | 11:35 | Transcript + board | Sort an array with three types of elements |
| 33 | Merge overlapping intervals | 25:16 | Transcript + board |  |
| 34 | Meeting the maximum guests | 10:40 | Transcript + board | Meeting the maximum guests |
| 35 | Cycle Sort | 18:05 | Transcript + board | Cycle Sort |
| 36 | Heap Sort | 12:53 | Transcript + board | Heap Sort |
| 37 | Counting Sort | 19:31 | Transcript + board | Counting Sort |
| 38 | Radix Sort | 15:25 | Transcript + board | Radix Sort |
| 39 | Bucket Sort | 17:12 | Transcript + board | Bucket Sort |

Every Sorting article matches a video, so the Track practice set lists only the 20 problems. V12, V15, V21 and V30 have no Transcript button and were done from frames and the description; no transcript was cut off early. V28's auto-generated transcript is badly garbled, so its notes follow the board. Course progress was unchanged (14/39 videos watched, 33%, no article marked as read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 39 Sorting videos.

### Track 8: Matrix, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Multidimensional array in CPP | 14:07 | Transcript + board | Introduction to Matrix; 2D Vector in C++ |
| 2 | Passing 2D arrays as arguments in CPP | 11:09 | Transcript + board |  |
| 3 | Multidimensional array in Java | 7:41 | Transcript + board | Implementing Matrix using 2D Arrays in Java |
| 4 | Passing 2D arrays as arguments in Java | 2:38 | Transcript + board |  |
| 5 | Matrix in Snake Pattern | 3:29 | Transcript + board |  |
| 6 | Matrix Boundary Traversal | 5:24 | Transcript + board |  |
| 7 | Transpose of a Matrix | 6:13 | Transcript + board | Transpose of a Matrix |
| 8 | Rotate Matrix Anti-clockwise by 90 | 8:03 | Transcript + board | Matrix Rotation |
| 9 | Spiral Traversal of Matrix | 10:08 | Transcript + board | Spiral Traversal of Matrix |
| 10 | Search in Row-wise and Column-wise sorted matrix | 11:53 | Transcript + board | Search in Row-wise and Column-wise sorted matrix |
| 11 | Median of a Row Wise Sorted Matrix | 13:27 | Board + description | Median of a Row Wise Sorted Matrix |
| 12 | Median of a Row Wise Sorted Matrix Java | 13:22 | Board + description |  |

"Matrix Operations (Addition, Subtraction, Multiplication)", "Sample Problems on Matrix" and "Determinant of a Matrix | Explanation" match no video, so they're in the Track practice set with the 15 problems. V11 and V12 have no Transcript button and were done from frames and the description; no transcript was cut off early. V6's transcript is heavily garbled, so its notes follow the board. The track page shows 0% and no watched count; it was unchanged, no article was marked as read, and all resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 12 Matrix videos.

### Track 9: Hashing, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Introduction to Hashing | 6:47 | Transcript + board | Introduction to Hashing |
| 2 | Hashing Application | 5:13 | Transcript + board | Hashing Application |
| 3 | Direct Address Table | 7:37 | Transcript + board | Direct Address Table |
| 4 | Hashing Functions | 15:36 | Transcript + board | Hashing Functions |
| 5 | Collision Handling | 4:15 | Transcript + board | Collision Handling |
| 6 | Chaining | 12:30 | Transcript + board |  |
| 7 | Implementation of Chaining | 7:18 | Board + description | Implementation of Chaining |
| 8 | Open Addressing | 22:23 | Transcript + board | Open Addressing |
| 9 | Double Hashing | 17:18 | Transcript + board | Double Hashing |
| 10 | Implementation of Open Addressing | 16:28 | Transcript + board | Implementation of Open Addressing |
| 11 | Chaining vs Open Addressing | 6:09 | Transcript + board | Chaining vs Open Addressing |
| 12 | Unordered_set in C++ STL | 11:37 | Board + description | unordered_set in C++ STL |
| 13 | Unordered_map in C++ STL | 14:16 | Board + description | unordered_map in C++ STL |
| 14 | HashSet in Java | 7:15 | Transcript + board | HashSet in Java |
| 15 | HashMap in Java | 7:19 | Transcript + board | HashMap in Java |
| 16 | Count Distinct Elements | 7:13 | Board + description | Count Distinct Elements |
| 17 | Frequencies of array elements | 11:18 | Transcript + board | Frequencies of array elements |
| 18 | Intersection of two unsorted arrays | 8:22 | Transcript + board |  |
| 19 | Union of two unsorted arrays | 8:23 | Transcript + board |  |
| 20 | Pair with given sum in unsorted array | 7:52 | Transcript + board |  |
| 21 | Subarray with zero sum | 9:12 | Board + description | Subarray with Zero Sum |
| 22 | Subarray with given Sum | 9:26 | Transcript + board | Subarray with given Sum |
| 23 | Longest subarray with given sum | 16:42 | Transcript + board |  |
| 24 | Longest subarray with equal number of 0's and 1's | 6:51 | Transcript + board | Longest Subarray with equal number of 0s and 1s |
| 25 | Longest common span with same sum in binary arrays | 7:56 | Transcript + board |  |
| 26 | Longest Consecutive Subsequence | 16:00 | Transcript + board | Longest Consecutive Subsequence |
| 27 | Count Distinct Elements In Every Window | 10:57 | Transcript + board | Count Distinct Elements In Every Window |
| 28 | More than n/k Occurences | 8:43 | Board + description |  |
| 29 | More than n/k Occurences (O(nk) solution) | 10:59 | Board + description |  |

"Hashing in C++ using STL" and "Implementing Hashing in Java" match no video, so they're in the Track practice set with the 22 problems. V7, V12, V13, V16, V21, V28 and V29 have no Transcript button and were done from frames and the description (V29's description is only the title and code links); no transcript was cut off early. Course progress was unchanged (6/29 videos watched, 15%, 0/23 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 29 Hashing videos.

### Track 10: Strings, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Introduction to String | 14:18 | Transcript + board | Introduction to Strings |
| 2 | Strings in C++ | 18:08 | Board + description | Strings in C++ |
| 3 | String in Java | 15:16 | Transcript + board | Strings in Java |
| 4 | Palindrome Check | 9:17 | Transcript + board | Check for Palindrome in Cpp; Check for Palindrome in Java |
| 5 | Check if a String is Subsequence of Other | 13:25 | Transcript + board |  |
| 6 | Check for Anagram | 7:25 | Transcript + board | Check for Anagram |
| 7 | Leftmost Repeating Character | 12:46 | Transcript + board |  |
| 8 | Leftmost Non-repeating Element | 9:56 | Transcript + board |  |
| 9 | Reverse words in a string | 14:45 | Transcript + board | Reverse words in a given string |
| 10 | Overview of Pattern Searching | 7:13 | Transcript + board |  |
| 11 | Naive Pattern Searching | 7:56 | Transcript + board | Naive Pattern Searching Algorithm |
| 12 | Improved Naive Pattern Searching for Distinct | 11:40 | Transcript + board |  |
| 13 | Rabin Karp Algorithm | 22:28 | Transcript + board | Rabin-Karp Algorithm for Pattern Searching |
| 14 | KMP Algorithm (Part 1 : Constructing LPS Array) | 25:00 | Transcript + board |  |
| 15 | KMP Algorithm (Part 2 : Complete Algorithm) | 21:30 | Transcript + board | KMP Algorithm for Pattern Searching |
| 16 | Check if Strings are Rotations | 7:17 | Transcript + board | Check if Strings are Rotations |
| 17 | Anagram Search | 11:17 | Transcript + board |  |
| 18 | Lexicographic Rank of a String | 19:10 | Transcript + board |  |
| 19 | Longest Substring with Distinct Characters | 17:58 | Transcript + board | Longest Substring with Distinct Characters |

Every Strings article matches a video, so the Track practice set lists only the 26 problems. V2 has no Transcript button and was done from frames and the description; no transcript was cut off early. Course progress was unchanged (8/19 videos watched, 20%, no article marked as read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 19 Strings videos.

### Track 11: Linked List, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Problems With Array Data Structures | 17:30 | Transcript + board |  |
| 2 | Introduction to Linked List | 3:23 | Transcript + board | Linked List \| Introduction |
| 3 | Simple Linked List Implementation in C++ | 8:43 | Transcript + board |  |
| 4 | Simple Linked List Implementation in Java | 6:11 | Board + description |  |
| 5 | Applications of Linked List | 6:39 | Board + description |  |
| 6 | Traversing a Linked List in C++ | 6:49 | Transcript + board |  |
| 7 | Traversing a Linked List in Java | 5:08 | Board + description |  |
| 8 | Recursive Traversal of Singly Linked List | 4:19 | Board + description | Recursive Traversal of Singly Linked List |
| 9 | Insert at Begin of Singly Linked List | 6:02 | Board + description | Insertion in Singly Linked Lists; Insert at Begin of Singly Linked List |
| 10 | Insert at the end of Singly Linked List | 5:14 | Transcript + board | Insert at the end of Singly Linked List |
| 11 | Insert at given position in Singly Linked List | 7:36 | Board + description | Insert at given position in Singly Linked List |
| 12 | Delete First Node of Singly Linked List | 3:22 | Transcript + board | Delete First Node of Singly Linked List |
| 13 | Delete Last Node of Singly Linked List | 5:52 | Transcript + board | Delete Last Node of Singly Linked List |
| 14 | Search in a Linked List (Iterative and Recursive) | 11:09 | Board + description | Search in a Linked List (Iterative and Recursive) |
| 15 | Doubly Linked List in C++ | 2:49 | Board + description | Doubly Linked List |
| 16 | Doubly Linked List in Java | 2:57 | Board + description |  |
| 17 | Singly Vs Doubly Linked List (Advantages + Disadvantages) | 6:01 | Transcript + board |  |
| 18 | Insert at Begin of Doubly Linked List | 4:00 | Transcript + board | Insertion in a Doubly Linked List |
| 19 | Insert at End Doubly Linked List | 5:54 | Transcript + board |  |
| 20 | Reverse a Doubly Linked List | 8:00 | Transcript + board | Reverse a Doubly Linked List |
| 21 | Delete Head of a Doubly Linked List | 3:51 | Transcript + board | Delete Head of a Doubly Linked List |
| 22 | Delete Last of a Doubly Linked List | 6:13 | Transcript + board |  |
| 23 | Circular Linked List in C++ | 2:44 | Board + description | Circular Linked in C++ |
| 24 | Circular Linked List in Java | 2:43 | Board + description |  |
| 25 | Circular Linked List (Advantages + Disadvantages) | 4:25 | Board + description | Circular Linked List (Advantages & Disadvantages) |
| 26 | Circular Linked List Traversal in C++ | 5:59 | Transcript + board | Circular Linked List Traversal |
| 27 | Circular Linked List Traversal in Java | 7:45 | Transcript + board |  |
| 28 | Insert at Begin of Circular Linked List | 10:17 | Transcript + board | Insert at Begin of Circular Linked List |
| 29 | Insert at the end of Circular Linked List | 8:32 | Transcript + board | Insert at the end of Circular Linked List |
| 30 | Delete Head of Circular Linked List | 5:42 | Transcript + board | Delete Head of Circular Linked List |
| 31 | Delete Kth of a Circular Linked List | 7:14 | Board + description |  |
| 32 | Circular Doubly Linked List | 7:28 | Transcript + board | Circular Doubly Linked List |
| 33 | Sorted Insert in a Singly Linked List | 10:35 | Transcript + board | Sorted Insert in a Singly Linked List |
| 34 | Middle of linked list | 6:55 | Transcript + board | Middle of linked list |
| 35 | Nth Node from end of Linked List | 9:01 | Board + description | Nth Node from end of Linked List |
| 36 | Reverse a linked list iterative | 10:02 | Transcript + board | Reverse a linked list iterative |
| 37 | Recursive reverse a linked list (Part 1) | 7:09 | Transcript + board |  |
| 38 | Recursive reverse a linked list (Part 2) | 7:02 | Transcript + board |  |
| 39 | Remove duplicates from a sorted Singly Linked List | 10:00 | Partial transcript + board | Remove duplicates from a sorted Singly Linked List |
| 40 | Reverse a linked list in groups of size k | 13:03 | Transcript + board | Reverse a linked list in groups of size k |
| 41 | Detect loop | 14:08 | Transcript + board | Detect loop |
| 42 | Detect loop using floyd cycle detection | 13:37 | Transcript + board | Detect loop using floyd cycle detection |
| 43 | Detect and remove loop in linked list | 18:13 | Transcript + board | Detect and remove loop in linked list |
| 44 | Delete node with only pointer given to it | 4:34 | Transcript + board | Delete node with only pointer given to it |
| 45 | Segregate Even and Odd Nodes in C++ | 9:10 | Board + description | Segregate Even and Odd Nodes |
| 46 | Segregate Even and Odd Nodes in Java | 9:50 | Board + description |  |
| 47 | Intersection Point of two linked list | 8:02 | Transcript + board | Intersection of two linked list |
| 48 | Pairwise Swap Nodes of linked list in C++ | 11:41 | Transcript + board | Pairwise Swap Nodes of linked list |
| 49 | Pairwise Swap Nodes of linked list in Java | 11:51 | Transcript + board |  |
| 50 | Clone a linked list with Random Pointer in C++ | 13:38 | Transcript + board | Clone a linked list with Random Pointer |
| 51 | Clone a linked list with Random Pointer in Java | 13:51 | Transcript + board |  |
| 52 | LRU Cache Design | 13:24 | Transcript + board | LRU Cache Design |
| 53 | Merge two sorted linked lists | 15:03 | Transcript + board | Merge two sorted linked lists |
| 54 | Palindrome Linked List | 10:18 | Board + description | Palindrome Linked List |

"Sample Problems on Linked List", "XOR Linked Lists" and "Circular Linked Lists" match no video, so they're in the Track practice set with the 25 problems. V4, V5, V7, V8, V9, V11, V14, V15, V16, V23, V24, V25, V31, V35, V45, V46 and V54 have no Transcript button and were done from frames and the description. V39's transcript stops at 7:00 of 10:00; the rest is from frames. Course progress was unchanged (4/54 videos watched, 17%, 0/40 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 54 Linked List videos.

### Track 12: Stack, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Stack Data Structure | 6:50 | Board + description | Stack Data Structure |
| 2 | Array Implementation of Stack in C++ | 12:48 | Board + description | Array Implementation of Stack |
| 3 | Array Implementation of Stack in Java | 12:52 | Board + description |  |
| 4 | Linked List Implementation of Stack in C++ | 8:38 | Board + description | Linked List implementation of Stack |
| 5 | Linked List Implementation of Stack in Java | 7:47 | Board + description |  |
| 6 | Applications of Stack | 9:00 | Transcript + board | Applications of Stack |
| 7 | Stack in C++ STL | 6:06 | Transcript + board | Stack in C++ STL |
| 8 | Stack in Java Collections | 5:16 | Board + description | Stack in Java Collection |
| 9 | Balanced Parenthesis | 12:43 | Board + description | Balanced Parenthesis |
| 10 | Implement two Stacks in an Array | 12:32 | Transcript + board | Implement two Stacks in an Array |
| 11 | Implement K Stacks in an Array in C++ | 9:50 | Transcript + board | Implement K Stacks in an Array |
| 12 | Implement K Stacks in an Array in Java | 9:35 | Transcript + board |  |
| 13 | Stock span problem | 26:41 | Board + description | Stock span problem |
| 14 | Previous Greater Element | 8:02 | Transcript + board | Previous Greater Element |
| 15 | Next Greater Element | 14:49 | Transcript + board | Next Greater Element |
| 16 | Largest Rectangular Area in a Histogram (Part 1) | 12:39 | Transcript + board |  |
| 17 | Largest Rectangular Area in a Histogram (Part 2) | 9:11 | Transcript + board | Largest Rectangular Area in a Histogram |
| 18 | Largest Rectangle with all 1's | 13:09 | Transcript + board | Largest Rectangle with all 1's |
| 19 | Stack with getMin() in O(1) | 9:05 | Transcript + board |  |
| 20 | Design a Stack with getMin() in O(1) Space | 16:25 | Board + description | Stack with getMin() in O(1) |
| 21 | Infix, Prefix and Postfix Introduction | 9:54 | Transcript + board |  |
| 22 | Infix to Postfix (Simple sol.) | 9:35 | Transcript + board |  |
| 23 | Infix to Postfix (Efficient Solution) | 12:32 | Transcript + board | Infix to Postfix |
| 24 | Evaluation of Postfix | 10:24 | Transcript + board | Evaluation of Postfix |
| 25 | Infix to Prefix (Simple Solution) | 9:00 | Transcript + board |  |
| 26 | Infix to Prefix (Efficient Solution) | 15:47 | Transcript + board | Infix To Prefix |
| 27 | Evaluation of Prefix | 6:51 | Transcript + board | Evaluation of Prefix |

Every Stack article matches a video, so the Track practice set lists only the 17 problems. V1, V2, V3, V4, V5, V8, V9, V13 and V20 have no Transcript button and were done from frames and the description; no transcript was cut off early. Course progress was unchanged (1/27 videos watched, 10%, 0/19 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 27 Stack videos.

### Track 13: Queue, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Queue Data Structure | 3:59 | Transcript + board | Introduction to Queues |
| 2 | Application of Queue Data structure | 6:43 | Transcript + board |  |
| 3 | Implementation of Queue using Array | 15:31 | Board + description |  |
| 4 | Implementation of Queue using Linked List | 11:40 | Board + description |  |
| 5 | Queue in C++ STL | 6:50 | Transcript + board | Implementing Queue in C++ and Java using Built-in Classes |
| 6 | Queue in Java | 12:09 | Transcript + board |  |
| 7 | Implementing stack using queue | 6:47 | Transcript + board | Implementing Stack using Queue |
| 8 | Reversing a Queue | 7:02 | Board + description |  |
| 9 | Generate numbers with given digits | 6:30 | Transcript + board |  |

"Implementing Queue using Stack" and "Sample Problems on Queue" match no video, so they're in the Track practice set with the 9 problems. V3, V4 and V8 have no Transcript button and were done from frames and the description; no transcript was cut off early. Course progress was unchanged (0/9 videos watched, 22%, 0/5 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 9 Queue videos.

### Track 14: Deque, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Deque Data Structure | 9:06 | Transcript + board | Deque Data Structure |
| 2 | Array Implementation of Deque | 17:19 | Transcript + board | Circular implementation of Deque |
| 3 | Deque in C++ STL | 13:43 | Transcript + board | Deque in C++ STL |
| 4 | Deque in Java | 8:04 | Transcript + board | Deque in Java |
| 5 | ArrayDeque in Java | 20:45 | Transcript + board |  |
| 6 | Design a Data Structure with Min and Max operations | 5:12 | Transcript + board | Design a Data Structure with Min and Max operations |
| 7 | Maximums of all subarrays of size k | 20:26 | Transcript + board | Maximums of all subarrays of size K |
| 8 | First Circular Tour | 27:52 | Transcript + board | First Circular Tour |

Every Deque article matches a video, so the Track practice set lists only the 6 problems. Every Deque video has a full transcript; none was cut off early. Course progress was unchanged (0%; the track shows no Watched or Read counter, and the articles still show "Mark as Read"). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 8 Deque videos.

### Track 15: Tree, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Tree Data Structure | 4:26 | Transcript + board | Introduction to Trees |
| 2 | Application of Tree | 4:44 | Transcript + board | Application of Tree |
| 3 | Binary Tree | 6:29 | Transcript + board | Binary Tree |
| 4 | Tree Traversal | 9:05 | Transcript + board | Binary Tree Traversals |
| 5 | Implementation of Inorder Traversal | 8:24 | Transcript + board | Implementation of Inorder, Preorder and Postorder Traversal |
| 6 | Implementation of Preorder Traversal | 5:26 | Transcript + board |  |
| 7 | Implementation of Postorder Traversal | 4:25 | Transcript + board |  |
| 8 | Height of Binary Tree | 7:40 | Transcript + board | Height of Binary Tree |
| 9 | Print Nodes at K distance | 6:22 | Transcript + board | Print Nodes at K Distance |
| 10 | Level Order Traversal | 10:27 | Board + description | Level Order Traversal of a Binary Tree |
| 11 | Level Order Traversal Line by Line (Part 1) | 6:09 | Transcript + board |  |
| 12 | Level Order Traversal Line by Line (Part 2) | 3:45 | Transcript + board |  |
| 13 | Size of Binary Tree | 12:17 | Transcript + board | Size of Binary Tree |
| 14 | Maximum in Binary Tree | 8:57 | Transcript + board | Maximum in Binary Tree |
| 15 | Print Left View of Binary Tree | 9:34 | Transcript + board | Left, Right, Top and Bottom View of a Binary Tree |
| 16 | Children Sum Property | 6:27 | Transcript + board |  |
| 17 | Check for Balanced Binary Tree | 11:39 | Transcript + board | Check for Balanced Binary Tree |
| 18 | Maximum Width of Binary Tree | 4:59 | Transcript + board | Maximum width of Binary Tree |
| 19 | Convert Binary Tree to Doubly Linked List | 15:23 | Transcript + board |  |
| 20 | Construct Binary Tree from Inorder and Preorder | 20:10 | Transcript + board | Construct Binary Tree from Inorder and Preorder |
| 21 | Tree Traversal in Spiral Form | 21:41 | Transcript + board | Tree Traversal in Spiral Form |
| 22 | Diameter of a Binary Tree | 15:26 | Transcript + board | Diameter of a Binary Tree |
| 23 | LCA of Binary Tree (Part 1) | 12:57 | Transcript + board | Finding LCA in Binary Tree |
| 24 | LCA of Binary Tree (Part 2) | 10:52 | Transcript + board |  |
| 25 | Burn a Binary Tree from a Leaf | 16:44 | Transcript + board | Burn a Binary Tree From a Leaf |
| 26 | Count nodes in a Complete Binary Tree | 18:28 | Transcript + board |  |
| 27 | Serialize and Deserialize a Binary Tree | 19:16 | Transcript + board | Serialize and Deserialize a Binary Tree |
| 28 | Iterative Inorder Traversal | 10:15 | Transcript + board |  |
| 29 | Iterative Preorder Traversal (Simple) | 6:52 | Transcript + board | Iterative Preorder Traversal |
| 30 | Iterative Preorder Traversal (Space Optimized) | 9:53 | Transcript + board |  |

"Insertion in a Binary Tree", "Deletion in a Binary Tree", "Threaded Binary Tree" and "Sample Problems on Trees" match no video, so they're in the Track practice set with the 32 problems. "Finding LCA in Binary Tree" (both methods) is folded into V23, and "Iterative Preorder Traversal" (both solutions) into V29. V10 has no Transcript button and was done from frames and the description; no transcript was cut off early. Course progress was unchanged (23/30 videos watched, 52%, 0/24 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 30 Tree videos.

### Track 16: Binary Search Tree, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Binary Search Tree(Background) | 6:40 | Transcript + board |  |
| 2 | Binary Search Tree(Introduction) | 8:20 | Transcript + board | Introduction to Binary Search Trees |
| 3 | Search in BST (Introduction) | 3:49 | Transcript + board |  |
| 4 | Search in BST C++ | 7:37 | Transcript + board | Binary Search Tree (Search and Insert) |
| 5 | Search in BST Java | 7:07 | Transcript + board |  |
| 6 | Insert in BST | 3:31 | Transcript + board |  |
| 7 | Insert in BST C++ | 7:19 | Transcript + board |  |
| 8 | Insert in BST Java | 7:28 | Transcript + board |  |
| 9 | Deletion in BST | 5:02 | Transcript + board | Deletion in a Binary Search Tree |
| 10 | BST deletion in C++ | 8:19 | Transcript + board |  |
| 11 | BST Deletion in Java | 8:01 | Transcript + board |  |
| 12 | Floor in BST | 7:36 | Transcript + board | Floor in BST |
| 13 | Floor in BST in CPP | 4:08 | Board + description |  |
| 14 | Floor in BST Java | 3:31 | Transcript + board |  |
| 15 | Ceil in BST | 7:42 | Transcript + board | Ceil in BST |
| 16 | Self Balancing BST | 9:55 | Transcript + board | Self Balancing BST |
| 17 | AVL Tree | 13:09 | Board + description | Introduction to AVL Tree |
| 18 | Red Black Tree | 7:24 | Transcript + board | Red Black Tree |
| 19 | Applications of BST | 5:43 | Transcript + board | Applications of BST |
| 20 | Ceiling on left side in an array | 7:09 | Transcript + board |  |
| 21 | Find Kth Smallest in BST | 12:32 | Transcript + board | Find Kth Smallest in BST |
| 22 | Check for BST | 14:52 | Transcript + board | Check for BST |
| 23 | Fix BST with Two Nodes Swapped | 11:39 | Board + description | Fix BST with two nodes swapped |
| 24 | Pair Sum with given BST | 10:01 | Transcript + board | Pair Sum with given BST |
| 25 | Vertical Sum in a Binary Tree | 14:02 | Transcript + board | Vertical Sum in a Binary Tree |
| 26 | Vertical Traversal of Binary Tree | 16:09 | Transcript + board |  |
| 27 | Top View of Binary Tree | 13:28 | Transcript + board | Top View of Binary Tree |
| 28 | Bottom View of Binary Tree | 13:48 | Transcript + board |  |

"Finding LCA in Binary Search Tree" matches no video, so it's in the Track practice set with the 23 problems. V13, V17 and V23 have no Transcript button and were done from frames and the description; no transcript was cut off early. Course progress was unchanged (12/28 videos watched, 35%, 0/16 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 28 BST videos.

### Track 17: Heap, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Binary Heap Introduction | 9:12 | Transcript + board | Binary Heap Introduction |
| 2 | Binary Heap Implementation | 1:39 | Transcript + board |  |
| 3 | Binary Heap Insert | 6:38 | Transcript + board |  |
| 4 | Binary Heap (Heapify and Extract) | 18:23 | Transcript + board | Insertion and Deletion in Heap |
| 5 | Binary Heap (Decrease Key, Delete and Build Heap) | 15:22 | Board + description | Operations of Heap Data Structure |
| 6 | Heap Sort | 12:53 | Transcript + board | Heap Sort |
| 7 | Priority Queue in C++ | 16:20 | Transcript + board | Implementing Heaps using inbuilt classes in C++ and Java |
| 8 | PriorityQueue in Java | 2:29 | Board + description |  |
| 9 | Sort K-Sorted Array | 7:35 | Transcript + board | Sort K-Sorted Array |
| 10 | Buy Maximum Items with Given Sum | 5:21 | Transcript + board | Buy Maximum Items with Given Sum |
| 11 | K Largest Elements | 8:48 | Transcript + board | K Largest Elements |
| 12 | K Closest Elements | 12:17 | Board + description | K Closest Elements |
| 13 | Merge K Sorted Arrays | 20:36 | Transcript + board | Merge K Sorted Arrays |
| 14 | Median of a Stream | 20:36 | Transcript + board | Median of a Stream |

Every Heap article matches a video, so the Track practice set lists only the 11 problems. V5, V8 and V12 have no Transcript button and were done from frames and the description; no transcript was cut off early. Course progress was unchanged (10/14 videos watched, 40%, 0/11 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 14 Heap videos.

### Track 18: Graph, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Introduction to Graph | 8:53 | Transcript + board | Introduction to Graphs |
| 2 | Graph Representation (Adjacency Matrix) | 7:17 | Transcript + board | Graph Representation |
| 3 | Graph Representation (Adjacency List) | 7:06 | Transcript + board |  |
| 4 | Adjacency List implementation in CPP | 4:35 | Transcript + board |  |
| 5 | Adjacency List implementation in Java | 5:44 | Transcript + board |  |
| 6 | Adjacency Matrix and List Comparison | 6:15 | Transcript + board | Adjacency Matrix and List Comparison |
| 7 | Breadth First Search | 20:16 | Transcript + board | Breadth First Traversal of a Graph |
| 8 | Applications of BFS | 3:30 | Transcript + board | Applications of BFS |
| 9 | Depth First Search | 20:07 | Transcript + board | Depth First Traversal of a Graph |
| 10 | Applications of DFS | 5:25 | Transcript + board | Applications, Advantages and Disadvantages of DFS |
| 11 | Shortest Path in an Unweighted Graph | 6:56 | Transcript + board | Shortest path in an Unweighted graph |
| 12 | Detect Cycle in Undirected Graph | 7:14 | Transcript + board | Detect cycle in Undirected graph |
| 13 | Detect Cycle in a Directed Graph (Part 1) | 10:14 | Transcript + board | Detect Cycle in a Directed Graph |
| 14 | Topological Sorting (Kahn's BFS Based Algortihm) | 12:32 | Transcript + board | Topological Sorting (Kahn's BFS Based Algortihm) |
| 15 | Detect Cycle in a Directed Graph (Part 2) | 4:36 | Transcript + board | Detect Cycle in a Directed Graph (Part 2) |
| 16 | Topological Sorting (DFS Based Algorithm) | 9:06 | Transcript + board |  |
| 17 | Shortest Path in DAG | 9:42 | Transcript + board |  |
| 18 | Prim's Algorithm/Minimum Spanning Tree | 9:26 | Transcript + board | Prim's Minimum Spanning Tree Algorithm |
| 19 | Implementation of Prim's Algorithm C++ | 16:52 | Board + description |  |
| 20 | Implementation of Prim's Algorithm Java | 17:11 | Transcript + board |  |
| 21 | Dijkstra's Shortest Path Algorithm | 19:02 | Transcript + board | Dijkstra's Algorithm for Shortest Path in a Weighted Graph |
| 22 | Implementation of Dijkstra's Algorithm C++ | 11:03 | Board + description |  |
| 23 | Implementation of Dijkstra's Algorithm Java | 10:06 | Board + description |  |
| 24 | Kosaraju's Algorithm Part 1 | 13:43 | Transcript + board | Kosaraju's Algorithm / Strongly Connected Components |
| 25 | Kosaraju's Algorithm Part 2 | 11:02 | Board + description |  |
| 26 | Bellman Ford Shortest Path Algorithm | 12:51 | Transcript + board | Bellman-Ford Algorithm for Shortest Path |
| 27 | Articulation Point | 22:33 | Board + description | Articulation Points (or Cut Vertices) in a Graph |
| 28 | Bridges in Graph | 10:34 | Transcript + board | Bridges in a Graph |
| 29 | Tarjans Algorithm | 14:24 | Transcript + board |  |
| 30 | Kruskal's Algorithm | 24:04 | Transcript + board |  |

"Number of Strongly Connected Components in an Undirected Graph" and "Sample Problems on Graphs" match no video, so they're in the Track practice set with the 24 problems. V19, V22, V23, V25 and V27 have no Transcript button and were done from frames and the description; no transcript was cut off early. Course progress was unchanged (26/30 videos watched, 36%, 0/20 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 30 Graph videos.

### Track 19: Greedy, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Introduction to Greedy Algorithms | 12:07 | Transcript + board | Introduction to Greedy Algorithms |
| 2 | Activity Selection Problem | 8:25 | Transcript + board | Activity Selection Problem |
| 3 | Activity Selection Solution in C++ | 3:58 | Transcript + board |  |
| 4 | Activity Selection Solution in Java | 5:20 | Board + description |  |
| 5 | Fractional Knapsack Problem | 7:48 | Transcript + board | Fractional Knapsack Problem |
| 6 | Fractional Knapsack in C++ | 5:42 | Transcript + board |  |
| 7 | Fractional Knapsack in Java | 9:48 | Board + description |  |
| 8 | Job Sequencing Problem | 12:23 | Transcript + board | Job Sequencing Problem \| Greedy Approach |
| 9 | Huffman Coding (introduction) | 8:56 | Transcript + board |  |
| 10 | Huffman Algorithms | 14:25 | Board + description | Huffman Coding |
| 11 | CPP Implementation of Huffman coding | 9:01 | Transcript + board |  |
| 12 | Java Implementation of Huffman coding | 10:40 | Transcript + board |  |

All 5 articles match a video; the Track practice set lists the 6 problems. V4, V7 and V10 have no Transcript button and were done from frames and the description; no transcript was cut off early. Course progress was unchanged (0%, 0/5 articles read). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 12 Greedy videos.

### Track 20: Backtracking, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Concepts of Backtracking | 10:27 | Transcript + board | Concept of Backtracking |
| 2 | Rat In a Maze | 10:27 | Transcript + board | Rat in a Maze |
| 3 | N Queen Problem | 20:06 | Transcript + board | N-Queen Problem |
| 4 | Sudoku Problem | 14:06 | Board + description | Sudoku Problem |

All 4 articles match a video; the Track practice set lists the 7 problems. V4 has no Transcript button and was done from frames and the description. Course progress was unchanged (0%). All resume positions were 0:00 and were restored. The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 4 Backtracking videos.

### Track 21: Dynamic Programming, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Introduction to DP | 4:46 | Transcript + board | Introduction to Dynamic Programming; Properties of a DP Problem; Optimal Substructure Property |
| 2 | Dynamic Programming Memoization | 15:30 | Transcript + board | Overlapping Subproblems Property |
| 3 | Dynamic Programming Tabulation | 8:09 | Transcript + board | Tabulation vs Memoization |
| 4 | Longest Common Subsequence (Part 1) | 24:24 | Transcript + board | Longest Common Subsequence (Part 1) |
| 5 | Longest Common Subsequence (Part 2) | 9:07 | Transcript + board | Longest Common Subsequence (Part 2) |
| 6 | Variation of LCS | 13:45 | Transcript + board |  |
| 7 | Coin Change (Naive Recursive Solution) | 9:56 | Transcript + board |  |
| 8 | Coin Change (DP Solution) | 9:26 | Transcript + board | Coin Change |
| 9 | Edit Distance Problem | 14:59 | Transcript + board |  |
| 10 | Edit Distance Problem DP solution | 11:15 | Transcript + board | Edit Distance Problem |
| 11 | Longest Increasing Subsequence Problem | 22:16 | Transcript + board | Longest Increasing Subsequence |
| 12 | Longest Increasing Subsequence in O(nlogn) | 15:34 | Transcript + board | Longest Increasing Subsequence in O(nlogn) |
| 13 | Variation of LIS (Part 1) | 13:16 | Transcript + board |  |
| 14 | Variations of LIS (Part 2) | 11:50 | Transcript + board |  |
| 15 | Maximum Cuts | 10:22 | Transcript + board | Maximum Cuts |
| 16 | Minimum coins to make a value | 21:50 | Transcript + board | Minimum coins to make a value |
| 17 | Minimum Jumps to reach at end | 17:12 | Transcript + board | Minimum Jumps to reach at end |
| 18 | 0-1 knapsack problem | 14:32 | Transcript + board |  |
| 19 | 0-1 knapsack problem DP Solution | 13:43 | Transcript + board | 0-1 knapsack problem |
| 20 | Optimal Strategy for a Game | 27:09 | Transcript + board | Optimal Strategy for a Game |
| 21 | Egg Dropping Puzzle - Part 1 | 13:09 | Transcript + board |  |
| 22 | Egg Dropping Puzzle - Part 2 | 9:40 | Transcript + board | Egg Dropping Puzzle |
| 23 | Count BSTs with n keys | 13:40 | Board + description | Count BSTs with n keys |
| 24 | Maximum sum with no two consecutive | 13:36 | Board + description | Maximum sum with no two consecutive |
| 25 | Subset Sum Problem (Recursive Solution) (Medium) | 10:53 | Transcript + board |  |
| 26 | Subset Sum Problem (DP Solution) (Medium) | 10:55 | Transcript + board | Subset Sum Problem |
| 27 | Matrix Chain Multiplication | 16:06 | Board + description |  |
| 28 | Matrix Chain Multiplication (DP Solution) (Hard) | 10:42 | Board + description | Matrix Chain Multiplication |
| 29 | Palindrome Partitioning | 15:52 | Board + description | Palindrome Partitioning |
| 30 | Allocate Minimum Pages (Naive Method) | 8:54 | Board + description |  |
| 31 | Allocate Minimum Pages (DP Solution) (Hard) | 10:18 | Board + description | Allocate Minimum Pages |

"Solving a Dynamic Programming Problem" and "Sample Problems on Dynamic Programming" match no video, so they're in the Track practice set with the 28 problems. V23, V24, V27, V28, V29, V30, V31 have no Transcript button and were done from frames and the description; no transcript was cut off early. Course progress was unchanged (40%, 21/31 videos watched). All resume positions were restored (V1 was at 0:03 and was put back there). The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 31 DP videos.

### Track 22: Trie, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Trie Data Structure (Introduction) | 4:30 | Transcript + board |  |
| 2 | Trie (Representation, Search and Insert) | 21:48 | Transcript + board | Trie (Insert and Search) |
| 3 | Trie Delete | 11:11 | Board + description | Deletion in a Trie |
| 4 | Count Distinct Rows in a Binary Matrix | 7:37 | Transcript + board |  |

"Implementing Auto-Complete Feature using Trie" matches no video, so it's in the Track practice set with the 6 problems. V3 has no Transcript button and was done from frames and the description. Course progress was unchanged (0%). All resume positions were restored (V1 was at 0:03 and was put back there). The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 4 Trie videos.

### Track 23: Segment and Binary Indexed Trees, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Segment Tree (Introduction) | 22:07 | Transcript + board | Introduction to Segment Trees |
| 2 | Constructing Segment Tree | 10:11 | Transcript + board |  |
| 3 | Range Query on Segment Tree | 13:48 | Board + description |  |
| 4 | Update Query on Segment Tree | 10:03 | Transcript + board |  |
| 5 | Binary Indexed Tree (Intoduction) | 6:10 | Board + description | Binary Indexed Tree |
| 6 | Binary Indexed Tree (An Example Problem) | 6:00 | Transcript + board |  |
| 7 | Binary Indexed Tree (Prefix Sum) | 15:19 | Transcript + board |  |
| 8 | Binary Indexed Tree (Prefix Sum Implemention) | 11:34 | Board + description |  |
| 9 | Binary Indexed Tree (Update Operation) | 10:41 | Board + description |  |
| 10 | Binary Indexed Tree (Construction) | 6:11 | Transcript + board |  |

"Segment Tree | Range Minimum Query" matches no video, so it's in the Track practice set with the 6 problems. V3, V5, V8 and V9 have no Transcript button and were done from frames and the description. V10's transcript is auto-generated and garbled, so the notes lean on the board. Course progress was unchanged (0%). All resume positions were restored (V1 was at 0:02 and was put back there). The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists 10 videos.

### Track 24: Disjoint Set, per video

| # | Video | Duration | Source | Articles folded in |
|---|-------|---------:|--------|--------------------|
| 1 | Disjoint Set Introduction | 10:17 | Transcript + board |  |
| 2 | Find and Union Operations on Disjoint Sets | 8:11 | Transcript + board | Disjoint Set Data Structure \| Introduction |
| 3 | Union by Rank | 7:40 | Transcript + board | Union by Rank and Path Compression |
| 4 | Path Compression | 5:09 | Transcript + board |  |
| 5 | Kruskal's Algorithm | 24:04 | Same video as Graph V30 (notes repeated) | Kruskal's Minimum Spanning Tree Algorithm |

All 3 articles match a video; the Track practice set lists the 4 problems. V5 has the same video ID as Graph V30, so its notes are copied from there and re-linked to this track. Course progress was unchanged (6%, 1/5 videos watched). All resume positions were restored (V1 was at 0:07 and was put back there). The render check was done offline: every template's tags balance, the page script parses, and TRACKS lists all 470 videos across the 24 tracks.

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
- `10fb46a`: Add Searching track notes (18 videos, 13 articles, 18 problems)
- `c40a4e7`: Add Sorting track notes (39 videos, 29 articles, 20 problems)
- `671776d`: Add Matrix track notes (12 videos, 11 articles, 15 problems)
- `4d2a6f6`: Add Hashing track notes (29 videos, 23 articles, 22 problems)
- `5a47254`: Add Strings track notes (19 videos, 12 articles, 26 problems)
- `3251af2`: Add Linked List track notes (54 videos, 40 articles, 25 problems)
- `5e04a24`: Add Stack track notes (27 videos, 19 articles, 17 problems)
- `e80e175`: Add Queue track notes (9 videos, 5 articles, 9 problems)
- `6a5d4d9`: Add Deque track notes (8 videos, 7 articles, 6 problems)
- `684a13d`: Add Tree track notes (30 videos, 24 articles, 32 problems)
- `839335d`: Add Binary Search Tree track notes (28 videos, 16 articles, 23 problems)
- `cd1b6ea`: Add Heap track notes (14 videos, 11 articles, 11 problems)
- `92dabf7`: Add Graph track notes (30 videos, 20 articles, 24 problems)
- `ef72ced`: Add Greedy track notes (12 videos, 5 articles, 6 problems)
- `1000f12`: Add Backtracking track notes (4 videos, 4 articles, 7 problems)
- `dc87f65`: Add Dynamic Programming track notes (31 videos, 25 articles, 28 problems)
- `4198a96`: Add Trie track notes (4 videos, 3 articles, 6 problems)
- `a5d69c2`: Add Segment and Binary Indexed Trees track notes (10 videos, 3 articles, 6 problems)
- (this commit): Add Disjoint Set track notes (5 videos, 3 articles, 4 problems)

### What's next
- All 24 tracks are written and pushed to `claude/project-thread-8jxc30`.
- The private artifact link (https://claude.ai/artifact/XStbsSAnGcAdMa1AU9CBmL) has not been refreshed with tracks 2–24. The full 2.2 MB file is too large for Claude to read end-to-end before publishing, so meanwhile use `notes/dsa-notes.html` from the repo.

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
  - Completed track 7 (Sorting): 39 videos, 29 articles, 20 problems.
  - Completed track 8 (Matrix): 12 videos, 11 articles, 15 problems.
  - Pushed the branch to origin up to `671776d` (user's OK).
  - Completed track 9 (Hashing): 29 videos, 23 articles, 22 problems.
  - Completed track 10 (Strings): 19 videos, 12 articles, 26 problems.
  - Completed track 11 (Linked List): 54 videos, 40 articles, 25 problems.
  - Completed track 12 (Stack): 27 videos, 19 articles, 17 problems.
  - Completed track 13 (Queue): 9 videos, 5 articles, 9 problems.
  - Completed track 14 (Deque): 8 videos, 7 articles, 6 problems.
  - Completed track 15 (Tree): 30 videos, 24 articles, 32 problems.
  - Completed track 16 (Binary Search Tree): 28 videos, 16 articles, 23 problems.
  - Completed track 17 (Heap): 14 videos, 11 articles, 11 problems.
  - Completed track 18 (Graph): 30 videos, 20 articles, 24 problems.
  - Completed track 19 (Greedy): 12 videos, 5 articles, 6 problems.
  - Completed track 20 (Backtracking): 4 videos, 4 articles, 7 problems.
  - Completed track 21 (Dynamic Programming): 31 videos, 25 articles, 28 problems.
  - Completed track 22 (Trie): 4 videos, 3 articles, 6 problems.
  - Completed track 23 (Segment and Binary Indexed Trees): 10 videos, 3 articles, 6 problems.
  - Completed track 24 (Disjoint Set): 5 videos, 3 articles, 4 problems. All 24 tracks done.

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

### Disjoint Set: teacher slips flagged
- V2/V3 (board): the functions are named `union`, a C++ keyword (a real program needs another name).
- V4 (board): `paren[x] = find(parent[x])` (it's `parent[x]`).

### Segment and Binary Indexed Trees: teacher slips flagged
- V2: the board labels the root's range [3, 3] (it's [0, 3]); the transcript says the 30 is written "at index 0" (it's tree[1]).
- V4 (board): the right child is labelled [1, 3] (it's [2, 3]).
- V6 (board): the second example's output is first written "23 20" (it's 33 30).
- V3, V8, V9 (board): `&&`, `||` and `&` are drawn like "$$", "¦¦" and "$" or "8". Spoken slips couldn't be checked for V3, V5, V8 and V9 (no transcript).

### Trie: teacher slips flagged
- V2 (board): the Java TrieNode declares `bool isEnd` (Java's type is `boolean`); the Java search reads `key.charAt(index)` with loop variable `i`.
- V3 (board, Java): `root.isEnd == false;` is a comparison where an assignment is meant; the function is headed `delNode` but calls `delKey`; `bool isEmpty`. Spoken slips couldn't be checked (no transcript).

### Dynamic Programming: teacher slips flagged
- V6: the board writes "Superequence"; when printing the LCS, the teacher says the "upper and lower" neighbours (they're upper and left).
- V8: the board's column headers read 0 1 2 2 3; the transcript says the coin is usable when its value is "more than equal to J" (it's coins[i−1] ≤ j).
- V10: the mismatch case is first written without "1 +" (corrected on screen).
- V16 (board): the INT_MAX initialisation loop starts at i = 0 and overwrites dp[0] = 0 (it must start at 1).
- V18: the second example's answer is said as "hundred twenty" (it's 220); "there is a partial marking" is said while explaining that there's none; "theta of M" is said for Θ(n).
- V20: the dp[0][3] pick-j case uses 3 for arr[3] (it's 6; the max is still 25); "24 and 8" is said for 32 (20 + 4 + 8).
- V28 (board): `dp[j][k]` should be `dp[k][j]`.
- V29 (board): `isPal[i+1][j−1] || gap == 1` reads an unset cell when gap is 1 (gap == 1 should be checked first).
- Videos without a transcript (23, 24, 27, 28, 29, 30, 31): spoken slips couldn't be checked.

### Backtracking: teacher slips flagged
- V1 (board): `&&` is drawn like "88"; the naive cost is written "!n × n" for n! × n. The second isSafe condition is a typed overlay.
- V2 (board): `boolean maze[N][N], sol[N][N]` holds 1/0 values. The destination check comes before isSafe, so a blocked bottom-right cell still returns true.
- V3 (board): `boolean board[N][N]` holds 1/0 values; the loop header is written `i < N < i++`. The N = 5 output's last row is hidden (0 0 1 0 0 is the only one that fits).
- V4 (board): in solve(), `break` exits only the inner loop, so the first empty cell is lost (fixed with `if (j < N) break;`). The `rs` line reads like `i - j % s` (should be `i - i % s`). `int g[N][N]` needs a constant N. Spoken slips couldn't be checked (no transcript).

### Greedy: teacher slips flagged
- V1 (board): mixes `coins[]` and `coin[i]`.
- V3 (board): `myCmp` is declared `void`; it must return `bool`.
- V4 (board): `Arrays.sort(arr, MyCmp)` needs an instance, `new MyCmp()`.
- V5: an "Else if" with no preceding if. The transcript says I2 is "50 kg" (it's 5) and "divided by 15" for the partial value.
- V7 (board): `Array.sort(arr)` for `Arrays.sort`.
- V9 (board): 00001 is listed as "aac" and "bc", which decode 0001. The real decodings of 00001 are aaac, bac and abc.
- V10 (board): the frequency-50 leaf is labelled "b 50" and printed "b 10" (it's d). The high-level code list shows "a 1100" twice.
- V11 (board): `compare` returns `l->freq < r->freq`, which makes priority_queue a max heap (a min heap needs `>`). `new Node(arr[i], freq[i])` and `new Node('$', …)` swap the constructor's (freq, ch) order. `int arr[]` should be `char arr[]`. The transcript and one tree say "b" for d 40 (d 111).
- Videos without a transcript (4, 7, 10): spoken slips couldn't be checked.

### Graph: teacher slips flagged
- V5 (board): `int V = 5;` for a 4-vertex graph.
- V9 (board): the C++ source DFS calls `DFSRec(adj, s)` without `visited`.
- V13 (board/description): `recSt[3] = false` should be `recSt[s] = false`; `&&` is drawn like "$$". V13 and V15's descriptions say "Undirected Graph" for directed-graph cycle detection.
- V14: Kahn's is said to use "O(E) extra space"; the in-degree array is size V.
- V19, V20, V22 (board): `&&` is drawn like "$$"; `vector<int> graph[]` is used as a V × V matrix. V20's inner update is partly hidden (taken from the transcript). V23 (board) writes `min` for Java's `Math.min`.
- V21 (board): the C–F edge weight (1) is hidden; it's taken from the transcript.
- V26: "works in big-oh of V plus e" in the summary; Bellman–Ford is O(VE).
- Videos without a transcript (19, 22, 23, 25, 27): spoken slips couldn't be checked.

### Heap: teacher slips flagged
- V3, V5, V6 (board): `&&` is drawn like "$$".
- V4: "smallest is initialized as zero" (it's i); "int mix Int Max" means `INT_MAX`.
- V6 (board): the `heapSort` loop calls `heapify(arr, i, 0)` though the function is `maxHeapify`. The transcript says intro sort switches when recursion depth "can become O(log n)"; it switches when the depth goes beyond log n.
- V7 (board): the comparator body `p1.ht < p2.ht;` is missing `return`; `&p1` is drawn like "$p1".
- V9 (board/teacher): the min-heap declaration lacks a comma before `greater<int>`. Pop and push are called "log n"; with k + 1 items they're log k.
- V13: the complexity is first said with "K the maximum number of elements in any array" (the notation is swapped). The members are called "aPov/bPov"; the board has `aPos`/`vPos`.
- V14 (board/teacher): `Collections.ReverseOrder()` for `reverseOrder()`; `s.push(g.poll())` mixes C++ and Java. The transcript says "12 plus 15 37" (27) and "this 50" (15).
- The "K Closest Elements" article solves a sorted-array, exclude-x variant, different from the video's.
- Videos without a transcript (5, 8, 12): spoken slips couldn't be checked.

### Binary Search Tree: teacher slips flagged
- V7: in the iterative trace, "parent → right equal to 10"; the code sets `parent->right = temp` (20).
- V8 (board): `curr = (curr.right);` has an extra parenthesis. In the final if-else, the teacher says "smaller → insert left"; the code inserts left when `parent.key > x`.
- V10: the successor function is said to work "only when your right child is empty" (it's *non*-empty), and the successor is called the "leftmost leaf" (it's the leftmost node). `&&` is drawn like "88".
- V11 (board/teacher): `&&` is drawn like "$$". The first delete-30 walk-through says "root.right" where the parent assigns `root.left`.
- V12: "58 is greater than 15" at the root, which is 50.
- V14 (board): `Node res = null` has no semicolon. The x = 58 trace ends with "reference of 50"; the floor is 55.
- V15: in the x = 63 trace, "63 is greater … 70 is smaller" is backwards (50 < 63, 70 > 63).
- V17 (board, no transcript): "Balace Factor".
- V20: for 15, "only one element which is greater"; 30 is the only one ≥ 15.
- V21 (board/teacher): the naive pseudo code calls `printKth(root.right)` without k. On insert, the transcript says "decrement the lcount"; it should increment (delete decrements).
- V22 (board/teacher): `&&` is drawn like "$$". `int prev = INT_MIN` has no semicolon. "Greater than 80, like 22" means greater than 20.
- V23 (board, no transcript): `&&` is drawn like "$$". The final swap isn't written on the board (it's in the description).
- V24 (board): the last call is `isPairBST` for `isPairSum`; `&s` is drawn like "$s".
- V25 (board/teacher): `TreeMab`, `Mab.Entry`; printing uses `mp.getValue()` for `sum.getValue()`. The transcript reads the output as "−30, 20, 40+10 50, 50".
- V26 (board/teacher): the printing board has (−1, {30}) for {20}, and the spoken output "40, 30, 10 50, 30" differs from the board's 40 | 20 | 10 50 | 30.
- Videos without a transcript (13, 17, 23): spoken slips couldn't be checked.

### Tree: teacher slips flagged
- V6 (board): the Java version writes `root != NULL`; Java uses `null`.
- V8 (board): the C++ version writes `height(roo->left)`.
- V15, V18 (board): the C++ queue front is read with `q.top()`; `std::queue` uses `q.front()`. V18's Java also starts with `q.push(root)` and `q.inEmpty()`.
- V16, V17, V23, V24 (board): `&&` is drawn like "$$" or "88". V16's ✗ mark only demonstrates the missing leaf check. V17 also writes `isBlanced` and `Nod root`.
- V19 (board): the Java left call is `BToDLL` for `BTToDLL`.
- V20: the C++ code declares `inIndx` and uses `inIndex`. For hashing the teacher says `unordered_set`/`HashSet`, but a key → index table is `unordered_map`/`HashMap`.
- V21 (board): the Java header is `prinSpiral`. The second Method 2 example's last level, as read in the transcript, doesn't match the board and is left out.
- V22: "the map can be built in O(1)" (it's O(n)); the Java `int res = 0` has no semicolon.
- V23 (board): the Java `lca` declares `ArrayList<Integer>` paths though `findPath` takes `ArrayList<Node>`.
- V25 (board): the `Distance` constructor sets `val = v` for `val = d`; `Dis ldist` stands for `Distance ldist`. The code doesn't return −1 for a missing leaf, despite the problem statement.
- V26 (board): headers are `countNode` while the calls are `countNodes`; the C++ header has `root *root`; the Java `Math.pow` needs an `(int)` cast.
- V27: the Java deserialize uses `arr[index]` on an ArrayList (needs `.get`). The teacher says the −1 call "returns −1" (it returns null).
- V28 (board): the stack is declared `st` but used as `s`.
- V29: "DFS traversal or level order traversal, we use a queue". Level order is BFS.
- V30 (board): the first sketch pushes the root and loops while the stack isn't empty; the final code doesn't push the root and loops while `curr != NULL || !st.empty()`.
- V10 (no transcript): spoken slips couldn't be checked.

### Deque: teacher slips flagged
- V4 (board): Example 2's last two lines print `g.getFirst()`/`g.getLast()`; the deque is `d`.
- V6 (board): the Java `insertMin()`/`insertMax()` are written with no parameter, though the bodies use `x`.
- V7 (board): the C++ second loop ends `dq.push_back();` for `dq.push_back(i);`; `&&` is drawn like "$$".
- The "Design a Data Structure with Min and Max operations" article solves a different problem (a queue with getMin) from the video's.

### Queue: teacher slips flagged
- V3 (board): the circular-array formulas on the 10:50 board are labelled with enque/deque swapped; the final code has them right.
- V7 (board): the stack-using-queue `pop()` returns `q1.front()` without removing it, and push uses `q1.top()`/`q2.top()` (std::queue has `front()`).
- V9 (board): `queue<int>` (Java `Queue<Integer>`) holds strings, and the front is read with `q.top()`.
- Videos without a transcript (V3, V4, V8): spoken slips couldn't be checked.

### Stack: teacher slips flagged
- V3 (board): the Java ArrayList stack heads isEmpty with `bool` for `boolean`.
- V8 (board): after the pop the remaining stack is drawn as just 10, though 10 and 20 remain.
- V9 (board): the Java version writes `str.CharAt(i)` for `charAt`.
- V10 (board): push2 omits `arr[top2] = x;`, and the second pop is headed `pop1()` again.
- V11 (board): the C++ KStacks constructor never allocates `next`.
- V17 (board): the first loop mixes `st.top()`/`st.pop()` with the stack named `s`.
- V20 (board): the empty-stack case in push writes `min = t` for `min = x` (both methods).
- `&&` is drawn like "$$" (V9, V13, V14, V17). Videos without a transcript (V1–V5, V8, V9, V13, V20): spoken slips couldn't be checked.

### Linked List: teacher slips flagged
- V13 (board): the Java version's second check is `if(head.next = null)`, an assignment; it should be `==`.
- V3 (board): the short version's third line is written `head -> next => next`.
- V33 (board): the Java sorted insert writes `curr.next.dat` for `data`. The course Description's second example shows a stray leading 5 (10→20→30, x = 25 → "5->10->20->25->30").
- V35 (board): the Java Method 1 signature omits `int n`.
- V40 (Description): the first example's output is "30->10->20->50->40"; the board and transcript give 30→20→10→50→40.
- V43 (board): the detect-and-remove code breaks when the loop starts at head (m = 0, more than one node): the second phase doesn't run, and `fast->next = NULL` cuts head's next.
- V45 (board): the C++ segregate's odd branch is `os = oe = NULL;`; it should be `curr`. `x` is undeclared in V45 and V46.
- V48 (board): the C++ base case uses `and` where `||` is meant; V48 and V49 draw the naive "After Second Iteration" as 1→2→4→3→5 instead of 2→1→4→3→5.
- V50/V51 (board): C++ Method 1 uses `.` on `Node *` map values; `curri` for `curr`; Java Step 3 uses a reference as a condition, Step 2 has `curr.next, next`, and `Node curr` is redeclared.
- V52: the Description expands LRU as "Last Recently Used"; the transcript says "20 and R4" where R2 is meant.
- V53 (board): `Node *head = NULL; *tail = NULL;`, with a semicolon for a comma.
- V54 (board): the C++ efficient signature takes `root` but the body uses `head`.
- `&&` is drawn like "$$" (V11). Videos without a transcript (17 of them): spoken slips couldn't be checked.

### Strings: teacher slips flagged
- V2 (board, no transcript): in the C++ string comparison, `s1 < s2` prints "Greater" and the else prints "Smaller", the reverse of the strcmp version; strcmp/strcpy are written "strcmb"/"strcby".
- V4 (board): the naive Java palindrome is headed `bool` instead of `boolean`.
- V17 (board): the naive `areAnagram` loops `j < txt.length()`, where the pattern's length is meant; as written and described, the efficient version checks `areSame` before each slide, so the last window is never compared.
- V19 (board): the naive inner loop starts at `j = 0` instead of `j = i`; the Java efficient version fills `visited` though the array is `prev`.
- Board notation: `&` and `&&` are drawn like "$" and "$$" (V4–V8, V11, V15).
- V2 (no transcript): spoken slips couldn't be checked.

### Hashing: teacher slips flagged
- V7 (board, no transcript): the Java `remove` casts the slot index, `remove((Integer)i)`; to remove the key it would be `(Integer)key`.
- V9: the board's insert ends `table[probe] = m;`; the teacher says key. The transcript says an empty slot in search means "return true"; it means not present. At the analysis it says "Universal hashing" for double hashing.
- V10 (board): neither constructor allocates `arr` before filling it with −1; `&&` is drawn as "$$". The transcript says search "returns this index"; the function returns true.
- V12 (board, no transcript): the complexity row reads cbegin(), cend() at first and looks like rbegin(), rend() later.
- V16 (board, no transcript): the C++ efficient version has no semicolon after `s.insert(arr[i])`.
- V17 (board): both efficient `countFreq` versions are declared `int` but only print.
- V18 (board): the Java version calls `s.insert(b[i])`; HashSet's method is `add`.
- V22 (board): the C++ version declares `unordered_sum<int> h;` for unordered_set.
- V23 (board): C++ `res == i+1;` for `res = i+1;`; Java declares `Map<Integer, Integer> = new HashMap<>();` without the name m, loops to `n` (not a parameter) and calls `m.contains` for `containsKey`.
- V26 (board): Java `new Hashet<>()` and `while(s.contains(x+curr))` on s, though the set is h.
- V28 (board, no transcript): the naive inner loop has `arr[i] = arr[i-1]` (assignment) with "$$"; the C++ efficient line `m[arr[i]]++` has no semicolon; Java loops over `m` instead of `m.entrySet()`, and `n` isn't a parameter.
- Videos without a transcript (7, 12, 13, 16, 21, 28, 29): spoken slips couldn't be checked.

### Matrix: teacher slips flagged
- V2 (board): the array-of-vectors `main` calls `print(arr)` without m; the vector-of-vectors print writes `arr[i].size` without brackets; `&` is drawn like "$".
- V8 (board): the naive `rotate90(int mat[R][C])` uses n inside, and one line has no semicolon.
- V9 (board): the walkthrough writes 8 as "18" (1 2 3 4 18 12 16 …); the header reads `voia`.
- V10 (board): the efficient walkthrough for x = 29 ends "Found at (2, 3)"; it is (2, 1), as on the first board.
- V11 (board, no transcript): `upper_bound` is written "ubber_bound" and the subtraction uses `m[i]` for `mat[i]`.
- V12 (board, no transcript): the comparison uses `MedPos` for `medPos`.
- V11, V12 (no transcript): spoken slips couldn't be checked.
- Board notation: `&&` is handwritten like "$$" (V9, V10).

### Sorting: teacher slips flagged
- V10: "one more bad thing about quicksort, mergesort", meaning merge sort.
- V11: the efficient-idea walkthrough uses a = 10, 20, 35 ("compare 35 and 50"); the board dry run uses {10, 20, 50}. The idea board writes `a[i] < b[j]`; the final code uses `<=`.
- V13: the call for the single element 5 is spoken as "L equal to 0 and R equal to one" (it is l = 1, r = 1); `l + (r-l)/2` is read as "R plus L by 2".
- V16 (board): the final while loops put `i++`/`j++` inside the `if`, so the index only moves when an element is printed.
- V17: "smaller than all the elements from i to n1 − i" means i to n1 − 1. Board: `counInv` and `countandMerge` for countInv/countAndMerge.
- V18: "an array of size temp"; the board code has a typed overlay (`&& i!=p`, `temp[index++] = arr[p]`) over the handwriting.
- V19: "your i becomes 1" after the 40 swap (board: i = 2); "i is 5" for 50 (j = 5).
- V20: the board first writes `j = h-1`, later `h+1`; "I begins with i − 1" means l − 1; j is said to keep "incrementing".
- V23 (board): the left child of qS(2, 3) is labelled qS(3, 2); the teacher says 2 to 2.
- V24: the worst case is "n − 1 elements on one side and n on the other" (1 on the other); "better than … mergesort and quicksort".
- V28 (board): the final code passes `l, r` for lo, hi, returns `p` instead of `arr[p]`, sets `high` for hi, has missing semicolons, and the last dry-run row shows 20 for 26. Its transcript is badly garbled.
- V29: the pair count is called "n*(n+1)/2 sort of expression".
- V32 (board): declares `lo` but uses `low` in the 0 case.
- V33: merging takes "min as minimum of 2 end values" (the starts); overlap is described as "start is more than end" (the code checks `end >= st`); "process them in nlogn time", then corrected to linear.
- V34: "if current arrival is more than current departure, then this arrival event is first" (the code checks `arr[i] <= dep[j]`).
- V35: "40 has to go to index zero" (10 goes there).
- V36: the board's heapSort calls `heapify` while the function is `maxHeapify`; quicksort's recursion depth "can become O(log n)".
- V37: the cumulative step is narrated "next index, index 1" (index 2); the naive function is written `counSort`.
- V38 (board): the cumulative loop starts at `i=0`, reading count[i−1]. Spoken: "because the EXP is 10" for exp = 1, and the count is "incremented" after placing (it is decremented).
- V39: "22 to 39" for the 20–39 range; the board's C++ `int max_val = arr[0]` has no semicolon.
- V12, V15, V21, V30 (no transcript): spoken slips couldn't be checked.
- Board notation: `&&` is handwritten like "$$" (V12, V15, V16, V17, V34, V36).

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
