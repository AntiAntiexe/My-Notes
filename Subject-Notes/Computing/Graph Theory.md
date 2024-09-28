# Graph Theory

- A large part of time in algorithmics is devoted to the study of graohs, they are useful in representing data.
- This is an example of a graph:

![image.png](Subject-Notes/Computing/Graph%20Theory/image.png)

## Nodes and Edges

- These are **nodes**:

![image.png](Subject-Notes/Computing/Graph%20Theory/image%201.png)

- Nodes (also sometimes called vertices) represent some point of data (maybe a city, house, computer, or road intersection).
- To provide information about how two nodes are related we can connect then together with an edge.

![image.png](Subject-Notes/Computing/Graph%20Theory/image%202.png)

- Edges represent a connect between two things that themselves are represented as nodes. E.g.
    - roads connecting cities or network cables connecting computer
- IN the above graoh there is a 10 over the edge. That is the edge’s weight, it can be used to represent the distance between two planes, or the number of changes between two states.
- The weight of an edge represents a characteristic of that connection between nodes.
- Edges can also be directed, this means that they have a direction by which the connection goes. This is represented by the arrow on the end of the edge. We call the node at the end of the arrow the target node, and the one at the start the source node.

![image.png](Subject-Notes/Computing/Graph%20Theory/image%203.png)

- Nodes also have a characteristic that descibe the number of edges connected to them. This is called their degree.

![image.png](Subject-Notes/Computing/Graph%20Theory/image%204.png)

## Notation

- A graph can be expressed as:

$$
G=\{V, \ E\}, \ V = \{\text{Vertices}\}, \ E = \{\text{Edges}\}
$$

# Circuits

- A graph contains a circuit if there is more than one path that connects two nodes. This pops up when there is a “loop” or “circle” in the edges of a graoh.
- Circuits themselves specifically contain no repeated edges (but they can contain repeated nodes) and start and end on the same node.
    
    > Note: In the graoh below, there is a circuit following the path of “a”, “b”, “c” then “a” again. If there wasn’t an edge between “c” and “a”, then there wouldn’t be a circuit in this graph.
    > 

![image.png](Subject-Notes/Computing/Graph%20Theory/image%205.png)

# Graphs

A graph is a collection of nodes and edges that may or may not be joining those nodes. These are some specific categories of graph:

- **Connected Graphs:** These graphs are ones where every
node is connected to every other node, either directly or indirectly.
That is, starting from any node, you can reach any other node by
traversing one or more edges.
    - Minimum edges required: $|E| = |V| - 1$
    - A bridge is an edge which, if deleted, cause the graph to become disconnected.
- **Directed Graphs:** Directed graphs feature exclusively edges that are directed.
    - $A \rightarrow B$  exists, but $B \rightarrow A$ might not.
        
        ![image.png](Subject-Notes/Computing/Graph%20Theory/image%206.png)
        
- **Complete Graphs:** Every node is adjacent to every other vertex.
    - Degree (No. of edges incident ti a vertex) = $|V|-1$
    - Size: $|E| = \frac{|V|(|V|-1)}{2}$
        
        ![image.png](Subject-Notes/Computing/Graph%20Theory/image%207.png)
        
- **Weighted Graphs:** A Weighted graph is one that has weights on all of its edges.
- **Labelled Graphs:** A Labelled graph has got labels on all of its nodes.
- **Trees:** A tree is a kind of graph that is connected, but does not contain any circuits.
- **Forests:** Forests are a collection of tree graphs
that are not joined to each other (although, you can connect them by
just adding one edge).
- **Subgraphs:** A Subgraph is a part of a larger graph.
All edges and nodes in a subgraph must be in the original graph, but not all edges and nodes in the original graph have to be in the subgraph.

## Weight

Graphs also have a property called width. On weighted graphs, the width is the maximum of the minimum distance between two nodes (that is, where you sum up all the edge weights between those two nodes). So, for the graph below, the weight would be 19. This is because the minimum distance path between "b" and "d" is the longest of the paths in the graph.

![Screenshot 2024-09-22 at 7.58.46 pm.png](Screenshot_2024-09-22_at_7.58.46_pm.png)

The only way to calculate the width of a graph is to go through every apri of nodes and find the minimum distance between them.

> On an unweighted graph, the width is found by assuming that each edge has a weight of one.
> 

# Coloured Graph

A method for managing conflicts of interest & resource allocation. IN a coloured graph, adjacent vertices muct have different colours.

**Chromatic Number:** The minimum value of $k$ such that $k$-coloured graph can exist for a given graph.

![image.png](image%208.png)

# Minimum Spanning Trees

A Minimum Spanning Tree (MST) is a subset if a connected, undirected and weighted graph that represents the tree that connects all nodes in that graph with the smallest distance possible. As an MST is a tree, it cannot have any circuits in it.

For the previous graph, the minimum spanning tree would look something like the tree highlighted in green here:

![image.png](image%209.png)

> Note: the edge between the nodes “e” and “b” could be switched for the edge between “a” and “b” or the one between “c” and “b”. This is because they all connect the tree to node “b” and have the same weight.
> 

## How to find the minimum spanning tree

The easiest method is **Prim’s Algorithm**. These are the generalised steps:

1. Choose a starting node (it doesn’t matter which one you go with).

2. Look at the edges coming out of that node and choose the one with the lowest weight (if there are multiple with the same weight, it doesn’t 
matter which one you pick). These nodes and the edge that connects them will form the start of the MST.

3. Now look at all the edges coming of from the nodes currently in your 
tree and select once again the edge with the smallest weight. But do not pick an edge that would connect the graph to itself.

4. Repeat this process until all the nodes are connected.