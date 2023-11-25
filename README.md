[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ux_Rl8PV)
[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/O3kA3uAf)


## Project 1
### Due date: Sunday, 12/03, @11:59pm

*Note*: This assignment requires understanding tail-recursion.
The idea of a singly-linked list doesn't have a `size` member variable. Instead of recursive *algorithms*, we can talk about recursive *data structures*. The singly-linked list is a good example: we can consider a "list" that consists of *just* each node, pointing to the rest of the list:

```java
class ListNode {

    int value = 0;
    ListNode rest = null;

    // ...

}
```

This is the *original* linked list, then called a *cons cell*, invented in 1958. The only thing you can do with this "list" is get the first element or the rest. A complete implementation of this linked list is found in `ListNode.java`. Documentation of this class is in the [ListNode Javadoc](./javadocs/ListNode.html).

This programming project asks you to write twelve tail-recursive linked list functions. The signatures of these functions are listed below; you can read more about them in the [ListFuntions JavaDoc](./javadocs/ListFunctions.html)

* <code class="prettyprint lang-java">boolean isEmpty(ListNode list)</code>
* <code class="prettyprint lang-java">int size(ListNode list)</code>
* <code class="prettyprint lang-java">int get(ListNode list, int index)</code>
* <code class="prettyprint lang-java">int indexOf(ListNode list, int element)</code>
* <code class="prettyprint lang-java">int lastIndexOf(ListNode list, int element)</code>
* <code class="prettyprint lang-java">boolean equals(ListNode list1, ListNode list2)</code>
* <code class="prettyprint lang-java">ListNode reverse(ListNode list)</code>
* <code class="prettyprint lang-java">ListNode headList(ListNode list, int n)</code>
* <code class="prettyprint lang-java">ListNode tailList(ListNode list, int n)</code>
* <code class="prettyprint lang-java">ListNode subList(ListNode list, int start, int end)</code>
* <code class="prettyprint lang-java">ListNode add(ListNode list, int element)</code>
* <code class="prettyprint lang-java">ListNode addAll(ListNode list1, ListNode list2)</code>

`ListFunctions.java` contains function stubs for each function above, although you should feel free to write additional private functions. A second file, `ListFunctionsTestUtils.java`, contains utility functions you may use for testing but which should *not* be used in your code. You can find details on those functions in the [ListFunctionsUtils Javadoc](./javadocs/ListFunctionsUtils.html).

Your submission should additionally follow the constraints below:

1. All recursive functions should be tail recursive. Not all functions require recursion, but all recursive functions must be tail-recursive - that is, whenever functions call themselves, the result must be returned directly. You cannot use non-recursive looping, such as `for`, `while`, or `goto`.
2. You are not allowed to have non-local variables (i.e., variables that exist outside of functions), nor create any arrays.
3. Your functions must run in O(n) time (or better).
4. You should not use the later functions in earlier ones. For example, the code for `addAll` can use `reverse`, but not vice versa.

