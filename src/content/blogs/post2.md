---
title: "Learning CS314: Data Structures"
description: "My experience and thoughts regarding CS314: Data Structures taught at 
The University of Texas at Austin."
pubDate: "Dec 2 2023"
heroImage: "/blogs/post2/hero.png"
badge: "NEW"
tags: ["Academics"]
updatedDate: "Dec 4 2023"
---
# My thoughts #
I felt like this course was challenging but still completely doable as a student who had some decent
programming knowledge in high school but hadn't ever touched Java. The effort put into the course is
well rewarded by the knowledge you gain. This course can definitely be challenging and confusing at times
but the structure of the content and the practice material given allowed me to understand with enough
repitition. The material I learned in this course gave me a deeper understanding of Computer Science as a
whole and I feel like it adequately prepared me for future CS courses.

This course was taught by <a target="_blank" href="https://www.cs.utexas.edu/~scottm/">Mike Scott</a>, a professor who's incredibly passionate and engaging. Mike knows
how to teach the course and knows the material very well. He doesn't make the 50 minute lecture boring
at any time and is always enthusiastic about what he's teaching. He uses slideshows for notes so there's
less time taking notes and more time understanding. The only drawback with his teaching style is that he
can be a bit fast at times, moving on before many of us can comprehend the material fully. However, this 
is mostly out of his control as there is a strict schedule to stick to.

Assignments varied from trivial (data structure implementations) to extremely difficult and confusing 
(compressing algorithms). However, the assignments were thorough and helped me understand the data structures
we were learning even more. We are given a week to complete them and they took me approximately 10 to 20 hours 
to finish, including implementing, checking, and visiting office hours.

# What we covered #
Data structures are **bolded** and ideas presented are in more-or-less chronological order.
1. &nbsp;&nbsp;&nbsp;&nbsp;- Algorithm Analysis (calculating T(N) and Big-O of functions)
2. &nbsp;&nbsp;&nbsp;&nbsp;- Java Techniques and Characteristics
3. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Syntax, Encapsulation, Inheritance, 
Polymorphism, Generics, Iterators
4. &nbsp;&nbsp;&nbsp;&nbsp;- Interfaces
4. &nbsp;&nbsp;&nbsp;&nbsp;- Abstract Classes
4. &nbsp;&nbsp;&nbsp;&nbsp;- **Lists** (ArrayLists, Linked-Lists)
5. &nbsp;&nbsp;&nbsp;&nbsp;- **Maps**
6. &nbsp;&nbsp;&nbsp;&nbsp;- Recursion and Recursive Backtracking
7. &nbsp;&nbsp;&nbsp;&nbsp;- Searching and Sorting
8. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Linear, Selection, Insertion, Mergesort, 
Quicksort, Radix Sort
9. &nbsp;&nbsp;&nbsp;&nbsp;- **Stacks**
10. &nbsp;&nbsp;&nbsp;&nbsp;- **Queues** (and Priority Queues)
11. &nbsp;&nbsp;&nbsp;&nbsp;- **Binary Trees**
12. &nbsp;&nbsp;&nbsp;&nbsp;- **Binary Search Trees**
13. &nbsp;&nbsp;&nbsp;&nbsp;- **Red Black Trees**
14. &nbsp;&nbsp;&nbsp;&nbsp;- Huffman Coding (Compression Algorithm)
15. &nbsp;&nbsp;&nbsp;&nbsp;- **Graphs**
16. &nbsp;&nbsp;&nbsp;&nbsp;- **Hash Tables**
17. &nbsp;&nbsp;&nbsp;&nbsp;- **Tries**
18. &nbsp;&nbsp;&nbsp;&nbsp;- **Heaps**
19. &nbsp;&nbsp;&nbsp;&nbsp;- Dynamic Programming
20. &nbsp;&nbsp;&nbsp;&nbsp;- Functional Programming  

<br/>

# Hardest concepts in the class #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Recursive Backtracking
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Huffman's Compression Algorithm
3. &nbsp;&nbsp;&nbsp;&nbsp;3\. Conditional and dependent loop Big-O

I found recursive backtracking hard to understand because of the sheer amount of things you need
to take care of. The idea is to try different options to see if they lead to the desire outcome
but to "backtrack" if they lead to a dead end, similar to a maze. The idea is to have a base case,
like any recursion algorithm. Then the recursive step includes looping through the different choices
that the algorithm can take, for example, going up, down, left, or right in a maze. Then you need
to make that choice, either by marking it as visited or updating a variable. Then you compare that 
result with a recursive call and finally, undo the choice so that it can be potentially done at a later
step by a whole different recursive branch. The most difficult part about this was that the problems
and solutions could vary widely so there was no general solution beyond the very vague guideline I listed.

Huffman's compression algorithm was also difficult to understand because I found it to be quite extensive.
In class, we implemented Huffman's algorithm using an array to count frequencies, a priority queue to store
values and their frequencies, and then we created a curated Huffman binary tree. Then there were more steps
to encode, compress, and write the data bit-by-bit. After working on the assignment and actually implementing
it myself, it became easier to understand however.

Conditionals and dependent loops were a specific case of Big-O problems I encountered during the course and I
found them to trip me up occasionally. These problems weren't necessary difficult to understand, but rather
a contrasting pattern to calculating the Big-O for the algorithms we were given. For example, an outside loop
containing a dependent loop would usually be O(n^2) but if the dependent loop was exponential, the entire
algorithm would be O(n) rather than O(nlogn) or something similar. I found this to simply be a trial of 
pattern matching and knowing the different types of dependent loops I might seee in the course and exams.
<br/>

# Conclusion #
This class was made interesting and fun because of Mike but I also found the content to be extremely
valuable and necessary. This course can be challenging but with enough effort and determination, a 
strong grade in the course isn't unrealistic. Additionally, help and resources were readily available
and extremely easy to access. 

# Some resources #
1. &nbsp;&nbsp;&nbsp;&nbsp;- <a target="_blank" href="https://www.cs.utexas.edu/~scottm/cs314/">Course Website</a>
