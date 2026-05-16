# Edge-Weighted Graph Refactoring (Vertex-Oriented Approach)

## Project Overview
This project refactors a classic edge-weighted graph structure by eliminating the traditional, separate `Edge` class. Instead, it implements an **object-oriented, distributed adjacency list** where each vertex manages its own outgoing connections and weights. 

## Key Architectural Changes
* **Removed `Edge` Class:** Edge data is now fully integrated inside the vertices.
* **Updated `Vertex<V>`:** Encapsulates underlying data and a `Map<Vertex<V>, Double> adjacentVertices` to map destinations directly to edge weights.
* **Simplified `WeightedGraph<V>`:** Replaced the complex `Map<Vertex, List<Edge>>` structure with a clean, straightforward registry list: `List<Vertex<V>>`.

---

## Algorithms Implemented
* **Breadth-First Search (BFS):** Graph traversal to check connectivity and unweighted paths.
* **Dijkstra's Algorithm:** Shortest-path calculation utilizing a `PriorityQueue` for optimal vertex relaxation.

---

## Class Structure
* `Vertex.java` – Represents a graph node with localized adjacency data.
* `WeightedGraph.java` – Manages the collection of vertices.
* `Search.java` – Abstract base class handling path-tracking properties.
* `BreadthFirstSearch.java` – BFS traversal logic.
* `DijkstraSearch.java` – Dijkstra's shortest path logic.
* `Main.java` – Practical demonstration using a map of cities.
