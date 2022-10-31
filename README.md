![Compilers for humans](https://github.com/anderson-joyle/compilers-for-humans/blob/main/cover.png)

### An ultra-simplified explanation  :thumbsup:

***
<i>Primarily written for my own benefit, but hopefully helpful to someone else as well. Here I try to make them stick in to your mind (and maybe mine) by explaining them in the simplest way possible. Contributions are always welcome.</i>
***

## Table of content

- [Introduction](#introduction)
- [Lexical analysis](#lexical-analysis)
- [Syntax analysis](#syntax-analysis)
- [Semantic analysis](#semantic-analysis)

## Introduction
A programmer is just a tool that converts caffeine into code. A compiler is just a tool that converts code into machine language.

Wikipedia says:
> A compiler is a computer program that translates computer code written in one programming language (the source language) into another language (the target language)

This article will use [Power Fx](https://github.com/microsoft/Power-Fx) (open-source language written in C#) as a practical example of how compilers work and their common phases.

## Lexical analysis
Wikipedia says:
> The process of converting a sequence of characters into a sequence of lexical tokens (strings with an assigned and thus identified meaning).


Let's take the following sentence (underscore char represents a blank space):
> Bob_drove_home.


We, humans, identify some elements from English grammar and American culture:
  - Subject (Bob)
  - Punctuation (blank space)
  - Verb (drive)
  - Punctuation (blank space)
  - Object (home)
  - Punctuation (.)  

Now, imagine that instead of having the full sentence upfront, you are giving one character per turn:
> B  
> Bo  
> Bob  
> Bob_  
> Bob_d  
> ...  
> Bob_drove_home.


## Syntax analysis
Coming soon.


## Semantic analysis
Coming soon.
