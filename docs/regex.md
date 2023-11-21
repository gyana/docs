# Regular expressions reference

How to search, extract and replace text in Gyana.

Regular expressions (or "regex") are a system for working with text data.

If you've hit the limitations of functions like `substitute`, `upper` or `strip`, you might find regular expressions useful. Think of it like advanced search and replace.

💡 There is a learning curve, but you'll unlock the ability to do pretty much anything you can imagine with text, and maybe even save the day.

In this guide, we'll give you a brief overview of how regular expressions work (with links), and show you how use the Gyana functions `regex_extract`, `regex_replace` `regex_search`.

## Regular expressions

Suppose you have the sentence "**The quick brown fox jumps over the lazy dog**", and you wanted to replace all occurrences of the word "**dog**" with "**cat**". You can do that with a standard search and replace, e.g. using the `substitute` function.

But now suppose you wanted to replace "**all words that start with 'd'**" with "**cat**". Standard search replace won't work, because there are lots of words that start with 'd'.

That's where we need a regular expression. A regular expression is how we describe something like "**all words that start with 'd'**", in a way a computer can understand. It's a language for describing patterns in text, which the computer will then go and search for.

In this case, the regular expression we want is `\sd[a-z]`+. Here's why:

*   `\s` matches a space (typically before a new word)
    
*   `d` matches the letter **d**
    
*   `[a-z]+` matches a string of lowercase letters one or more times
    

Taken together, the computer will look for "a **space,** followed by a **d**, followed by **one or more lowercase letters**" - which is the same as saying "**all words that start with 'd'**".

Designing a regex for your specific problem will take a few minutes of trial and error. Here are a few resources we recommend:

*   A guide for learning regex at RegexOne
    
*   Regex101, an interactive editor where you can prototype your regex
    
*   A syntax reference for re2, the regex engine used by Gyana
    

## Regex functions

Now that we've covered the basics, here's how to think about the regex functions in Gyana.

`regex_search` will return true if the text matches the regex pattern. Primarily useful for filtering data, e.g. to filter out records that contain a valid zip code or email address.

`regex_extract` will extract the specific piece of text in the regex pattern. This is great for cleaning data, e.g. extracting emails or phone numbers. Since a regex can have multiple matches, you use the `index` argument to decide which match to keep (e.g. first, second, ...).

`regex_replace` will replace the matched text with a replacement you define - think of it as advanced search and replace. If you want to refer to the original text in your replacement, use `\0` - for example, if the matched text is `dog` and the replacement is `\0s`, the final result is `dogs`.

If you ever get stuck, bear in mind that even seasoned programmers get tripped up by regex - you're not alone! If you have any issues, just reach out via the support.