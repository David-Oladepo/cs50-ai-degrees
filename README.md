# Degrees of Separation — CS50 AI

A Python implementation of the **Degrees of Separation** problem, developed as part of Harvard's CS50's Introduction to Artificial Intelligence with Python.

The program finds the shortest connection between two actors through films they have appeared in together.

## Project Overview

The goal is to determine the minimum number of movie connections separating one actor from another. Each connection represents a shared movie.

For example, if Actor A appeared in a film with Actor B, and Actor B appeared in another film with Actor C, then A and C are connected by a path of two movie links.

## Algorithm

This project uses **Breadth-First Search (BFS)** to find the shortest path in an unweighted graph.

The implementation:

1. Starts from the source actor.
2. Explores neighbouring actors using a FIFO queue.
3. Tracks explored actors to avoid unnecessary revisits.
4. Stores each node's parent and connecting movie.
5. Reconstructs the shortest path when the target actor is reached.
6. Returns `None` when no path exists.

## Technologies

* Python 3
* Graph search
* Breadth-First Search (BFS)
* Data structures: queues, sets, and linked search nodes
* CSV-based dataset processing

## Project Structure

```text
cs50-ai-degrees/
├── degrees.py    # Shortest-path search implementation
├── util.py       # Node and frontier data structures
└── README.md     # Project documentation
```

## How to Run

1. Install Python 3.
2. Obtain the original CS50 Degrees starter files and datasets from the [official project page](https://cs50.harvard.edu/ai/projects/0/degrees/).
3. Place `degrees.py`, `util.py`, and the supplied `small` or `large` dataset directory in the same project directory.
4. Run the program from your terminal:

```bash
python degrees.py small
```

Follow the prompts to enter the names of two actors.

To use the larger dataset:

```bash
python degrees.py large
```

## Testing

The submitted solution passed the official CS50 `check50` tests:

* **Correctness:** 7/7 checks passed
* **Style:** 1.00

These results were recorded for the submitted CS50 course project.

## What I Learned

* Representing relationships as a graph
* Applying BFS to find shortest paths
* Using queues and explored sets
* Tracking parent nodes to reconstruct a path
* Handling cases where a target cannot be reached

## Acknowledgment

This project was completed as part of [Harvard CS50's Introduction to Artificial Intelligence with Python](https://cs50.harvard.edu/ai/). The assignment and starter materials are provided by the course.

---

**Author:** David Oladepo

**Language:** Python

**Focus:** Artificial Intelligence · Graph Algorithms · Search
