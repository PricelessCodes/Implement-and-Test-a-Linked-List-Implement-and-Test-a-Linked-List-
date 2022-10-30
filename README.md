# Implement-and-Test-a-Linked-List-Implement-and-Test-a-Linked-List-
Data Structures and Performance University of California San Diego Course from Coursera.

Programming Assignment Part 1: Implement a Linked List

Assignment and Submission Details

Your submission of this assignment is divided into two parts: your code which implements a Linked List (MyLinkedList.java) and your code to test a Linked List implementation (MyLinkedListTester.java). You will submit a separate file for each part, as described below, but our guidelines for this project will more closely reflect how you will develop a project in industry.  We strongly recommend you write your tests as you write your implementation (and vice-versa). 

Step 1: Implement and test creating a Linked List Object, adding elements, and retrieving elements.
To get started, you need to decide if you wish to use sentinel nodes (like we've seen in the videos) or skip sentinel nodes.  We encourage you to use sentinels but either choice is okay. 

1. A.  Review the tester methods provided in MyLinkedListTester.java:

In the file MyLinkedListTester.java, review the setup() and fairly robust testGet() methods in MyLinkedListTester.java. We also provide the beginning of the testRemove method, with the tests from the concept challenge video.  These tests give you an idea of how your Linked List constructor, add method, and get method should perform, as well as a start on the tests for remove.  You can run them in JUnit by running the MyLinkedListTester.java file.  It should automatically run as a JUnit test suite.

1. B. Author the following methods in MyLinkedList.java:

public MyLinkedList()

This constructor should create the Linked List and setup any instance variables as needed.

public E get(int index)

This method returns the node in the list corresponding to the index. For example, if the list has the elements 6 and 9 (in that order) and you call "get" with index 0, you should get back 6. If the method is called with an invalid index (say -1 or 2 in the example above), you will thrown an IndexOutOfBoundsException.

public boolean add( E element )

This method adds an element to the end of the list. Null elements are not allowed in the list so if someone tries to insert one you should throw a NullPointerException.  Be sure to think about what happens when you add an element to an empty list as well as a list with already existing elements.  Drawing a picture of the list will help!

1.C. Run existing JUnit Tests by Running MyLinkedListTester

Run "MyLinkedListTester" and if your methods are working, you should get no errors or failures for testGet.  The rest of the tests are empty except for testRemove, which will fail.  If this bothers you, you can comment out the body of the testRemove method for now (just remember to put it back in the next part).  If you have no errors in testGet, your get method method is likely working correctly.  You will write tests to make sure your add method is working correctly in the next step.  

 1.D. Author the "testAddEnd"  and "testAddAtIndex" methods in MyLinkedListTester

The tests for "testGet" may not properly stress the add method.  To be sure your add method works properly, you should add tests to these two methods.

Important note about all Linked List test cases: We want you to test real use cases of your list, but please don't go overboard with the size of the lists you create in your tests.  Testing on lists on the order of tens or hundreds of elements is fine, but don't test on lists that contain thousands or millions of elements.  Because we're using Java, what works for a small list will almost certainly also work for a very large list, within the limits of Java itself.  Also keep in mind that most linked list operations are O(n) so tests on very large lists will take a very long time to run and risk breaking the grader.

Step 2: Implement and write tests for the remaining methods in MyLinkedList.

As we did in Step 1 above, you'll want to continue implementing and testing your MyLinkedList class.  To do so, add and test the methods below in the ordering of your choice.  You also must add JUnit tests the the MyLinkedListTester class to thoroughly test each method.  You will be graded not only on the correctness of your implementation, but also on the completeness of your tests.

To facilitate auto-grading, you need to read the method descriptions carefully to ensure they have the correct behavior.  Also, make sure you are consistent with our test cases/examples in the main method.  But, you have the freedom to implement the doubly-linked list with, or without, a sentinel head and tail node.  Our videos detail how to do this with the sentinel nodes, but feel free to omit the sentinels for extra challenge.

public int size()

This method returns the size of the list.  Be careful to update your size instance variable when adding and removing elements.  To test this method, use the method in MyLinkedListTester called testSize

public void add(int index, E element) 

This method adds an element at the specified index.  If elements exist at that index, you will move elements at that index (and beyond) up, effectively inserting this element at that location in the list. Null elements are not allowed in the list so if someone tries to insert one you should throw a NullPointerException.Although drawings are helpful for implementing any method, you will benefit heavily from drawing out what should happen in this method before trying to code it.  You will want to throw an IndexOutOfBoundsException if the index provided is not reasonable for inserting an element.  Optional:  After authoring this version of the add method, you could consider removing redundant code by having the add method you originally wrote just call this method.  To test this method, use the method in MyLinkedListTester called testAddAtIndex.

public E remove(int index) 

This method removes an element from that location.  Similar to the "add" method, we strongly encourage you to draw this out before trying to code it.  Like the "get" method, you will want to thrown an IndexOutOfBoundsException if the index provided is out of bounds. To test this method, use the method in MyLinkedListTester called testRemove.

public E set(int index, E element)

This method allows you to change elements in place by specifying a valid index of an existing element and a new value to change that element to. You should return the old value held at that index. Like the "get" method, you will want to thrown an IndexOutOfBoundsException if the index provided is out of bounds. In addition, if someone tries to set a node with a null element, you should throw a NullPointerException.  To test this method, use the method in MyLinkedListTester called testSet.

Hints: Potentially Useful (but not required) Methods

public String toString()

Although not included in the required methods for this class, you may find a "toString" method for the list and/or a "toString" method for each node helpful when testing and debugging.

Additional Constructor for LLNode

You may find yourself doing the same operations multiple time in the MyLinkedList class.  If so, you may want to consider a constructor that takes not only the element, but the previous and (possibly) next nodes.
