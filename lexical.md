![Compilers for humans](https://github.com/anderson-joyle/compilers-for-humans/blob/main/cover.png)

# Lexical analysis
Wikipedia says:
> The process of converting a sequence of characters into a sequence of lexical tokens (strings with an assigned and thus identified meaning).


Let's take the following sentence (underscore char represents a blank space):
> BOB_DROVE_HOME.

We, humans, identify some elements from English grammar and American culture. Now, imagine that instead of having the full sentence upfront, you are giving one character per turn. Let's do a lexical analysis, shall we?
> **B** - Doesn't mean anything.  
> **BO** - Doesn't mean anything.  
> **BOB** - Doesn't mean anything.  
> **BOB_**  - Wait! This is a blank space, meaning that we finish a word and a new one is about to start. **BOB** is a common name so we can mark it as the subject. Plus, a blank space is a punctuation.  

Moving forward:  
> **D** - Doesn't mean anything.  
> **DR** - Doesn't mean anything.  
> **DRO** - Doesn't mean anything.  
> **DROV** - Doesn't mean anything.  
> **DROVE** - Doesn't mean anything.  
> **DROVE_** - Wait! This is a blank space, meaning that we finish a word and a new one is about to start. **DROVE** is a known word and we can mark it as a verb. Plus, a blank space is a punctuation.  

Moving forward:  
> **H** - Doesn't mean anything.  
> **HO** - Doesn't mean anything.  
> **HOM** - Doesn't mean anything.  
> **HOME** - Doesn't mean anything.  
> **.** - Wait! This is a period, meaning that we've reached the end of the sentence. **HOME** is a known word and we can mark it as a object. Plus, a period is a punctuation.  

If we organize the results in a table-like structure, it would be something like the following:  
  - Subject (BOB)
  - Punctuation (blank space)
  - Verb (DRIVE)
  - Punctuation (blank space)
  - Object (HOME)
  - Punctuation (.)  

We just performed a basic lexical analysis, or in another words, TOKENIZATION. The product of this analysis is a list with all tokens found in the input sentence, categorized by each of their types (subject, punctuation, etc).  

Note that at this phase we are not concerned if there is any grammar error or any unknown word or punctuation. Tokenization job is simply to split the sentence into tokens, categorize them, and nothing more!  

If we take the previous sentence, add an unknown word to and perform the lexical analysis again, we would end up with the following list:  
  - Subject (BOB)
  - Punctuation (blank space)
  - **Unknown (ABCDEF)**
  - Punctuation (blank space)
  - Object (HOME)
  - Punctuation (.)  


## Power Fx syntax analysis
To be continued...
