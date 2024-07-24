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


Let's take the following sentence:
> BOB DROVE HOME.

We, humans, identify some elements of English grammar and American culture. Now, imagine that instead of having the full sentence upfront, you are reading one character per turn. Let's do a lexical analysis:
> **B** - Doesn't mean anything.  
> **BO** - Doesn't mean anything.  
> **BOB** - Doesn't mean anything.  
> **BOB **  - Wait! This is a blank space, meaning we finish a word. **BOB** is a word. Plus, a blank space is punctuation.  

Moving forward:  
> **D** - Doesn't mean anything.  
> **DR** - Doesn't mean anything.  
> **DRO** - Doesn't mean anything.  
> **DROV** - Doesn't mean anything.  
> **DROVE** - Doesn't mean anything.  
> **DROVE ** - Wait! This is a blank space, meaning that we finish a word. **DROVE** is a word. Plus, a blank space is punctuation.  

Moving forward:  
> **H** - Doesn't mean anything.  
> **HO** - Doesn't mean anything.  
> **HOM** - Doesn't mean anything.  
> **HOME** - Doesn't mean anything.  
> **HOME.** - Wait! This is a period, meaning that we finish a word. **HOME** is a word. Plus, a period is punctuation.  

If we organize the results in a table-like structure, it would be something like the following:  

| Token         | Kind        |
|---------------|-------------|
| BOB           | Word        | 
| (blank space) | Punctuation |
| DRIVE         | Word        |
| (blank space  | Punctuation |
| HOME          | Word        |
| .             | Punctuation |


We just performed a basic lexical analysis, or in other words, TOKENIZATION. The product of this analysis is a list containing all tokens found in the input sentence, categorized by each of their types (word, punctuation, etc).  

Note that at this phase we don't care if there is any grammar error or if a word is unknown. The tokenization job is simply to split the sentence into tokens, categorize them, and nothing more.  

  

Now, let's move on to a real-world scenario.  
`Abs(-10)` is a valid [Power Fx](https://github.com/microsoft/Power-Fx) expression. We can tokenize it by calling the following code:
```
using Microsoft.PowerFx;

var engine = new Engine();
var tokens = engine.Tokenize("Abs(-10)");
```

The result will be a similar table as the example above:  
| Token | Kind       |
|-------|------------|
| Abs   | Ident      | 
| (     | ParenOpen  |
| -     | Sub        |
| 10    | DecLit     |
| )     | ParenClose |


## Syntax analysis
Coming soon.


## Semantic analysis
Coming soon.
