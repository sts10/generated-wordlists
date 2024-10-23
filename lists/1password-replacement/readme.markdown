# Proposed new 1Password word list

This repository contains a proposed replacement word list for the password manager 1Password. I, Sam Schlinkert, created this new word list, primarily by [scraping publicly available Google Books Ngram word frequency data](https://github.com/sts10/common_word_list_maker) and Wikipedia word data (thanks to [this project](https://github.com/IlyaSemenov/wikipedia-word-frequency/)), and then doing additional edits.

## Attributes of the new list

I'm not 100% which wordlist the 1Password app uses currently, but there is [a wordlist in this public GitHub repository](https://github.com/1Password/spg/blob/master/testdata/agwordlist.txt). The list contains 18,325 words, ranging between 3 and 8 characters. (I've seen other versions of the list that are slightly shorter, like [this 18,176-word one](https://1password.com/txt/agwordlist.txt).)

My proposed replacement list is this same length -- 18,325 words -- but includes words up to 10 characters long.

```text
List length               : 18325 words
Mean word length          : 7.12 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 10 characters (zoological)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 14.162 bits
Efficiency per character  : 1.989 bits
Mean edit distance        : 7.020
```

## Which words were removed? Which were added?

You can see a list of exact cuts and additions in this directory/repo.

Some of the words on the current 1Password list but not on the new list include: loch, avioinc, coquina, nodulose, vide, wold, quean.

## Comparing 5 random passphrases from each list

From 1Password's current list (using 1Password's online password generator):

```text
guilt-triune-illumine-gail-jonquil-habacuc
blat-natality-deerskin-bedstead-purblind-tenon
mimi-dub-eugenics-bien-populism-squid
ham-cataract-thus-pithy-pushcart-piggy
convex-bump-styled-salesmen-iniquity-troupe
```

From this new list:

```text
hunt-annuities-lots-diaries-pertains-male
gave-flask-buy-hoped-idealized-roller
converted-roofing-purged-riddle-pans-participle
flattered-apostolic-provide-devolution-plenty-lain
together-rivals-puma-loneliness-reserve-clusters
```

## Methodology

My replacement new list uses frequently used words [Google Books Ngram data](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html) and Wikipedia (found via [this project](https://github.com/sts10/wla)). 

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
- [Wikipedia Frequent Word Scraper](https://github.com/IlyaSemenov/wikipedia-word-frequency/): To get a list of words frequently appearing on Wikipedia
- [Tidy](https://github.com/sts10/tidy): A command-line utility for editing word lists that I wrote
- [Word List Analyzer](https://github.com/sts10/wla): A tool I wrote to analyze word lists (rather than edit them)

## Disclaimers

While I've attempted to remove offensive or inappropriate words from this list, I can't guarantee I've caught all of them.

Also, I make no guarantees about the security of passphrases generated with words from this list. Please check its safety yourself before using in situations that require secure passphrases.

## On licensing/usage

This project has no association with 1Password, Wikipedia, or Google, nor, to my knowledge, do any of these entities endorse this project.

See parent directory's README for more licensing information.
