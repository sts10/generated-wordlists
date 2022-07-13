# Generated word lists

A repository for word lists I've generated. Some lists are based on Google Ngram data, while others are based on [word frequency on Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/blob/master/results/enwiki-20190320-words-frequency.txt).

## About the word lists

<details>
<summary><h3>Basic List: A long word list based on common words in Google Ngram data</h3></summary>

**[basic.txt](lists/basic.txt)**

```text
List length               : 18694 words
Mean word length          : 7.65 characters
Length of shortest word   : 3 characters (all)
Length of longest word    : 12 characters (conservative)
Free of prefix words      : false
Free of suffix words      : false
Entropy per word          : 14.190 bits
Efficiency per character  : 1.855 bits
Assumed entropy per char  : 4.730 bits
Above brute force line    : false
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 7.466
Longest shared prefix     : 10
Unique character prefix   : 11

Pseudorandomly generated sample passphrases
-------------------------------------------
constables stipulate emery combined office mythology 
result drama ancillary catalytic legends stew 
brilliance interfering grateful invoking blossoms carcinogens 
paper boasted footage wayward judging reacting 
tenderly settles prominently clandestine battering docket 
```
</details>

<details>
<summary><h3>1Password Replacement Word List</h3></summary>

**[1password-replacement.txt](lists/1password-replacement/1password-replacement.txt)**: A suggested replacement for [1Password](https://1password.com/)'s word list, based on common words in Google Ngram data. It has the same minimum and maximum word length as [the list 1Password was using in 2021](https://1password.com/txt/agwordlist.txt), plus adds 54 extra words. You can view lists of the words I added and removed from the 2021 1Password list in `lists/1password-replacement/` directory. See [the list's own README for more information](lists/1password-replacement/readme.markdown) on this list.
```text
List length               : 18230 words
Mean word length          : 6.36 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 8 characters (zucchini)
Free of prefix words      : false
Free of suffix words      : false
Entropy per word          : 14.154 bits
Efficiency per character  : 2.227 bits
Assumed entropy per char  : 4.718 bits
Above brute force line    : false
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 6.188
Longest shared prefix     : 7
Unique character prefix   : 8

Pseudorandomly generated sample passphrases
-------------------------------------------
relieved lung heating alone risk medal 
rude fixation ranch furnace walkway bun 
acorn lashes wrinkle smoother hosting pullover 
rider lilies hertz district caresses vagrants 
grimes papyri maternal turkey dish anger
```
</details>

<details>
<summary><h3>Diceware: A new list for using with diceware.</h3></summary>

**[diceware.txt](lists/diceware.txt)**: A new list for using with diceware. Like [the EFF long list](https://www.eff.org/dice), it is free of prefix words, though it has words longer than 9 characters, unlike the EFF long list. The version in this repo has the corresponding dice rolls preceding each word, followed by a tab. The EFF has [instructions for how to use dice and lists like this one to generate passphrases](https://www.eff.org/dice).
```text
List length               : 7776 words
Mean word length          : 7.83 characters
Length of shortest word   : 4 characters (aged)
Length of longest word    : 11 characters (withholding)
Free of prefix words      : true
Free of suffix words      : false
Entropy per word          : 12.925 bits
Efficiency per character  : 1.650 bits
Assumed entropy per char  : 3.231 bits
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 7.559
Longest shared prefix     : 10
Unique character prefix   : 11

Pseudorandomly generated sample passphrases
-------------------------------------------
zero annoyed paralysis prophetic pursuing implemented 
repairs relating withdrawal rewards empires oval 
relates obstacles validity provoked fury salesman 
smiles fears hereby relational rapidly discounted 
circles inclusion marketing reluctantly bureaucracy presently 
```

If you want a 7,776-word diceware list that _does_ include prefix words, there's [diceware-including-prefix.txt](lists/diceware-including-prefix.txt). Just be sure to use a character or space between words in your passphrase!
</details>

<details>
<summary><h3>Suffix-free Diceware: A new diceware list without suffix words</h3></summary>

**[diceware-suffix-free.txt](lists/diceware-suffix-free.txt)**: A new list for using with diceware. Rather than being free of prefix words, like the EFF long list, it is free of _suffix_ words. It's my contention that being free of suffix words provides the same security guarantees -- namely, being able to concatenate words in a passphrase without a delimiter -- as a prefix-word-free list. However, use at your own risk.

```text
List length               : 7776 words
Mean word length          : 7.08 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 10 characters (worthwhile)
Free of prefix words      : false
Free of suffix words      : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.825 bits
Assumed entropy per char  : 4.308 bits
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Longest shared prefix     : 9
Unique character prefix   : 10

Pseudorandomly generated sample passphrases
-------------------------------------------
writers ethic yet pockets lobby talk 
water stated daily trash sublime spelling 
undergoing drinking distinct scientists exposition chart 
remark suite joined sea fetal steal 
victor advocated unfair opponents enable overhead 
```
</details>

<details>
<summary><h3>Prefix Free: A long list free of prefix words.</h3></summary>

**[prefix-free.txt](lists/prefix-free.txt)** is a long list free of prefix words.
```text
List length               : 16606 words
Mean word length          : 8.30 characters
Length of shortest word   : 4 characters (able)
Length of longest word    : 18 characters (telecommunications)
Free of prefix words      : true
Free of suffix words      : false
Entropy per word          : 14.019 bits
Efficiency per character  : 1.689 bits
Assumed entropy per char  : 3.505 bits
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 8.100
Longest shared prefix     : 15
Unique character prefix   : 16

Pseudorandomly generated sample passphrases
-------------------------------------------
flint inflationary corresponds deterministic disappointing incisive 
recorders undoing modifying furthering crashes merrily 
forefront ardent eccentricity extraneous staked charred 
carcinogens militarism universals fanning communicates whereabouts 
repealed hedged legendary psychical thereof briefs 
```
</details>

<details>
<summary><h3>Suffix Free: A long list free of suffix words</h3></summary>

**[suffix-free.txt](lists/suffix-free.txt)** is a long list free of suffix words. I think this would be a good one to use as a wordlist for [the KeePassXC password manager](https://keepassxc.org/), but I'm not sure. Use at your own risk. A 7-word passphrase from this list provides 98.26 bits of entropy, compared to the EFF long list (KeePassXC's default list), from which a 7-word passphrase provides 90.47 bits.
```text
List length               : 16815 words
Mean word length          : 8.02 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 15 characters (vulnerabilities)
Free of prefix words      : false
Free of suffix words      : true
Entropy per word          : 14.037 bits
Efficiency per character  : 1.750 bits
Assumed entropy per char  : 4.679 bits
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 7.954
Longest shared prefix     : 14
Unique character prefix   : 15

Pseudorandomly generated sample passphrases
-------------------------------------------
adopting skeletons suitability silence tempered breathe 
seventies benevolent dining psychologically fortifications aggrieved 
predator shaft paternity resists instinctive coldly 
packs poisons indebtedness dislocation arrival sockets 
disarray midday industry defenders sculptors enclosed 
```
</details>

<details>
<summary><h3>Short: A short word list of 1,030 words</h3></summary>

**[short.txt](lists/short.txt)** is a short list with words that have unique three-character prefixes and the shortest edit distance between any two words is 3 characters. It's also free of prefix words. These attributes of the list are meant to emulate [the EFF short lists](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases).
```text
List length               : 1030 words
Mean word length          : 8.46 characters
Length of shortest word   : 5 characters (yusuf)
Length of longest word    : 12 characters (totalitarian)
Free of prefix words      : true
Free of suffix words      : true
Entropy per word          : 10.008 bits
Efficiency per character  : 1.183 bits
Assumed entropy per char  : 2.002 bits
Above brute force line    : true
Above Shannon line        : true
Shortest edit distance    : 3
Mean edit distance        : 8.046
Longest shared prefix     : 2
Unique character prefix   : 3

Pseudorandomly generated sample passphrases
-------------------------------------------
popcorn wisconsin charcoal citadel pavilion cylindrical 
hitchcock tavistock wasteland ridiculous evolutionary dyspnea 
sleepless mcmahon knoxville justinian tennyson haphazard 
cutaneous september appetites awareness lobbyists eritrea 
glucose ithaca baptized obesity superego aircraft 
```
</details>

<details>
<summary><h3>Wikilist: A word list based on word frequency from Wikipedia</h3></summary>

**[wikilist.txt](lists/wikilist.txt)** is based on [word frequency from Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/blob/master/results/enwiki-20190320-words-frequency.txt) rather than Google Ngram data. (Thanks to [Aaron Toponce](https://fosstodon.org/@atoponce) for pointing me to this list.)
```text
List length               : 17511 words
Mean word length          : 7.30 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 11 characters (worshippers)
Free of prefix words      : false
Free of suffix words      : false
Entropy per word          : 14.096 bits
Efficiency per character  : 1.932 bits
Assumed entropy per char  : 4.699 bits
Above brute force line    : true
Above Shannon line        : false
Shortest edit distance    : 1
Mean edit distance        : 7.243
Longest shared prefix     : 10
Unique character prefix   : 11

Pseudorandomly generated sample passphrases
-------------------------------------------
spiritual lobbyist ethics works doing curling 
condemning greenish literacy oddly thirds implies 
cad presenter pays tennis keyboard tutor 
coward sages opens aperture fossil custodian 
negative sectors afflicted bout ramps honeycomb
```
</details>

## Methodology

For the lists based on [Google Books Ngram data](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html), I [scraped](https://github.com/sts10/common_word_list_maker) the 2012 dataset and made a list of the most frequently appearing 100,000 words between 1975 and 2012. Then, using [a separate tool I wrote](https://github.com/sts10/tidy), I cut this list down into various sizes to create the word lists included in this repo.

Other lists in this repo use this study of [word frequency on Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/) as an initial input/corpus. 

### Assumed use-cases of passphrases 

Let's consider _**when**_ a password manager user might want to use a passphrase rather than a password like `96W8vaCHCR':XXj,xhJ6`. I based my work around three use-cases (loosely ranked by importance/priority): 

1. When creating a master password that the user will have to memorize and type frequently.
2. When creating an account where they'll enter the password in a situation where they can not auto-fill or copy it from a 1Password app (for example: a smart TV or computers where they don't have 1Password installed). I think of this as a case where the user needs to hold their password in their minds for a few seconds.
3. When creating an account they anticipate they may have to read the password over a voice channel.

For the first use-case, I wanted to make a list that prioritized words that were "story-able". By "story-able", I mean words that most users will be able to construct a story with. Inspired by [the "Password Strength" xkcd comic](https://xkcd.com/936/?correct=horse&battery=staple), I contend that users memorize passphrases by creating a little story for themselves. 

![Correct horse battery stapler comic](https://imgs.xkcd.com/comics/password_strength.png)

This guided my choice to use Google Books data -- these are words that literally make up the stories of English-speaking people. Whether certain parts of speech, like nouns, some balanced mix of parts of speech, or other categorizations of words, like singular nouns, are generally more "story-able" than others is a question to explore further.

While this "story-ability" will help with assumption #2, I argue that words that are good for holding in your mind temporarily are words that are what I'd call "mentally pronounceable" (shout-out to [Reddit user out0focus for crystallizing this for me](https://www.reddit.com/r/1Password/comments/ur4otq/comment/i8x040c/?utm_source=reddit&utm_medium=web2x&context=3)), by which I simply mean that you can hold them in your mind as a _word_ rather than a collection of letters. I think how easy a word is to spell is closely related to this -- perhaps "mental pronounceable" is the ease of "taking in" a word, and spell-ability is the ease of (re-)producing it (entering it into the interface). To make this more concrete, imagine carrying `entendre goyim ormolu waggish` (four words currently on 1Password's word list) vs. `doubling striker adverbs guided`.

Re: assumption #3, while I didn't optimize my lists for (phonetically) pronounceable words, I think that the methodology I used (striving to use "common" words) works toward this goal.

### The "re-roll" problem

When I [posted one of my lists to 1Password's subreddit](https://www.reddit.com/r/1Password/comments/ur4otq/proposed_new_word_list/), a few users mentioned how, when using the current 1Password list, they would "re-roll" for a new passphrase if they got a "weird" word in their original passphrase. This has the mathematical effect of making their passphrases weaker, since it effectively shortens the word list, and thus decreases the amount of entropy each word gives. (In practice, this would necessitate an attacker to skip these uncommon words in their attacks, which doesn't seem too improbable?) It's much better to replace these "skip" words in the word list, bringing the "real-world" amount of entropy-per-word more in-line with the theoretical figure, which we can easily calculate and base security guidance on.

### Auto-correct

If a word in a passphrase is very uncommon, it may even be auto-corrected by some applications you might pasted/type it in to. `quean` may be a good example of this. (Granted, if an interface has auto-correct working, it likely is NOT a place a secure passphrase should be entered, but that's a different issue.)

### The similar-words problem

Some of these lists contains very similar words, such as "tabs" and "tab" and/or "suggested", "suggesting", and "suggestions". I don't think this effect entropy-per-word calculations. But I could see how it would be awkward to get two similar words in the same passphrase.

However, I _think_ the chances of this are pretty small. If we assumed a hypothetical 18,000 word list that was just 9,000 words and their plurals, I think the odds of getting at least one "awkward double" in a 4-word passphrase is `(1/18000) * (2/18000) * (3/18000)`, which is a really small number. But check my math!

I'll also not that this issue is similar to the risk of getting the same exact word in a passphrase, which we can't help without changing how we generate the passphrases in a way that lowers the entropy of the resulting passphrase.

## Tools and resources I used to generate these word lists

- [Common Word List Maker](https://github.com/sts10/common_word_list_maker): Scrapes Google Books Ngram data to create a long word list
- [Tidy](https://github.com/sts10/tidy): A command-line utility for editing word lists. Can also print notable attributes of word lists, such as those printed above.
- [Homophones](https://github.com/sts10/homophones/tree/main/homophone-lists): A list of English homophones, and a method for producing more lists of English homophones
- This study of [word frequency on Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/)

## Disclaimers

While I've attempted to remove offensive words from these lists, since I haven't checked them by hand there may be some left. Apologies. Feel free to create an Issue or Pull Request removing offensive word(s).

Also, I make no guarantees about the security of passphrases using these lists. Please check their safety yourself before using in situations that require secure passphrases.

## On licensing/usage

This project and its word lists are licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/). See LICENSE file for more information.

The words for some of these generated word lists come from Google Books Ngram data. This data compilation "is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/)" ([source](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html)). This project has no association with Google, nor does Google endorse this project. [More information available at the original project's repo](https://github.com/sts10/common_word_list_maker).

I'll note here that at least one list in this project was derived from [this Wikipedia word frequency project](https://github.com/IlyaSemenov/wikipedia-word-frequency/), which uses the MIT license. I offer this list under the same license as the other word lists in this project.

## Related projects

As a proof-of-concept, I made some [word lists optimized for inputting on smart TVs](https://github.com/sts10/remote-words).

## Requests? Suggestions? 

Happy to make word lists given reasonable parameters! Just create an Issue.
