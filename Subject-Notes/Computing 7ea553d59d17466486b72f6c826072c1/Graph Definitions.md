# Graph Definitions

# Walk

A walk is a sequence of nodes/edges in a graph.

# Trail

Is a walk with *no* repeated edges but can repeat nodes.

# Path

Is a walk containing no repeated edges and no repeated nodes.

# Cycle

Is a path that starts and ends on the same node (that start and end node is the one exception to the rule of paths that there can be no repeated nodes).

# Order

The number of vertices or nodes, $|V|$.

# Size

Number of edges of a graph, $|E|$.

# Diameter

The number of edges in the longest, shortest path between any pair of nodes. THe diameter of a disconnected graph is always infinity.

# Eulerian Trails

Are trails (so they don’t repeat edges) that include all edges in a graph. In order for a Eulerian trail to exist, the graph would need to have exactly zero or two odd-degree nodes.

This is because you need to enter and exit each node, In order to move around the graph.

![Screenshot 2024-09-23 at 6.58.49 am.png](Graph%20Definitions%20109b7c5a9ed08042916af533aa3c868b/Screenshot_2024-09-23_at_6.58.49_am.png)

- These are also Eulerian Circuits, which are just eulerian trails but that start and end at the sane node.
- These circuits exist only if the graph is connected and if all the nodes of the graph have an even degree.

# Hamiltonian Path

Is a path (that is, contains no repeated edges or nodes) that includes all nodes in a graph.

# Hamiltonian Cycle

Is a Hamiltonian Path that starts and ends at the same node. (note the starting node is an exception to the no repeated nodes rule).

They are also said to be Hamiltonian paths that end at a node that is adjacent to the starting node. That is the end node needs to have an edge connecting it with the start node. 

This is an example of a Hamiltonian path

![Screenshot 2024-09-23 at 7.05.03 am.png](Graph%20Definitions%20109b7c5a9ed08042916af533aa3c868b/Screenshot_2024-09-23_at_7.05.03_am.png)

# Adjacency Matrices

We can represent a graph in a different way, as an adjacency matrix. Adjacency Matrices record the number of connections between the nodes of a graph. Below is a graph and underneath it, is its adjacency matrix.

![image.png](Graph%20Definitions%20109b7c5a9ed08042916af533aa3c868b/image.png)

![image.png](Graph%20Definitions%20109b7c5a9ed08042916af533aa3c868b/image%201.png)

- Every adjacency matrix has a row and a column for each node in the graph. The number represents the amount of edges connecting the node on the row to the node on the column.
- So, the 2 at the intersection of “a” and “b” means that there are two edges between the nodes “a” and “b”.