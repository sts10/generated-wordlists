# Proposed new 1Password word list

This repository contains a proposed replacement word list for the password manager 1Password. I, Sam Schlinkert, created this new word list, primarily by [scraping publicly available Google Books Ngram data](https://github.com/sts10/common_word_list_maker) and then doing additional edits.

I am publishing this list in hopes that AgileBits, the company that owns 1Password, wants to adopt it for 1Password's passphrase generator. 

Of course nothing is stopping others from using this list for other purposes, assuming they adhere to the attached LICENSE.

## Attributes of the new list

This new word list has the same minimum and maximum word length as the list 1Password was using in 2021 (3 and 8). My understanding is the list 1Password currently uses is 18,167 words long. This list has 18,231 words, ensuring that each word gives slightly more entropy than the current list. 

```
List length               : 18231
Mean word length          : 6.36
Length of shortest word   : 3 (ace)
Length of longest word    : 8 (zucchini)
Entropy per word          : 14.1541
```

## Which words were removed? Which were added?

You can see a list of exact cuts and additions in this directory/repo.

Some of the words on the current 1Password list but not on the new list include: loch, avioinc, coquina, nodulose, vide, wold, quean.

## Comparing 5 random passphrases from each list

From the old list (using 1Password's online password generator):

```
guilt-triune-illumine-gail-jonquil-habacuc
blat-natality-deerskin-bedstead-purblind-tenon
mimi-dub-eugenics-bien-populism-squid
ham-cataract-thus-pithy-pushcart-piggy
convex-bump-styled-salesmen-iniquity-troupe
```

From this new list: 

```
analyst-ensign-eggplant-singing-evenings-weekdays
meridian-itemized-prove-suffix-welt-skyward
quandary-layering-annexes-lard-aerial-clutter
earned-gospels-rushing-cinnamon-pressed-alerts
mishap-ruled-racism-samples-interim-flooding
```

## Methodology

This new list is based on [Google Books Ngram data](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html). [I used](https://github.com/sts10/common_word_list_maker) the 2012 dataset to compile a list of the most frequently appearing words between 1975 and 2012. Then, using [a separate tool I wrote](https://github.com/sts10/tidy), I cut this list down, removing "rare" or strange words, profane words, and words shorter than 3 characters and longer than 8 characters until it was just longer than the current 1Password list.

## Tools and resources I used to generate these word lists

- [Common Word List Maker](https://github.com/sts10/common_word_list_maker): Scrapes Google Books Ngram data to create a long word list of frequently appearing words
- [Tidy](https://github.com/sts10/tidy): A command-line utility for editing word lists

## Disclaimers

While I've attempted to remove offensive or inappropriate words from this list, I can't guarantee I've caught all of them. 

Also, I make no guarantees about the security of passphrases generated with words from this list. Please check its safety yourself before using in situations that require secure passphrases.

## On licensing/usage

The Google Books Ngram data compilation I used to construct the new word list "is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/)" ([source](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html)). This project has no association with Agile Bits/1Password or Google, nor, to my knowledge, does either company endorse this project. See LICENSE file in parent directory for more information on how this project is licensed.