# Binary search tree

## Prerequisites
![](https://blog.penjee.com/wp-content/uploads/2015/11/binary-search-tree-insertion-animation.gif)

Hello there fellow traveler, you are steping into the wild forests of the binary trees.
First, make sure that you have installed Python3 and some IDE to develop your code in.
Using Ubuntu/Mint you can make it like this:

```sh
  sudo apt-get install python3
```
 
 After it you may install IDE to simplify your development, I would recommend PyCharm(https://www.jetbrains.com/pycharm/).
 
 And after all of this we may go to coding.
 
 ## Practice
 
 Binary search tree is a data structure, and as each datastructure it has its own class, but before creating a tree itself we need to create a singular binary node, as each node have two possible children left and right, and value:
  
 ```python
 class Node:
    def __init__(self, value):
        self.right = None
        self.left = None
        self.value = value
  ```
  
   After Node creation we may start our work on our binary tree, it may consist out of hundreds, thouthands of nodes, but we don't need to store them all, all we need is just a head, or root, in current terminology:
  
 ```python
 class BinSearchTree:

    def __init__(self):
        self.root = None
         
    def insert(self, value):
      # insert functionality
      
    def search(self, value):
      # search functionality
    
    def delete(self, value):
      # delete functionality

 ```
 
 Those are main functions of Binary Search tree, we may also use verifyTree() function to check if tree is indeed binary search tree.
 Let's implement insert functionality:
  
 ```python
     def insert(self, value):
        #checking if root is empty
        if self.root is None:
            self.root = Node(value)
            return
        node = self.root
        # Searching for the place to insert our node
        while True:
            if node.value > value:
                if node.right is None:
                    node.right = Node(value)
                    return
                else:
                    node = node.right
            else:
                if node.left is None:
                    node.left = Node(value)
                    return
                else:
                    node = node.left

 ```
 
 That's nice, if you implemented everything correctly code below should work: 
 
 ```python
binSearch = BinSearchTree()
binSearch.insert(5)
binSearch.insert(1)
binSearch.insert(7)
binSearch.insert(16)
binSearch.insert(4)
 ```
 
 To accomplish the lab, accomplish the remaining functionality(search and delete by value). If you want to be a realy cool guy, you may also try to remove worst cale of O(n) performance.
 
