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

**Notes written: 13 of 24 tracks · 294 of 470 videos · 221 of 342 articles · 214 of 367 problems listed.** All work is on branch `claude/project-thread-8jxc30`. Track 1 is also in the private artifact.

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
| 14 | Deque | 8 | 7 | 6 | ⏭ Next |
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
- (this commit): Add Queue track notes (9 videos, 5 articles, 9 problems)

### What's next
- **Track 14: Deque** (8 videos, 7 articles, 6 problems), starting straight away.

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
