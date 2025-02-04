# Generated word lists

A repository for word lists I've generated. Most are proof-of-concept or experimental. Some lists are based on [Google Ngram data](https://github.com/sts10/common_word_list_maker), others are based on [word frequency data from (English) Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/), and some are based on a mix of both sources.

**If you're looking for more usable, polished wordlists, you should consider my [Orchard Street Wordlists](https://github.com/sts10/orchard-street-wordlists).**

## About the word lists

Detailed information about most of the lists in this repository is available below. The main differences are in list length, whether they're uniquely decodable, and whether they have corresponding dice roll values in them.

Following [the BIPS 0039 spec](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki), all lists in this repository are Unicode normalized with [NFKD](https://www.unicode.org/glossary/#normalization_form_kd), though since they're all English lists this shouldn't matter much, if at all.

### Just give me a word list

* If you're feeling **a little overwhelmed** by choice here, just head over to [Orchard Street Wordlists](https://github.com/sts10/orchard-street-wordlists). They are basically the cleaned-up, best-of-the-best lists from this project.
* If you just want **a plain, long word list**, I'd point you to [basic.txt](lists/basic.txt).
* If you want to **[use dice](https://www.eff.org/dice) to create your passphrases**, I'd suggest [diceware-suffix-free.txt](lists/diceware-suffix-free.txt).
* If you're **feeling adventurous**, I'd point you to [UD1](lists/experimental/ud1.txt) or [UDWiki](lists/experimental/ud_wikilist.txt); or if you're going to be using with dice, [diceware-ud](lists/experimental/diceware-ud.txt).
* If you want the **very long** list, [UD2](lists/experimental/ud2.txt) is 40,000 words, which gives 15.29 bits of entropy per word.
* If you're looking to make passphrases that you'll frequently be inputting on **smart TVs** and/or similar devices, I'd point you to [another repo of mine](https://github.com/sts10/remote-words).

<!--
|                       | length | Uniquely decodable? | Diceware compatible? |
|-----------------------|--------|---------------------|----------------------|
| basic.txt             | 18291  | ❌                  | ❌                   |
| UD1                   | 17576  | ✅                  | ❌                   |
| UD Diceware           | 7776   | ✅                  | ✅                   |
| 1Password replacement | 18208  | ❌                  | ❌                   |
-->
<details>
<summary><h3>Basic List: A long word list based on common words in Google Ngram data</h3></summary>

**[basic.txt](lists/basic.txt)**
```text
List length               : 18250 words
Mean word length          : 7.53 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 12 characters (workstations)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 14.156 bits
Efficiency per character  : 1.879 bits
Assumed entropy per char  : 4.719 bits
Above brute force line?   : false
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 7.501
Longest shared prefix     : 11
Unique character prefix   : 12

Word samples
------------
shapes doped ventures damp scholars curves
flanks carnal muster dialogues casualties crib
sandwiches accepting pronoun blasted microcosm madame
diminution rotate propped entitled familiar sessions
receive prevailed refused rotating smokers ensures
```
</details>

<details>
<summary><h3>Proposed New 1Password Word List</h3></summary>

**[1password-replacement.txt](lists/1password-replacement/1password-replacement.txt)**: A suggested replacement for [1Password](https://1password.com/)'s word list. You can view lists of the words I added and removed from [a recent version of the 1Password word list](https://github.com/1Password/spg/blob/master/testdata/agwordlist.txt) in `lists/1password-replacement/` directory. See [the list's own README for more information](lists/1password-replacement/readme.markdown) on this list.
```text
List length               : 18325 words
Mean word length          : 7.12 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 10 characters (zoological)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 14.162 bits
Efficiency per character  : 1.990 bits
Assumed entropy per char  : 4.721 bits
Above brute force line?   : false
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 7.020
Longest shared prefix     : 9
Unique character prefix   : 10

Word samples
------------
embracing mingle customs silences wholeness host
grinning defeat voodoo spin kitten audiences
sizeable warren dispatches relief managing bottled
offering genera ousted spherical sanctions expressway
motivate operative receding circus triangular pleases
```
</details>

<details>
<summary><h3>Diceware: A new list for using with diceware</h3></summary>

**[diceware.txt](lists/diceware.txt)**: A new list for using with diceware. Like [the EFF long list](https://www.eff.org/dice), it is free of prefix words, though it has words longer than 9 characters, unlike the EFF long list. The version in this repo has the corresponding dice rolls preceding each word, followed by a tab. The EFF has [instructions for how to use dice and lists like this one to generate passphrases](https://www.eff.org/dice).
```text
List length               : 7776 words
Mean word length          : 7.61 characters
Length of shortest word   : 3 characters (ads)
Length of longest word    : 11 characters (withholding)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.697 bits
Assumed entropy per char  : 4.308 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 7.431
Longest shared prefix     : 10
Unique character prefix   : 11

Word samples
------------
flown annotated issues operative referred dismissal
electricity temporal diversified imitate single signs
toilet gown corrective trailer airport ventricular
periphery tensions duly lent alloys agony
mills instructors bodily compelling defects alienation
```

If you want a 7,776-word diceware list that is **not** uniquely decodable, there's [diceware-not-ud.txt](lists/diceware-not-ud.txt). Just be sure to use a character or space between words in your passphrases!
</details>

<details>
<summary><h3>Suffix-free Diceware: A new diceware list without suffix words</h3></summary>

**[diceware-suffix-free.txt](lists/diceware-suffix-free.txt)**: A new list for using with diceware. Rather than being free of prefix words, like the EFF long list, it is free of _suffix_ words. The list is uniquely decodable, so words from it can be safely concatenated without a separator, just like the EFF long list.

```text
List length               : 7776 words
Mean word length          : 7.11 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 10 characters (worthwhile)
Free of prefix words?     : false
Free of suffix words?     : true
Uniquely decodable?       : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.819 bits
Assumed entropy per char  : 4.308 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 6.992
Longest shared prefix     : 9
Unique character prefix   : 10

Word samples
------------
fifth melancholy ounces vast slept separated
mobility games anonymous vertical ambitions autonomy
destined picking leave lawyers knights alarm
lifelong quietly chief diagonal leaf sadness
assessing jazz wishing fighting painter executing
```
</details>

<details>
<summary><h3>Prefix Free: A long list free of prefix words</h3></summary>

**[prefix-free.txt](lists/prefix-free.txt)** is a long list free of prefix words.
```text
List length               : 16385 words
Mean word length          : 8.26 characters
Length of shortest word   : 3 characters (ads)
Length of longest word    : 15 characters (vulnerabilities)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 14.000 bits
Efficiency per character  : 1.695 bits
Assumed entropy per char  : 4.667 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 8.063
Longest shared prefix     : 14
Unique character prefix   : 15

Word samples
------------
tranquility tents creatively anywhere hoarse ruled
stonewall creamy acclaimed protectors simulations peering
steaming vanishing malignant maximizes exasperated nemesis
chicks seaman circling oxen waxed prism
defeating preexisting moot authored earlier rocky
```
</details>

<details>
<summary><h3>Suffix Free: A long list free of suffix words</h3></summary>

**[suffix-free.txt](lists/suffix-free.txt)** is a long list that is uniquely decodable (it is free of suffix words). I think this would be a good one to use as a wordlist for [the KeePassXC password manager](https://keepassxc.org/), however use at your own risk. A 7-word passphrase from this list provides about 98 bits of entropy, compared to the EFF long list (KeePassXC's default list), from which a 7-word passphrase provides about 90.5 bits.
```
List length               : 16384 words
Mean word length          : 7.99 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 15 characters (troubleshooting)
Free of prefix words?     : false
Free of suffix words?     : true
Uniquely decodable?       : true
Entropy per word          : 14.000 bits
Efficiency per character  : 1.751 bits
Assumed entropy per char  : 4.667 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 7.946
Longest shared prefix     : 14
Unique character prefix   : 15

Word samples
------------
transported citizens punches privileged bytes dimensionless
window reputation embarked retreated adequately cartilage
sanction unbeaten dreamed suggestive planting magazine
converse assassinated omnibus hostages sandwiches constructions
fuels robotic compensating useless daylight athletic
```

</details>

<!--
<details>
<summary><h3>Short: A short word list of 1,030 words</h3></summary>

**[short.txt](lists/short.txt)** is a short list with words that have unique three-character prefixes and the shortest edit distance between any two words is 3 characters. It's also uniquely decodable -- it's actually free of prefix words and suffix words. These attributes of the list are meant to emulate [the EFF short lists](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases).
```text
List length               : 1030 words
Mean word length          : 8.46 characters
Length of shortest word   : 5 characters (yusuf)
Length of longest word    : 12 characters (totalitarian)
Free of prefix words?     : true
Free of suffix words?     : true
Uniquely decodable?       : true
Entropy per word          : 10.008 bits
Efficiency per character  : 1.183 bits
Assumed entropy per char  : 2.002 bits
Above brute force line?   : true
Above Shannon line?       : true
Shortest edit distance    : 3
Mean edit distance        : 8.046
Longest shared prefix     : 2
Unique character prefix   : 3

Word samples
------------
popcorn wisconsin charcoal citadel pavilion cylindrical
hitchcock tavistock wasteland ridiculous evolutionary dyspnea
sleepless mcmahon knoxville justinian tennyson haphazard
cutaneous september appetites awareness lobbyists eritrea
glucose ithaca baptized obesity superego aircraft
```
</details>
-->
<details>
<summary><h3>Wikilist: A word list based on word frequency from Wikipedia</h3></summary>

**[wikilist.txt](lists/wikilist.txt)** is based on [word frequency from English-language Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/) rather than Google Ngram data. (Thanks to [Aaron Toponce](https://fosstodon.org/@atoponce) for pointing me to this list.)
```
List length               : 17576 words
Mean word length          : 7.31 characters
Length of shortest word   : 3 characters (ace)
Length of longest word    : 11 characters (worshippers)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 14.101 bits
Efficiency per character  : 1.928 bits
Assumed entropy per char  : 4.700 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 7.252
Longest shared prefix     : 10
Unique character prefix   : 11

Word samples
------------
coupe autograph thrust groves hermitage asserts
investor reputation contempt happy chaplain vans
exponential turbine epistle comparable equatorial communes
robust incoming justified mandate evicted quitting
encryption cheated enlistment associates closer experienced
```
</details>

### Experimental lists

<details>
<summary><h3>UD1: A 17k-word, uniquely decodable word list</h3></summary>

**[ud1.txt](lists/experimental/ud1.txt)** is a long, uniquely decodable list, based on Google Ngram data. It was made uniquely decodable [via a process I created](https://sts10.github.io/2022/08/12/efficiently-pruning-until-uniquely-decodable.html) and thus I mark it as **EXPERIMENTAL**. Use with caution. As an aid to help you choose words randomly from this list, see the [cardware list](lists/experimental/cardware.txt).
```
List length               : 17576 words
Mean word length          : 8.00 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 15 characters (vulnerabilities)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 14.101 bits
Efficiency per character  : 1.763 bits
Assumed entropy per char  : 4.700 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 7.933
Longest shared prefix     : 14
Unique character prefix   : 15

Word samples
------------
platelets designation ministries theoretically revenge felony
risks landlord rotates brain shipment rafters
yellow gear contends dimensionless suspended uncertainties
delegations suspected enraged suite occasional circumference
obsessive assimilate localities rover cerebellum decks
```
</details>

<details>
<summary><h3>UD Diceware: A diceware list that is uniquely decodable</h3></summary>

**[diceware-ud.txt](lists/experimental/diceware-ud.txt)** is a uniquely decodable list for use with diceware. The words are based on Google Ngram data. It was made uniquely decodable [via a process I created](https://sts10.github.io/2022/08/12/efficiently-pruning-until-uniquely-decodable.html) and thus I mark it as **EXPERIMENTAL**. Use with caution.
```
List length               : 7776 words
Mean word length          : 7.06 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 10 characters (worthwhile)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.832 bits
Assumed entropy per char  : 4.308 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 6.957
Longest shared prefix     : 9
Unique character prefix   : 10

Word samples
------------
toolbar stations injected matters reaches rock
office clean surface marines food overnight
lexical meet avoid decoration thanked paint
responding within doctoral shift security hardy
wolf washed protest sheer virtues splitting
```
</details>

<details>
<summary><h3>UD2: A 40,000-word, uniquely decodable word list</h3></summary>

**[ud2.txt](lists/experimental/ud2.txt)** is a uniquely decodable list, based on Google Ngram data and [Niceware](https://github.com/diracdeltas/niceware) v. 4.0 list. It is free of some common homophones and British spellings of certain words. It was made uniquely decodable [via a process I created](https://sts10.github.io/2022/08/12/efficiently-pruning-until-uniquely-decodable.html) and thus I mark it as **EXPERIMENTAL**. Use with caution.
```
List length               : 40000 words
Mean word length          : 8.56 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 18 characters (transubstantiation)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 15.288 bits
Efficiency per character  : 1.787 bits
Assumed entropy per char  : 5.096 bits
Above brute force line?   : false
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 8.375
Longest shared prefix     : 17
Unique character prefix   : 18

Word samples
------------
blindfolded bossy peacemaker defter prefigured item
algorithm opaquest unrivalled deregulated ambience mules
topple relevantly compilers payload conditionals columbine
comedy conversationally littleness credential sputter kangaroos
strontium amputate skidding yeast heavies weirdest
```
</details>

<details>
<summary><h3>UDWiki: A uniquely-decodable list from Wikipedia word frequency data</h3></summary>

**[ud_wikilist.txt](lists/experimental/ud_wikilist.txt)** is a uniquely decodable list, based on [Wikipedia word frequency data](https://github.com/IlyaSemenov/wikipedia-word-frequency/). It was made uniquely decodable [via a process I created](https://sts10.github.io/2022/08/12/efficiently-pruning-until-uniquely-decodable.html) and thus I mark it as **EXPERIMENTAL**. Use with caution.
```
List length               : 17576 words
Mean word length          : 7.93 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 15 characters (vulnerabilities)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 14.101 bits
Efficiency per character  : 1.777 bits
Assumed entropy per char  : 4.700 bits
Above brute force line?   : true
Above Shannon line?       : false
Shortest edit distance    : 1
Mean edit distance        : 7.864
Longest shared prefix     : 14
Unique character prefix   : 15

Word samples
------------
exit jokes rainier masquerade renewed gurney
moths reversal temptation relented exported echoes
correcting precursor inferred debates baseline curators
registry assuming conceptions scrub faithfully scant
simplicity fingers qualitative siren thoughts gardener
```
</details>

## Methodology

For the lists based on [Google Books Ngram data](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html), I [scraped](https://github.com/sts10/common_word_list_maker) the 2012 dataset and made [a list of the most frequently appearing 100,000 words between 1975 and 2012](https://github.com/sts10/common_word_list_maker/blob/main/word_list_raw.txt).

Other lists in this repo use this [word frequency data from Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/) as an initial input/corpus.

In all cases, I then used [a separate tool I wrote called Tidy](https://github.com/sts10/tidy) to cut these long lists down into various sizes to create the word lists included in this repo.

### Assumed use-cases of passphrases

Let's consider _**when**_ a user might want to use a passphrase rather than a password like `96W8vaCHCR':XXj,xhJ6`. I based my work around three use-cases (loosely ranked by importance/priority):

1. When creating a master password for a password manager or an encrypted drive that the user will have to memorize.
2. When creating an account where they'll enter the password in a situation where they can not auto-fill or copy it from a password manager (for example: a smart TV or computers where they don't have access to their password database). I think of this as a case where the user needs to hold their password in their minds for a few seconds.
3. When creating an account they anticipate they may have to read the password over a voice channel.

For the first use-case, I wanted to make a list that prioritized words that were "story-able". By "story-able", I mean words that most users will be able to construct a story with. Inspired by [the "Password Strength" xkcd comic](https://xkcd.com/936/?correct=horse&battery=staple), I contend that users memorize passphrases by creating a little story for themselves.

![Correct horse battery stapler comic](https://imgs.xkcd.com/comics/password_strength.png)

This guided my choice to use Google Books data -- these are words that literally make up the stories of English-speaking people. Whether certain parts of speech, like nouns, some balanced mix of parts of speech, or other categorizations of words, like singular nouns, are generally more "story-able" than others is a question to explore further.

While this "story-ability" will help with assumption #2, I argue that words that are good for holding in your mind temporarily are words that are what I'd call "mentally pronounceable" (shout-out to [Reddit user out0focus for crystallizing this for me](https://www.reddit.com/r/1Password/comments/ur4otq/comment/i8x040c/?utm_source=reddit&utm_medium=web2x&context=3)), by which I simply mean that you can hold them in your mind as a _word_ rather than a collection of letters. I think how easy a word is to spell is closely related to this -- perhaps "mental pronounceable" is the ease of "taking in" a word, and spell-ability is the ease of (re-)producing it (entering it into the interface).

Re: assumption #3, while I didn't optimize my lists for (phonetically) pronounceable words, I think that the methodology I used (striving to use "common" words) works toward this goal.

### Avoiding the "re-roll" problem by keeping strange words off the lists

When I [posted one of my lists to 1Password's subreddit](https://www.reddit.com/r/1Password/comments/ur4otq/proposed_new_word_list/), a few users mentioned how, when using the current 1Password list, they would "re-roll" for a new passphrase if they got a "weird" word in their original passphrase, like "avioinc", "coquina", "nodulose", "vide", or "wold" (all words currently on the 1Password list as of 2022).

Words that are frequently "re-rolled" have the mathematical effect of making the passphrases of these users weaker, since it effectively shortens the word list, and thus decreases the amount of entropy each word gives. (In practice, this would necessitate an attacker to skip these uncommon words in their attacks, which doesn't seem too improbable?) It's much better to replace these "skip" words in the word list, bringing the "real-world" amount of entropy-per-word more in-line with the theoretical figure, which we can easily calculate and base security guidance on.

### The threat of auto-correct

If a word in a passphrase is very uncommon, it may even be auto-corrected by some applications you might paste or type it in to. `quean`, a word on the current 1Password list, may be a good example of this. (Granted, if an interface has auto-correct active, it likely is NOT a place a secure passphrase should be entered, but that's a different issue.)

### Are lists containing similar words, such as plurals, a problem (either for security or usability)?

Some of these lists contains very similar words, such as "tabs" and "tab" and/or "suggested", "suggesting", and "suggestions". I don't think this affects entropy-per-word calculations.

But I could see how it would be awkward to get two similar words in the same randomly generated passphrase. However, I _think_ the chances of this are pretty small. If we assumed a hypothetical 18,000 word list that was 9,000 words and their plurals, I think the odds of getting at least one "awkward double" in a 4-word passphrase is `1/9000 + 2/9000 + 3/9000 - 11/9000**2 + 6/9000**3`, which is a really small number. (Thanks to [bwbug](https://github.com/bwbug) for [checking my math](https://github.com/sts10/generated-wordlists/issues/1)!)

I'll also note that this issue is similar to the risk of getting the same exact word in a passphrase, which we can't help without changing how we generate the passphrases in a way that lowers the entropy of the resulting passphrase.

## What does it mean if a list is "uniquely decodable"?

If a word list is "uniquely decodable" that means that words from the list can be combined with a delimiter (e.g. "unwovenpreviousslanderpopcorngreedilyepiphany").

As a brief example, if a list has "boy", "hood", and "boyhood" on it, users who specified they wanted two words worth of randomness (entropy) might end up with "boyhood", which an attacker guessing single words would try. Removing the word "boy", which makes the remaining list uniquely decodable, prevents this possibility from occurring.

Some of the lists in this repository are uniquely decodable, while others are not. The lists marked "experimental" are so marked because I used a method adapted from [the Sardinas–Patterson algorithm](https://en.wikipedia.org/wiki/Sardinas%E2%80%93Patterson_algorithm) to make them uniquely decodable that I have named "Schlinkert pruning." You can learn more about uniquely decodable codes and Schlinkert pruning from [this blog post](https://sts10.github.io/2022/08/12/efficiently-pruning-until-uniquely-decodable.html). Use at your own risk!

Other lists in this repository were made uniquely decodable by more established methods, namely removing all [prefix words](https://en.wikipedia.org/wiki/Prefix_code) or removing all suffix words.

## Using these word lists with KeePassXC

[KeePassXC](https://keepassxc.org), a password manager, allows users to use any word list they want.

To do this, click on the dice icon to open the password generator, then click over to the "Passphrase" tab, then click to + button to choose a word list file. Be sure to **only use a uniquely decodable list with KeePassXC** like "Suffix Free" list or the UD1 list.

![Screenshot showing how to change the word list that KeePassXC uses](img/keepassxc-use.png)

## Tools and resources I used to generate these word lists

- [Common Word List Maker](https://github.com/sts10/common_word_list_maker): Scrapes Google Books Ngram data to create a long word list of commonly used words
- [Tidy](https://github.com/sts10/tidy): A command-line utility for editing word lists. Can also print notable attributes of word lists, such as those printed above.
- [Homophones](https://github.com/sts10/homophones/tree/main/homophone-lists): A list of English homophones, and a method for producing more lists of English homophones
- [This study of word frequencies on Wikipedia](https://github.com/IlyaSemenov/wikipedia-word-frequency/)

## Disclaimers

While I've attempted to remove offensive words from these lists, since I haven't checked them by hand there may be some left. Apologies. Feel free to create an Issue or Pull Request removing offensive word(s).

Also, I make no guarantees about the security of passphrases generated from these lists, nor the promised amount of entropy, which is theoretical. Please check their safety yourself before using in situations that require secure passphrases. And the method of choosing words from these lists must be sufficiently random to ensure promised security.

## Related projects

* [Orchard Street Wordlists](https://github.com/sts10/orchard-street-wordlists) are a set of more polished word lists I have made.
* I have also created some [word lists optimized for inputting with TV remotes or video game controllers](https://github.com/sts10/remote-words).

## On licensing/usage

The words contained in these word lists are taken from two sources: [Google Books Ngram data](https://storage.googleapis.com/books/ngrams/books/datasetsv3.html) and [Wikipedia](https://www.wikipedia.org/), via [a Wikipedia word frequency project](https://github.com/IlyaSemenov/wikipedia-word-frequency/).

This project has no association with Google, Wikipedia, or the creators of the Wikipedia frequency project cited above. Neither Google, Wikipedia, nor the creators of the Wikipedia word frequency project cited above endorses this project.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

## Requests? Suggestions?

Happy to make word lists given reasonable parameters! Just create an Issue.
