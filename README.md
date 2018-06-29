# Map Reduce-Single Target Shortest Path
By Shuning Zhao April 2018

Given a graph and a node “t”, find the shortest distances of all nodes to “t” together with the paths. For example, the shortest distance from node 1 to t is 7 with path 1->3->4->t. Please note that this is different from the single-source shortest path problem!! However, you can make minor modifications to the algorithm for that problem to solve this one.

![](https://github.com/ShuningZhao/MapReduce-SingleTargetShortestPath/blob/master/Images/01Graph.png?raw=true)

**Input files:**  
In the [input file](https://webcms3.cse.unsw.edu.au/COMP9313/18s1/resources/15990), each line is in format of:  
“EdgeId FromNodeId ToNodeId Distance”.  
In the above example, the input contains (assume t has node id 0):

![](https://github.com/ShuningZhao/MapReduce-SingleTargetShortestPath/blob/master/Images/02Input.png?raw=true)

**Output:**  
Set the number of reducers to 1. The single output file contains the shortest distances and paths of all nodes to the given node. Each line is in format of “SourceNodeID\tDistance\tPath”. The shortest distances are of double precision, and each path is a sequence of nodes on the shortest path. Remove the nodes that cannot reach the query node and sort the output by SourceNodeID according to its numeric value. Given the example graph,
the output file is like:

![](https://github.com/ShuningZhao/MapReduce-SingleTargetShortestPath/blob/master/Images/03output.png?raw=true)

**Files**  
The file [SingleTargetSP.java](https://github.com/ShuningZhao/MapReduce-SingleTargetShortestPath/blob/master/SingleTargetSP.java) takes three parameters: the input folder containing the graph file, the output folder storing the result file and the query target node ID.