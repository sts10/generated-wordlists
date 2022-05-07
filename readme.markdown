# Generated word lists

A repository for word lists I've generated. Some lists are based on Google Ngram data, while others are based on [word frequency on Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/blob/master/results/enwiki-20190320-words-frequency.txt).

## About the word lists

**[basic.txt](lists/basic.txt)**: A long word list based on common words in Google Ngram data
```text
List length               : 18652
Mean word length          : 7.66
Length of shortest word   : 3 (can)
Length of longest word    : 11 (worshipping)
Free of prefix words      : false
Entropy per word          : 14.1870
Assumed entropy per letter: 4.7290
Above brute force line    : false
Above Shannon line        : false
Shortest edit distance    : 1
Longest shared prefix     : 10
Unique character prefix   : 11
```

**[1password-replacement.txt](lists/1password-replacement.txt)**: A suggested replacement for [1Password](https://1password.com/)'s word list, based on common words in Google Ngram data. It has the same minimum and maximum word length, though has 207 more words than [the list 1Password was using in 2021](https://1password.com/txt/agwordlist.txt).
```text
List length               : 18383
Mean word length          : 6.35
Length of shortest word   : 3 (ace)
Length of longest word    : 8 (zucchini)
Free of prefix words      : false
Entropy per word          : 14.1661
Assumed entropy per letter: 4.7220
Above brute force line    : false
Above Shannon line        : false
Shortest edit distance    : 1
Longest shared prefix     : 7
Unique character prefix   : 8
```

**[diceware.txt](lists/diceware.txt)**: A new list for using with diceware. Like [the EFF long list](https://www.eff.org/dice), it is free of prefix words, though it has words longer than 9 characters, unlike the EFF long list. The version in this repo has the corresponding dice rolls preceding each word, followed by a tab. 
```text
List length               : 7776
Mean word length          : 7.83
Length of shortest word   : 4 (aged)
Length of longest word    : 11 (withholding)
Free of prefix words      : true
Entropy per word          : 12.9248
Assumed entropy per letter: 3.2312
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Longest shared prefix     : 10
Unique character prefix   : 11
```

**[short.txt](lists/short.txt)** is a short list with words that have unique three-character prefixes and the shortest edit distance between any two words is 3 characters. It's also free of prefix words. These attributes of the list are meant to emulate [the EFF short lists](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases).
```text
List length               : 1030
Mean word length          : 8.46
Length of shortest word   : 5 (yusuf)
Length of longest word    : 12 (totalitarian)
Free of prefix words      : true
Entropy per word          : 10.0084
Assumed entropy per letter: 2.0017
Above brute force line    : true
Above Shannon line        : true
Shortest edit distance    : 3
Longest shared prefix     : 2
Unique character prefix   : 3
```

**[wikilist.txt](lists/wikilist.txt)** is based on [word frequency from Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/blob/master/results/enwiki-20190320-words-frequency.txt) rather than Google Ngram data. (Thanks to [Aaron Toponce](https://fosstodon.org/@atoponce) for pointing me to this list.)
```text
List length               : 17511
Mean word length          : 7.30
Length of shortest word   : 3 (ace)
Length of longest word    : 11 (worshippers)
Free of prefix words      : false
Entropy per word          : 14.0960
Assumed entropy per letter: 4.6987
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Longest shared prefix     : 10
Unique character prefix   : 11
```

## Tools and resources I used to generate these word lists

- [Common Word List Maker](https://github.com/sts10/common_word_list_maker): Scrapes Google Books Ngram data to create a long word list
- [Tidy](https://github.com/sts10/tidy): A command-line utility for editing word lists. Can also print notable attributes of word lists, such as those printed above.
- [Homophones](https://github.com/sts10/homophones/tree/main/homophone-lists): A list of English homophones, and a method for producing more lists of English homophones
- This study of [word frequency on Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/).

## Disclaimers

While I've attempted to remove offensive words from these lists, since I haven't checked them by hand there may be some left. Apologies! Feel free to create an Issue or Pull Request removing the offensive word(s).

Also, I make no guarantees about the security of passphrases using these lists. Please check their safety yourself before using in situations that require secure passphrases.

## On licensing/usage

This project and its word lists are licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/). See LICENSE file for more information.

The words for some of these generated word lists come from Google Books Ngram data. This data compilation "is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/)" ([source](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html)). This project has no association with Google, nor does Google endorse this project. [More information available at the original project's repo](https://github.com/sts10/common_word_list_maker).

Other lists come from [this Wikipedia word frequency project](https://github.com/IlyaSemenov/wikipedia-word-frequency/), which uses the MIT license. I'm not sure where that leaves my lists that use those results as their corpus, legally speaking! 

## Requests? Suggestions? 

Happy to make word lists given reasonable parameters! Just create an Issue.
