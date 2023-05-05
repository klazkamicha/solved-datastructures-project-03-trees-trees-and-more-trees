Download Link: https://assignmentchef.com/product/solved-datastructures-project-03-trees-trees-and-more-trees
<br>



You are required to implement three tree data structures: a general tree, a heap tree, and an AVL tree. No tree should contain duplicate values. You are also required to create UML diagrams for each of the classes that you implement. Finally, you have to provide the means to test your system by developing a menu program that allows the user to manipulate your structures.

It is strictly prohibited to use the structures and/or algorithms defined in the C++ standard library (STL). So, if your design requires a list, queue, stack, or a hash table, you can only use your own implementations.

Underflow exceptions might be generated in some of the functions you implement. Make sure exceptions are thrown and caught where appropriate.

<h1>Deliverables</h1>

<ul>

 <li>A 1 page report with your UML diagrams that explains the design of your data structures. Please include what each teammate did and approximate hours spent on the project.</li>

 <li>An implementation of a general tree.</li>

 <li>An implementation of a heap tree.</li>

 <li>An implementation of an AVL tree.</li>

 <li>A menu program to test the implemented data structures.</li>

</ul>

<h1>1           General Tree</h1>

In this part of the project, you need to implement two classes, a <em>TreeNode Class </em>and a <em>LinkedTree Class</em>; create their respective UML diagrams. Your TreeNode class can be used for all trees (not all trees will use all data members). If you would like to include further data members you may although it is not necessary. Some of the methods are the same but have different names, you may feel free to rename them as you see fit as long as they are descriptive. Calculate the running time of your functions and include them in your report.

<em>1.1      Description</em>

<h2>1.1         Description</h2>

A tree is a structure that is formed by Nodes (vertices) and Edges (arcs). Edges connect nodes together. Any two nodes in the tree are connected by one and only one path.

<h2>1.2         Data Members</h2>

Specify all the data members your implementation needs. You are required to instantiate a <em>TreeNode </em>object for each of the nodes in the tree. Each node has a <strong>key</strong>(int) – for Heap tree only, <strong>value </strong>(Type), <strong>balanceFactor </strong>(short int: -1 for right high, 0 for balanced, 1 for left high) – for AVL tree only, and a <strong>parent</strong>, <strong>left </strong>and <strong>right </strong>child (pointers for General and AVL tree, unused for Heap tree because it is an array implementation).

<strong>1.3      Member Functions Constructors</strong>

defines constructor.

<h2>Destructor</h2>

defines destructor.

<strong>Accessors getRoot()    </strong>returns the root of the tree.

<strong>getSize()        </strong>returns number of elements in the tree. <strong>getHeight()             </strong>returns the height of the three.

<strong>getHeight(node) </strong>returns the height of the node in the argument (from the root). <strong>empty() </strong>returns true if the tree is empty, false otherwise. <strong>leaves() </strong>returns the number of leaves in the tree.

<strong>siblings(node)             </strong>returns the number of siblings of the node in the argu-

ment.

<strong>findNode(data) </strong>returns a pointer to a node that holds the data in the argument.

<em>1.3</em>

<strong>preorder()    </strong>performs preorder traversal. <strong>postorder() </strong>performs postorder traversal. <strong>inorder()       </strong>performs in order traversal.

<h2>Mutators</h2>

<strong>clear()            </strong>removes all the elements in the tree <strong>insert(data)   </strong>inserts data in the tree. <strong>del(data)       </strong>removes data from the tree.

<strong>Friends</strong>

no friends for this class.

<h1>2           Heap</h1>

In this part of the project, you need to implement an additional <em>MaxHeapTree Class</em>; create the UML diagram. Calculate the running time of your functions and include them in your report.

<h2>2.1         Description</h2>

A priority queue is like a dictionary in the sense that it stores entries (key,value). However, a dictionary is used when you want to look up a particular key. A priority queue is used when you want to prioritize entries. There is a total order defined on the keys. The main operations that a priority key allows to do are:

<ul>

 <li>Identify or remove the entry that has the smallest (largest) key. It is the only one that could be removed quickly.</li>

 <li>Insert anything you want in any time.</li>

</ul>

A binary heap is a particular implementation of the priority queue abstract data type. ‘<strong>A heap data structure should not be confused with the heap which is a common name for the pool of memory from which dynamically allocated memory is allocated</strong>’. Its definition encompasses several things:

<ul>

 <li>Identify or remove the entry that has the smallest (or largest) key. It is the only one that can be removed quickly.</li>

 <li>Insert anything you want at a more specific location in the tree.</li>

</ul>

For this part of the project you will implement a max heap and all of its operations. Entries are stored in a dynamic array. If an entry is being inserted, and the array is already full, the capacity of the array is doubled. If, after removing an entry from the heap, and the number of entries is one-quarter (1/4) the capacity of the array, then the capacity of the array is halved. The capacity of the array may not be reduced below the initially specified (by you) capacity.

<h2>2.2         Data Members</h2>

Specify all the data members your implementation needs. You are required to instantiate a <em>TreeNode </em>object for each of the nodes in the tree. Your nodes have a key (integer) and a value (Type), and they are stored in a dynamic array.

<h2>2.3             Member Functions Constructors</h2>

defines constructor.

<em>2.3</em>

<h2>Destructor</h2>

defines destructor.

<strong>Accessors getMax()     </strong>returns the root of the tree.

<strong>getSize()        </strong>returns number of elements in the tree. <strong>getHeight()             </strong>returns the height of the tree.

<strong>empty()         </strong>returns true if the tree is empty, false otherwise. <strong>leaves()    </strong>returns the number of leaves in the tree.

<strong>print()      </strong>prints the heap.

<h2>Mutators</h2>

<strong>clear()     </strong>removes all the elements in the tree

<strong>insert(key,data)            </strong>inserts data in the tree. This operation must satisfied

the heap property.

<strong>delMax()         </strong>removes the entry specified by maximum key in the tree. This

operation must satisfied the heap property.

<strong>Friends</strong>

defines friends for this class.

<h1>3           AVL Tree</h1>

In this part of the project, you need to implement an additional <em>AVL Class</em>; create the UML diagram. Calculate the running time of your functions and include them in your report.

<h2>3.1         Description</h2>

A binary search tree (BST) is a powerful tool to quickly search values in a tree. However, if the BST is not balanced its operations can degenerate to linear behavior, which makes them no faster than lists.

An AVL tree is a BST that includes complicated updating rules to keep the tree balanced. An AVL tree requires that the height of the left and right children of every node to differ by at most ± 1. Simple and double rotation are executed when inserting or deleting an entry to/from the tree.

<h2>3.2         Data Members</h2>

Specify all the data members your implementation needs. You are required to instantiate a <em>TreeNode </em>object for each of the nodes in the tree. Each node has a value (Type), and access to its parent, left and right child.

<strong>3.3      Member Functions Constructors</strong>

defines constructor.

<h2>Destructor</h2>

defines destructor.

<strong>Accessors getRoot()    </strong>returns the root of the tree.

<strong>getSize()        </strong>returns number of elements in the tree. <strong>getHeight()             </strong>returns the height of the tree.

<strong>getHeight(node) </strong>returns the height of the node in the argument (from the root). <strong>empty() </strong>returns true if the tree is empty, false otherwise. <strong>leaves() </strong>returns the number of leaves in the tree.

<em>3.3</em>

<strong>siblings(node)             </strong>returns the number of siblings of the node in the argu-

ment. <strong>find(data) </strong>returns a pointer to a node that holds the data in the argument. <strong>preorder() </strong>performs preorder traversal. <strong>postorder() </strong>performs postorder traversal. <strong>inorder() </strong>performs inorder traversal. <strong>inorder() </strong>performs inorder traversal.

<h2>Mutators</h2>

<strong>clear()     </strong>removes all the elements in the tree

<strong>insert(data) </strong>inserts data in the tree. Tree must be kept balanced after the insertion.

<strong>del(data) </strong>removes data from the tree. Tree must be kept balanced after the deletion.

<strong>Friends</strong>

defines friends for this class.

<h1>4           The Menu Program</h1>

In order to test your program, you are required to implement a menu program that provides the means to run each of the functions in your classes (name your executable proj3). Please choose the <em>string </em>data type for the values (or ’data’)

of your entries. The TA will choose one group to demo the project.

<strong>Format for the Menu Program</strong>

First, take a character, ’g’, ’h’, or ’a’ (lowercase) that specifies whether we will be working with a general tree, a heap, or an AVL tree, respectively, and creates an instance of the tree. Next, give the options for each specific tree (please have them in this <strong>EXACT </strong>order for grading purposes):

<strong>General Tree or AVL Tree</strong>

<ol>

 <li>Return root</li>

 <li>Return size</li>

 <li>Return height</li>

 <li>Return height (node)</li>

 <li>Is tree empty?</li>

 <li>Return number of leaves</li>

 <li>Return number of siblings (node)</li>

 <li>Find node (data)</li>

 <li>Print preorder</li>

 <li>Print postorder</li>

 <li>Print inorder</li>

 <li>Clear tree</li>

 <li>Insert (data)</li>

 <li>Delete (data)</li>

 <li>Exit</li>

</ol>

<strong>Max Heap</strong>

<ol>

 <li>Return root</li>

 <li>Return size</li>

 <li>Return height4. Is tree empty?</li>

 <li>Return number of leaves</li>

 <li>Print</li>

 <li>Clear tree</li>

 <li>Insert (key, data)</li>

 <li>Delete</li>

 <li>Exit</li>

</ol>