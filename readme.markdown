# Generated word lists

A repository for word lists I've generated. Some lists are based on Google Ngram data, while others are based on [word frequency on Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/blob/master/results/enwiki-20190320-words-frequency.txt).

## About the word lists

**[basic.txt](lists/basic.txt)**: A long word list based on common words in Google Ngram data
```text
List length               : 18695 words
Mean word length          : 7.65 characters
Length of shortest word   : 3 characters (all)
Length of longest word    : 12 characters (conservative)
Free of prefix words      : false
Entropy per word          : 14.190 bits
Efficiency per character  : 1.855 bits
Assumed entropy per char  : 4.730 bits
Above brute force line    : false
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 7.466
Longest shared prefix     : 10
Unique character prefix   : 11

Pseudorandomly generated sample words
-------------------------------------
french culturally hastened meditation moments achieves 
declares battled strut heck allocate blooms 
legendary lakes envied bullets fern sparrows 
poisoning obliterated wrinkled monsoon ornate proteins 
lipid excite short camping pollster rigged 
```

**[1password-replacement.txt](lists/1password-replacement/1password-replacement.txt)**: A suggested replacement for [1Password](https://1password.com/)'s word list, based on common words in Google Ngram data. It has the same minimum and maximum word length as [the list 1Password was using in 2021](https://1password.com/txt/agwordlist.txt), plus adds 55 extra words. You can view lists of the words I added and removed from the 2021 1Password list in `lists/1password-replacement/` directory. See [the list's own README for more information](lists/1password-replacement/readme.markdown) on this list.
```text
List length               : 18231 words
Mean word length          : 6.36 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 8 characters (zucchini)
Free of prefix words      : false
Entropy per word          : 14.154 bits
Efficiency per character  : 2.227 bits
Assumed entropy per char  : 4.718 bits
Above brute force line    : false
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 6.188
Longest shared prefix     : 7
Unique character prefix   : 8

Pseudorandomly generated sample words
-------------------------------------
deafen kitten detain snake effigy fetching 
openings racer theistic tsunami joyous splendid 
caseload suits eaters treads outgrown dye 
gold thinner thief propose color mister 
desires corpora phantoms annex puppet squire
```

**[diceware.txt](lists/diceware.txt)**: A new list for using with diceware. Like [the EFF long list](https://www.eff.org/dice), it is free of prefix words, though it has words longer than 9 characters, unlike the EFF long list. The version in this repo has the corresponding dice rolls preceding each word, followed by a tab. 
```text
List length               : 7776 words
Mean word length          : 7.83 characters
Length of shortest word   : 4 characters (aged)
Length of longest word    : 11 characters (withholding)
Free of prefix words      : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.650 bits
Assumed entropy per char  : 3.231 bits
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 7.559
Longest shared prefix     : 10
Unique character prefix   : 11

Pseudorandomly generated sample words
-------------------------------------
policing calmly urged attractive inhabitants restless 
hated bags stretches reaching traded resisting 
arrests desktop voted directed words bluff 
ensures lodging proprietor spokesman laborers realism 
indicates scrutiny belongs managed crowds researchers
```

If you want a 7,776-word diceware list that _does_ include prefix words, there's [diceware-including-prefix.txt](lists/diceware-including-prefix.txt). Just be sure to use a character or space between words in your passphrase!

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

## Methodology

For the lists based on [Google Books Ngram data](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html), I [scraped](https://github.com/sts10/common_word_list_maker) the 2012 dataset and made a list of the most frequently appearing 100,000 words between 1975 and 2012. Then, using [a separate tool I wrote](https://github.com/sts10/tidy), I cut this list down into various sizes to create the word lists included in this repo.

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

I'll note here that at least one list in this project was derived from [this Wikipedia word frequency project](https://github.com/IlyaSemenov/wikipedia-word-frequency/), which uses the MIT license. I offer this list under the same license as the other word lists in this project.

## Related projects

As a proof-of-concept, I made some [word lists optimized for inputting on smart TVs](https://github.com/sts10/remote-words).

## Requests? Suggestions? 

Happy to make word lists given reasonable parameters! Just create an Issue.
