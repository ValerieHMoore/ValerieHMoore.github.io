---
layout: post
title:      "Pseudocoding: In Your Own Words"
date:       2019-07-06 14:27:01 +0000
permalink:  pseudocoding_in_your_own_words
---


As a Technical Coach for Flatiron School’s Software Engineering programs, I help students debug and solve coding challenges in Ruby, Rails, SQL, JavaScript, React, Redux, and HTML/CSS. A common mistake I see is that students try to write code without really understanding it. They read about methods in the lessons, and just use trial and error to implement them, getting more frustrated as they go.

When I encounter a student with this situation, I ask them to describe to me in words, not code, what they’re trying to do. I ask a) what *should* be happening? and b) what’s happening instead? This is called Rubber Duck debugging, or explaining your code to a non-technical person or object. My rubber duck happens to resemble an [opera star](https://renepape.com/en/papeduck/), but you can also talk to your dog, your grandmother, or your favorite presidential hopeful.

After you’ve clearly stated your problem out loud, write it down in those plain words. Type it right into your method as a comment. This is called pseudocode or pseudocoding. When you are pseudocoding, things start to make sense. Then you can think of ways to change those clear words into clear code. Or, worst case, you now have a phrase you can Google.

If you find you can’t put it into your own words, copy the test or project requirement as a comment right into the method you’re trying to write. Then write each piece step by step. If you’re still stuck, you may need clarification on the instructions or specs. 

## Example
Here are the instructions: “You will write a program that, given a word and a list of possible anagrams, selects the correct one(s).” Some students don’t know what an anagram is, so step 1 is to Google that: “An anagram is a word, phrase, or name formed by rearranging the letters of another, such as cinema, formed from iceman.” 

## Rubber Ducking
“![Mr. Duck](https://celebriducks.com/), I need to compare two words to see if they have the same letters in a different order. If the letters were tiles from Words With Friends, I would just rearrange them. I would put the letters in alphabetical order and compare them.”

## Pseudocode
Take the word apart into letters and sort them, then put them back together. Google: “ruby how to sort the letters in a word alphabetically.” That led me to this link: https://stackoverflow.com/questions/9464065/how-to-sort-a-strings-characters-alphabetically. The top-voted answer to this question has the following code snippet: str.chars.sort.join. *Aha!* Let’s look at the instructions one more time: turns out there’s a good hint in there! “You will write a program that, given a word and a list of possible anagrams, *selects* the correct one(s).”

And here is the final answer:

```
def match(word_array)
    @word = @word.chars.sort.join	
    word_array.select {|word| word.chars.sort.join == @word}
 end
```


Happy pseudocoding!




