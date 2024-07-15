# Breadth First Search Project



## Objective

In this project, we will cover the fundamentals of a Breadth-first search, and how to implement it using a Linked list.


## Problem


Create `breadthFirstSearch` function to perform a breadth-first traversal of a binary tree.

## Implementation
* Create a LinkedLis named queue to store the nodes that must be processed during the traversal.
* The `root` node is added to the queue using the `add` method. This marks the start of the traversal.
* Create a loop that continues until the queue is empty, the condition `!queue.isEmpty()` is used to check if there are any remaining nodes to process.
* Inside the loop, the first node in the queue is removed using the `poll` method, which returns and removes the head of the queue. The removed node is assigned to the current variable.
* If the current node has a left child `current.left != null`, it is enqueued by adding it to the queue using the add method. This ensures that the left child will be processed in the subsequent iterations.
* if the current node has a right child `current.right is not null`, it is enqueued by adding it to the queue.
* The loop continues to the next iteration, where the next node in the queue becomes the current node, this process repeats until all nodes have been processed and the queue becomes empty.

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
