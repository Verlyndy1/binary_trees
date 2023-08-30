C - Binary trees
A binary tree is a type of data structure used in computer science and programming. It is composed of nodes, where each node can have at most two children referred to as the left child and the right child. The binary tree follows a hierarchical structure, starting from the root node and branching out to form subtrees.

Here are some key properties of a binary tree:
Root Node: The topmost node in the tree is called the root node. It is the starting point of the tree.

Nodes and Children: Each node in a binary tree can have at most two children, a left child and a right child. These children nodes can themselves be the root of their own subtrees.

Leaf Nodes: Nodes that do not have any children are called leaf nodes or terminal nodes. They are located at the bottom of the tree.

Internal Nodes: Nodes that have at least one child are called internal nodes. They are located between the root and leaf nodes.

Parent and Siblings: In a binary tree, each node (except the root) has a parent node, which is the node directly above it. Nodes that share the same parent are called siblings.

Binary trees can be used to represent various data structures or solve specific problems efficiently. Some common applications of binary trees include binary search trees, expression trees, and binary heaps. The binary tree structure allows for efficient search, insertion, and deletion operations in certain cases, depending on the specific type of binary tree being used.

In C, a binary tree can be represented using a structure and pointers. Here's an example:
struct Node {
    int data;
    struct Node* left;
    struct Node* right;
};
Using this structure, we can create and manipulate a binary tree. Here's a simple example of creating a binary tree with three nodes:
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* left;
    struct Node* right;
};

struct Node* createNode(int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}

int main() {
    // Creating the nodes
    struct Node* root = createNode(1);
    struct Node* leftChild = createNode(2);
    struct Node* rightChild = createNode(3);

    // Connecting the nodes to form the tree
    root->left = leftChild;
    root->right = rightChild;

    // Accessing and printing the values of the nodes
    printf("Root Node: %d\n", root->data);
    printf("Left Child: %d\n", root->left->data);
    printf("Right Child: %d\n", root->right->data);

    return 0;
}
