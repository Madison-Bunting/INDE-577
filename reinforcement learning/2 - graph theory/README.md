# Graph Theory

**Graphs**, in the context of graph theory, are visual representations *relationships* rather than values or statistics. As a primer, a history lesson:

Kaliningrad, Russia was formerly known as Konigsberg Prussia. In the early 1700s, that city had a river going between it that had two islands in the middle, and various bridges connecting the land masses, as illustrated below.

![image](https://miro.medium.com/max/1050/1*EnntiaJYoXdz2swncIpFJQ.jpeg)

Villagers challenged each other to touch all the land masses without crossing any of the bridges more than once, but no one was able to do it. Euler (from Euler's constant) eventually decided to investigate this puzzle, and his research birthed the fields of graph theory and topology in mathematics. He decided to simplify the problem, and re-drew the map as shown below.

![image](https://miro.medium.com/max/1050/1*94Ex37b-oFyV8Dc_Okp2nQ.jpeg)

Euler realized that, ultimately, the properties of the bridges did not matter; not the size, material, length, or whether they were over water or land. The only things that mattered were the land masses, and the concept of the "bridge" as something that linked those land massses. Hence, mathematical graphs represent *realtionships*, not values or numbers like business pie charts and bar graphs. (The answer to the puzzle was that because there was an even number of land masses connected by an odd number of bridges points, it is impossible to touch all the land masses without crossing a bridge twice).

**A (non-comprehensive) list of definitions:**
- node: a connection point (in the case of the bridge problem, these were the land masses)
- edge: a line that connects two nodes (in the case of the bridge problem, these were the bridges)
- self-loop: a node that has an edge that connects to itself
- label: edges and/or nodes can be associated with letters, numbers, or symbols to make them easier to talk about (like how Euclid labeled the land masses A, B, C, and D)
- weights: sometimes, properties of the edges do matter, in which case those can be added to the graph as "weight" labels. For example, if the goal of the bridge problem was to get from land mass B to land mass C as quickly as possible, the length of the bridges would matter
- walk: traversing a graph
  - closed walk: destination node is the same as the source node (the walk starts and ends in the same place)
- trail: a walk with no repeated edges (what the villagers were trying to do in the bridge problem)
  - circuit: a closed trail
- path: a walk with no repeated nodes
  - cycle: a closed path

**Properties of graphs for classification:**
- Directed: edges have arrows on them that indicate directionality. For example, if the bridges were on-way roads
- Undirected: edges have no directionality
Graphs can have a combination of directed and undirected edges.

or

- Heterogeneous: there are different types of nodes in the graph
- Homogeneous: nodes within the graph are of the same type. Of these kinds of graphs, nodes are either
  - static: nodes and edges do not change; nothing is added or taken away
  - dynamic: nodes and edges can chang, be added, deleted, moved, etc

or

- Dense: composed of many nodes and edges
- Sparse: composed of fewer nodes and edges

or

- planar: nodes and edges can be visualized in such a way that none of them intersect
- non-planar: there is no way to rearrange the nodes and edges in a way that keeps the edges from intersecting

![image](https://miro.medium.com/max/900/0*EFTtnCgA_ESQ86LW.png)

**Visualizing graphs on computers:**
- incidence matrix (I): made up of -1, 0, 1

![image](https://miro.medium.com/max/1050/1*9Ux80uESvaUdtkEyRMYajw.png)

- (Weighted) Adjacency Matrix (A): also made up of 0 and 1 unless otherwise weighted or labeled. Thus, undirected graphs are symmetrical along their diagonals, as shown below. If graphs are weighted, the value of the weights replaces the 1s in the matrix. 

![image](https://user-images.githubusercontent.com/89811204/145887037-1f58aa47-df13-46f4-92be-07af65ffb3d3.png)

- Degree matrix (D): the number of degrees of a node is the number of edges attached to it. When in matrix form this means the value of each diagonal in the adjacency matrix is the degree of its corresponding node

![image](https://miro.medium.com/max/1050/0*q162kpWGY8o4GeL8.png)

Graphs can also have fun names!

![image](https://user-images.githubusercontent.com/89811204/145886971-ec9a068c-be7d-4a1c-9640-1480608aeb0c.png) 

Graph theory is particularly useful in developing Geometric Deep Learning models. Because the [Graph Theory notebook](https://github.com/Madison-Bunting/INDE-577/blob/main/reinforcement%20learning/2%20-%20graph%20theory/Graph%20Theory.ipynb) focuses on visualization, further investigation of the intersetion of graph theory and machine learning will be left to the reader. [This article](https://flawnsontong.medium.com/what-is-geometric-deep-learning-b2adb662d91d) is a great starting point.

