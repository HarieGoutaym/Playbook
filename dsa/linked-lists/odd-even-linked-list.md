# Odd Even Linked List (LeetCode 328)

## Date

21 July 2026

## What I understood

* Odd and even refer to the **position** of the node, not its value.
* We don't create new nodes; we only change the `next` pointers.
* The clean solution uses two pointers:

  * `odd`
  * `even`
* Save the first even node (`evenHead`) so it can be attached at the end.

## My first idea

I tried making two separate lists using:

* oddHead
* oddTail
* evenHead
* evenTail
* p

It worked in my head, but I kept getting `None` errors and forgot to move some pointers.

## Mistakes I made

* Forgot to update the tail after connecting a node.
* Used `p.next` when `p` was `None`.
* Forgot to connect the odd list with the even list at the end.

## Final idea

Instead of using another pointer, keep moving the `odd` and `even` pointers.

At the end:

* Connect the odd list to `evenHead`.
* Return `head`.

## Complexity

* Time: O(n)
* Space: O(1)

## Remember

Before writing code, draw the linked list and trace the pointers once. It makes the solution much easier to understand.
