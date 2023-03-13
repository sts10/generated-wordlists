# Proposed new 1Password word list

This repository contains a proposed replacement word list for the password manager 1Password. I, Sam Schlinkert, created this new word list, primarily by [scraping publicly available Google Books Ngram data](https://github.com/sts10/common_word_list_maker) and then doing additional edits.

I am publishing this list in hopes that AgileBits, the company that owns 1Password, wants to adopt it for 1Password's passphrase generator. 

Of course nothing is stopping others from using this list for other purposes, assuming they adhere to the attached LICENSE.

## Attributes of the new list

This new word list has the same minimum and maximum word length as the list 1Password was using in 2021 (3 and 8). My understanding is the list 1Password currently uses is 18,176 words long. This list has 18,197 words, ensuring that each word gives slightly more entropy than the current list. 

```
List length               : 18197 words
Mean word length          : 6.36 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 8 characters (zucchini)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 14.151 bits
Efficiency per character  : 2.226 bits
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

Thank you to the users who replied to [a Reddit post about this list](https://www.reddit.com/r/1Password/comments/ur4otq/proposed_new_word_list/) for helping me think through these notes further than I had.

### Assumed use-cases of passphrases 

Let's consider _**when**_ a password manager user might want to use a passphrase rather than a password like `96W8vaCHCR':XXj,xhJ6`. I based my work around three use-cases (loosely ranked by importance/priority): 

1. When creating a master password that the user will have to memorize and type frequently.
2. When creating an account where they'll enter the password in a situation where they can not auto-fill or copy it from a 1Password app (for example: a smart TV or computers where they don't have 1Password installed). I think of this as a case where the user needs to hold their password in their minds for a few seconds.
3. When creating an account they anticipate they may have to read the password over a voice channel.

For the first use-case, I wanted to make a list that prioritized words that were "story-able". By "story-able", I mean words that most users will be able to construct a story with. Inspired by [the "Password Strength" xkcd comic](https://xkcd.com/936/?correct=horse&battery=staple), I think users memorize passphrases by creating a little story for themselves. 

![Correct horse battery stapler comic](https://imgs.xkcd.com/comics/password_strength.png)

This guided my choice to use Google Books data -- these are words that literally make up the stories of English-speaking people. Whether certain parts of speech, like nouns, some balanced mix of parts of speech, or other categorizations of words, like singular nouns, are generally more "story-able" than others is a question to explore further.

While this "story-ability" will help with assumption #2, I argue that words that are good for holding in your mind temporarily are words that are what I'd call "mentally pronounceable" (shout-out to [Reddit user out0focus for crystallizing this for me](https://www.reddit.com/r/1Password/comments/ur4otq/comment/i8x040c/?utm_source=reddit&utm_medium=web2x&context=3)), by which I simply mean that you can hold them in your mind as a _word_ rather than a collection of letters. I think how easy a word is to spell is closely related to this -- perhaps "mental pronounceable" is the ease of "taking in" a word, and spell-ability is the ease of (re-)producing it (entering it into the interface). To make this more concrete, imagine carrying `entendre goyim ormolu waggish` (four words I'm cutting from the 1Password list) vs. `doubling striker adverbs guided` (four words I'm adding). 

Re: assumption #3, while I didn't optimize my list for (phonetically) pronounceable words, I think that the methodology I used (striving to use "common" words) works toward this goal.

## More reasons why 1Password may want to switch to this list

While the above section on use-cases presents some broad reasons this list may be attractive as a new 1Password word list, I'll touch on a few specific points here.

### The "re-roll" problem

When I [posted this list to 1Password's subreddit](https://www.reddit.com/r/1Password/comments/ur4otq/proposed_new_word_list/), a few users mentioned how, when using the current 1Password list, they would "re-roll" for a new passphrase if they got a "weird" word in their original passphrase. This has the mathematical effect of making their passphrases weaker, since it effectively shortens the word list, and thus decreases the amount of entropy each word gives. (In practice, this would necessitate an attacker to skip these uncommon words in their attacks, which doesn't seem too improbable?) It's much better to replace these "skip" words in the word list, bringing the "real-world" amount of entropy-per-word more in-line with the theoretical figure, which we can easily calculate and base security guidance on.

### Auto-correct

If a word in a passphrase is very uncommon, it may even be auto-corrected by some applications you might pasted/type it in to. `quean` may be a good example of this. (Granted, if an interface has auto-correct working, it likely is NOT a place a secure passphrase should be entered, but that's a different issue.)

## Tools and resources I used to generate these word lists

- [Common Word List Maker](https://github.com/sts10/common_word_list_maker): Scrapes Google Books Ngram data to create a long word list of frequently appearing words
- [Tidy](https://github.com/sts10/tidy): A command-line utility for editing word lists

## Disclaimers

While I've attempted to remove offensive or inappropriate words from this list, I can't guarantee I've caught all of them. 

Also, I make no guarantees about the security of passphrases generated with words from this list. Please check its safety yourself before using in situations that require secure passphrases.

## On licensing/usage

The Google Books Ngram data compilation I used to construct the new word list "is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/)" ([source](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html)). This project has no association with Agile Bits/1Password or Google, nor, to my knowledge, does either company endorse this project. See LICENSE file in parent directory for more information on how this project is licensed.
