# Ex.No: 2  Implementation of Depth First Search
### DATE:  26-08-2025                                                                          
### REGISTER NUMBER : 212223060070
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:

def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()
    
    # Mark the current node as visited
    visited.add(start)
    print(start, end=" ")

    # Recur for all the neighbors
    for neighbor in graph[start]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)

if __name__ == "__main__":
    # Graph represented as adjacency list
    graph = {
        'A': ['B', 'C'],
        'B': ['D'],
        'C': ['E'],
        'D': ['F'],
        'E': [],
        'F': []
    }

    print("DFS traversal starting from node A:")
    dfs(graph, 'A')

### Output:
DFS traversal starting from node A:
A B D F C E


### Result:
Thus the depth first search order was found sucessfully.
