[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/JWEh_q2R)

# Multi-Queue Round-Robin Café (Interactive CLI)

## How to run

1.  Ensure you are in the *root directory* of the repository (the folder containing src and tests).
2.  Execute the main CLI module using the Python package flag


## How to run tests locally
1. Ensure you have pytest installed:

pip install pytest

2. Execute the test suite from the project root:

pytest



## Complexity Notes
Complexity Notes Justification
Category:		
Queue Design	

Complexity: Custom Queue with Front Index	

Justification: The CustomQueue uses a standard Python list with a front index. This avoids the slow O(N) shift operation of list.pop(0). Periodic list compaction (trimming) ensures the performance stays efficient.

Time Complexity		
Enqueue/Dequeue	Amortized O(1)	Enqueue (list.append()) is amortized O(1). Dequeue is O(1) by index access, with the occasional O(N) compaction cost spread across many operations, making it amortized O(1).
Run	O(#turns+total_minutes_worked)	Runtime is dominated by the number of turns executed plus the total work time consumed across all tasks.
Space Complexity	O(N tasks+metadata)	Space scales linearly with the total number of tasks 👎 currently in all queues

## *Delete this section before submission.*
### Common pitfalls
- Display should print after each RUN turn only.

- Don’t advance time on empty or skipped queues.

- Enforce 1 ≤ steps ≤ #queues for RUN.

- Auto task IDs per queue: <queue_id>-NNN (zero-padded).

- Use exact messages:

    - Sorry, we're at capacity.

    - Sorry, we don't serve that.


### Grading rubric (I will be using this to grade your submission)

*__Correctness (50):__* RR behavior, logs, display-per-turn, auto task ids, menu handling, rejects.

*__Complexity notes (15):__* correct, concise, justified.

*__Student tests (15):__* ≥4 targeted, deterministic tests incl. steps validation.

*__Code quality (10):__* structure, type hints on public surfaces, docstrings, PEP 8.

*__Docs & UX (10):__* README completeness; exact messages; clear CLI.
classroom.github.com
Write to Rohit Chhantyal
