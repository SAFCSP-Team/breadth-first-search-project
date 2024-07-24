# Breadth First Search Project



## Objective

In this project, we will cover the fundamentals of a Breadth-first search, and how to implement it using a Linked list.


## Problem


Create `breadthFirstSearch` function to perform a breadth-first traversal of a binary tree.

## Implementation

* Create a LinkedList named `bfsobj` to store the nodes that must be processed during the traversal.
* The root node is added to the `bfsobj` using the add method. This marks the start of the traversal.
* Loop the queue until it's empty. Use the condition `!queue.isEmpty()` to stop the loop, and check if there are any remaining nodes to process.
* Within the loop, the first node in the `bfsobj` is dequeued using the poll method, which both returns and removes the head of the queue. The dequeued node is assigned to the current variable.
* If the current node has a left child `current.left != null`, it is enqueued by adding it to the `bfsobj` using the add method. This ensures that the left child will be processed in the subsequent iterations.
* If the current node has a right child `current.right` is not null, it is enqueued by adding it to the `bfsobj`.
* Repeats until all nodes have been processed, and the `bfsobj` becomes empty.

the output 
```java
Breadth-First Search:
1 2 3 4 5 6 7
```


  
```java
public class Breadthfirstsearch {

    private static class Node {
        int value;
        Node left;
        Node right;

        Node(int value) {
            this.value = value;
            left = null;
            right = null;
        }
    }

    public static void breadthFirstSearch(Node root) {
        if (root == null) {
            return;
        }

           /* write your code here */
    }

    public static void main(String[] args) {
        Node root = new Node(1);
        root.left = new Node(2);
        root.right = new Node(3);
        root.left.left = new Node(4);
        root.left.right = new Node(5);
        root.right.left = new Node(6);
        root.right.right = new Node(7);

        System.out.println("Breadth-First Search:");
        breadthFirstSearch(root);
    }
}

```
