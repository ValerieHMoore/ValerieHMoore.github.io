---
layout: post
title:      "Here's the Culprit: Ruby Debugging"
date:       2019-07-13 09:10:22 -0400
permalink:  heres_the_culprit_ruby_debugging
---


Here on “Ask a Question,” Flatiron School’s chat/screen share support tool for students struggling with their code, we frequently see certain types of errors. Here are some common Ruby problems and how to solve them.

## Syntax Errors
Nothing will work, and you won’t even be able to use debugging tools effectively, if you have a syntax error or several syntax errors. Does every `do` have an `end`? Review your if/else statements; do you have an `else` without an `if`, or an `if` without an `end`? Do you have extra `end`s in other methods, or at the bottom of the file you are working in? Indent your code properly for easy debugging; in the example below, each `end` is lined up with its corresponding `if` or `do`:

```
def num_points_scored(name)
  game_hash.each do |location, team_data|
    team_data[:players].each do |player_name, player_data|
      if name == player_name
        return player_data[:points]
      end
    end
  end
end
```


## Loops
Is your code stuck in an infinite loop? Or conversely, did you accidentally put a return *inside* your loop instead of *after* you have finished iterating over every item in an array? A return inside a loop will stop the loop. Notice how far down the return is in the following method. You could insert a binding.pry here and move it around to see what you are getting in different locations in your code before finally settling on a location for the return.

```
def team_names
  names_array = []
  game_hash.each do |location, team_data|
    team_data.each do |key, value|
      if key == :team_name
        names_array << value
      end
    end
  end
  return names_array
end
```


## Equals vs. Comparison
Using the code example above, if you are defining a variable, you use one equals sign, such as `names_array = []`. If you are trying to compare something, you use a double equals sign, such as `if key == :team_name`. Often students will try to use a single equals sign when making a comparison. If you are trying to compare two things, you need two equals signs.

## Data Types
Pay attention to the type of data you are working with. [Array](https://ruby-doc.org/core-2.4.1/Array.html) methods  such as `collect` and `push` can’t be used on a [string](https://ruby-doc.org/core-2.4.0/String.html) or a [hash](https://ruby-doc.org/core-2.5.1/Hash.html). If you are not sure what type of data you are working with, check the data that’s being passed into your method, or use a binding.pry to inspect it.

## Conclusion
Even experienced coders make these errors. If everything *should* work, but it doesn’t, check for these common culprits, and you may have your answer.








