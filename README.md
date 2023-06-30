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

# Lexical analysis
Wikipedia says:
> The process of converting a sequence of characters into a sequence of lexical tokens (strings with an assigned and thus identified meaning).


Let's take the following sentence (underscore char represents a blank space):
> BOB_DROVE_HOME.

We, humans, identify some elements of English grammar and American culture. Now, imagine that instead of having the full sentence upfront, you are giving one character per turn. Let's do a lexical analysis, shall we?
> **B** - Doesn't mean anything.  
> **BO** - Doesn't mean anything.  
> **BOB** - Doesn't mean anything.  
> **BOB_**  - Wait! This is a blank space, meaning that we finish a word and a new one is about to start. **BOB** is a common name so we can mark it as the subject. Plus, a blank space is punctuation.  

Moving forward:  
> **D** - Doesn't mean anything.  
> **DR** - Doesn't mean anything.  
> **DRO** - Doesn't mean anything.  
> **DROV** - Doesn't mean anything.  
> **DROVE** - Doesn't mean anything.  
> **DROVE_** - Wait! This is a blank space, meaning that we finish a word and a new one is about to start. **DROVE** is a known word and we can mark it as a verb. Plus, a blank space is punctuation.  

Moving forward:  
> **H** - Doesn't mean anything.  
> **HO** - Doesn't mean anything.  
> **HOM** - Doesn't mean anything.  
> **HOME** - Doesn't mean anything.  
> **.** - Wait! This is a period, meaning that we've reached the end of the sentence. **HOME** is a known word and we can mark it as an object. Plus, a period is punctuation.  

If we organize the results in a table-like structure, it would be something like the following:  
  - Subject (BOB)
  - Punctuation (blank space)
  - Verb (DRIVE)
  - Punctuation (blank space)
  - Object (HOME)
  - Punctuation (.)  

We just performed a basic lexical analysis, or in other words, TOKENIZATION. The product of this analysis is a list with all tokens found in the input sentence, categorized by each of their types (subject, punctuation, etc).  

Note that at this phase we are not concerned if there is any grammar error or any unknown word or punctuation. The tokenization job is simply to split the sentence into tokens, categorize them, and nothing more!  

If we take the previous sentence, add an unknown word to it and perform the lexical analysis again, we would end up with the following list:  
  - Subject (BOB)
  - Punctuation (blank space)
  - **Unknown (ABCDEF)**
  - Punctuation (blank space)
  - Object (HOME)
  - Punctuation (.)  

## Syntax analysis
Coming soon.


## Semantic analysis
Coming soon.
