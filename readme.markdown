# Generated word lists

A repository for word lists I've generated. 

## About the word lists

`lists/basic.txt`: A long word list using common English words [based on Google Ngram data](https://github.com/sts10/common_word_list_maker).
```text
List length               : 18209
Mean word length          : 7.69
Length of shortest word   : 4 (ably)
Length of longest word    : 11 (worshipping)
Free of prefix words      : false
Entropy per word          : 14.1524
Assumed entropy per letter: 3.5381
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Longest shared prefix     : 10
Unique character prefix   : 11
```

`lists/1password-replacement.txt`: A suggested replacement for 1Password's word list.
```text
List length               : 18123
Mean word length          : 6.34
Length of shortest word   : 3 (ace)
Length of longest word    : 8 (zucchini)
Free of prefix words      : false
Entropy per word          : 14.1455
Assumed entropy per letter: 4.7152
Above brute force line    : false
Above Shannon line        : false
Shortest edit distance    : 1
Longest shared prefix     : 7
Unique character prefix   : 8
```

`lists/diceware.txt`: A new list for using with diceware. Like [the EFF long list](https://www.eff.org/dice), it is free of prefix words.
```text
List length               : 7776
Mean word length          : 6.93
Length of shortest word   : 5 (aback)
Length of longest word    : 9 (yesterday)
Free of prefix words      : true
Entropy per word          : 12.9248
Assumed entropy per letter: 2.5850
Above brute force line    : true
Above Shannon line        : true
Shortest edit distance    : 1
Longest shared prefix     : 4
Unique character prefix   : 5
```

## Tools I use to generate word lists

- [Common Word List Maker](https://github.com/sts10/common_word_list_maker): Scrapes Google Books Ngram data to create a long word list 
- [Tidy](https://github.com/sts10/tidy): A command-line utility for editing word lists. Also print attributes of word lists, such as those printed above.
- [Homophones](https://github.com/sts10/homophones/tree/main/homophone-lists): A list of English homophones, and method for producing more lists of English homophones

## On licensing/usage

This project and its word lists are licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/). See LICENSE file for more information.

The words for most or all of these generated word lists come from Google Books Ngram data. This data compilation "is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/)" ([source](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html)). This project has no association with Google, nor does Google endorse this project. [More information at the original project's repo](https://github.com/sts10/common_word_list_maker).

## Requests? Suggestions? 

Happy to make word lists given reasonable parameters! Just create an Issue.
