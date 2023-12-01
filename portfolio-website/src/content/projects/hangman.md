---
title: "Evil Hangman"
description: "An altered version of the famous traditional game of Hangman."
heroImage: "/projects/hangman/hero.png"
pubDate: "Sep 1 2023"
badge: ""
tags: ["Java"]
code: ""
demo: ""
blog: ""
---
# Overview #
An altered version of the famous traditional game of Hangman. In this "evil" version,
the chosen word to be guessed is undetermined for as long as possible until the
player ultimately narrows the list of possible words to just a single word. This project
was done as a school assignment so code cannot be published.

# Purpose #
This project was used to understand data structures such as lists, maps, and sets.

# How it works #
<br/>
<center>
    <img src="/projects/hangman/test.png" alt="Word families in evil hangman" width="300" height="150">
    <p class="caption">Debugging the program by analyzing word families</p>
</center>

The program uses a set of known English words or a dictionary. This dictionary determines
what constitutes a word. Like a traditional Hangman game, the word length needs to be 
inputted by the player. This given word length trims down the entire dictionary just to 
words that are of the given word length (ex: cat is not a possible solution to _ _ _ _ _).

As the player makes a guess, the program creates "word families" which are essentially 
groups of words that match the same character pattern. This information is stored in a 
map, mapping a String (pattern) to an ArrayList of Strings (list of possible words). 
An example of the word familiy of "_ a _" and "p _ _" is:

| _ a _ : | p _ _ : |
| :-----: | :-----: |
| bar     | put     |
| far     | par     |
| car     | poe     |
|         | pie     |

Obviously, an actual word family would be dozens of words that match that pattern. With 
these word families, we have a way of determining which word family is "harder" than another. 
Most intuitively, this is based on the number of words within that family as there are more 
possible words the guess can be. In reality, this method of determining difficulty isn't always 
accurate.  

Now we have a map of word families that are possible from the given guess and we can set the 
pattern shown to the player to the pattern of the "hardest" word family, or the word family
with the most number of words in it. More often than not, the largest word family pattern is 
an empty pattern with no letterns filled in, resulting in a wrong guess shown to the player.

With each guess, new word families are regenerated based on the current pattern and the new 
guess. As the program selects a new word familiy, the dictionary of possible words that can be
picked by the program to be the right answer slowly narrows down. Once it reaches a point where
the dictionary is only one word, only one word family is generated and it's the only one to be 
picked to be the new pattern. Using these word families are essentially how the program "holds
off of picking a definite word" to be the right answer, as the right answer can be any word within the 
dictionary of possible words. 

To add further nuance, the Evil Hangman game was given a difficulty level to be selected by the 
player. At hard difficulty, the largest word family was always chosen; at medium, the second largest
word family was chosen on every 4th guess; at easy, the second largest word family was chosen on 
every other guess. This required the word families to be sorted by the size of the word family,
making this part of the game scalable and easily changed. 

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Exchanging data between data structures
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Sorting the word families by difficulty

One of the hardest parts about this assignment was navigating between the different data structures
used to store all the information required by the game. I found it hard to keep track of the 
different syntax, methods, and characteristics between the data structures. One of the more common
annoyances was the inability to iterate through a map, instead needing to create a key set to
go through the map. 

Another difficult part about the assignment was implementing the nuance of allowing various difficulties.
This required the word families to be sorted but this proved to be difficult as it was my first time
implementing a Comparator class for the word families. If there were ties between word families due to
having the same number of words, they were to be broken by least letters revealed and lexicographical ordering.

# Full Tech Stack #  
|            | Languages |           | Tools      |
| :--------- | :-------- | :-------- | :--------- |
|            | - Java    |           | - Intellij |
|            |           |           |            |
|            |           |           |            |
|            |           |           |            |
