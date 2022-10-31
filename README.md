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
> BOB_DROVE_HOME.


We, humans, identify some elements from English grammar and American culture:
  - Subject (BOB)
  - Punctuation (blank space)
  - Verb (DRIVE)
  - Punctuation (blank space)
  - Object (HOME)
  - Punctuation (.)  

Now, imagine that instead of having the full sentence upfront, you are giving one character per turn. Let's do a lexical analysis, shall we?
> **B** - Doesn't mean anything  
> **BO** - Doesn't mean anything  
> **BOB** - Doesn't mean anything  
> **BOB_**  - Wait! This is a blank space, meaning that we finish a word and a new one is about to start. **BOB** is a common name so we can mark it as the subject. Plus, a blank space is a punctuation. It's a good idea to keep a record of these elements
| Element         | Type     |
|--------------|-----------|
| BOB |   Subject   |
| blank space      | Punctuation |

> **BOB_D** 


## Syntax analysis
Coming soon.


## Semantic analysis
Coming soon.
