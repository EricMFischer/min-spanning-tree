## Synopsis
Here we'll code up Prim's minimum spanning tree algorithm.
The accompanying text file describes an undirected graph with integer edge costs. It has the format:

[number_of_nodes] [number_of_edges]
[one_node_of_edge_1] [other_node_of_edge_1] [edge_1_cost]
[one_node_of_edge_2] [other_node_of_edge_2] [edge_2_cost]
...

For example, the third line of the file is "2 3 -8874", indicating that there is an edge
connecting vertex #2 and vertex #3 that has cost -8874. Do NOT assume that edge costs are positive, nor that they are distinct.

Run Prim's minimum spanning tree algorithm on this graph, and reported the
overall cost of a minimum spanning tree --- an integer, which may or may not be negative.

IMPLEMENTATION NOTES: This graph is small enough that the straightforward O(mn) time
implementation of Prim's algorithm should work fine. OPTIONAL: For an
additional challenge, try implementing a heap-based version. The simpler approach, which should
already give a healthy speed-up, is to maintain relevant edges in a heap (with keys = edge
costs). The superior approach stores the unprocessed vertices in the heap. Note this requires
a heap that supports deletions and requires one to maintain
some kind of mapping between vertices and their positions in the heap.

## Motivation

Prim's minimum spanning tree algorithm to compute overall cost provides an **O(mn)** solution by using a heap to maintain relevant edges. But we can generate an even better solution with another heap to store the unprocessed vertices. So again, we can see how using a heap is a great way to optimize a pre-existing algorithm that is dependent on looking up some kind of data.

## Acknowledgements

This algorithm is part of the Stanford University Algorithms 4-Course Specialization on Coursera, instructed by Tim Roughgarden.
