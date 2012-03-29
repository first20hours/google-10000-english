About This Repo
===============

This repo contains a list of the 10,000 most common English words in order of frequency, as determined by [n-gram](http://en.wikipedia.org/wiki/N-gram) [frequency analysis](http://en.wikipedia.org/wiki/Frequency_analysis) of the [Google's Trillion Word Corpus](http://books.google.com/ngrams/info).

According to the [Google Machine Translation Team](http://googleresearch.blogspot.com/2006/08/all-our-n-gram-are-belong-to-you.html):

>Here at Google Research we have been using word n-gram models for a variety of R&D projects, such as statistical machine translation, speech recognition, spelling correction, entity detection, information extraction, and others. While such models have usually been estimated from training corpora containing at most a few billion words, we have been harnessing the vast power of Google's datacenters and distributed processing infrastructure to process larger and larger training corpora. We found that there's no data like more data, and scaled up the size of our data by one order of magnitude, and then another, and then one more - resulting in a training corpus of one trillion words from public Web pages.
>
>We believe that the entire research community can benefit from access to such massive amounts of data. It will advance the state of the art, it will focus research in the promising direction of large-scale, data-driven approaches, and it will allow all research groups, no matter how large or small their computing resources, to play together. That's why we decided to share this enormous dataset with everyone. We processed 1,024,908,267,229 words of running text and are publishing the counts for all 1,176,470,663 five-word sequences that appear at least 40 times. There are 13,588,391 unique words, after discarding words that appear less than 200 times.

This repo is derived from [Peter Novig's](http://norvig.com/ngrams/) compilation of the [1/3 million most frequent English words](http://norvig.com/ngrams/count_1w.txt). I limited this file to the 10,000 most common words, then removed the appended frequency counts by running this sed command in my text editor: 

    sed 's/[0-9]*//g'

Usage
-----

This repo is useful as a corpus for typing training programs. According to analysis of the [Oxford English Corpus](http://oxforddictionaries.com/words/the-oec-facts-about-the-language), the 7,000 most common English lemmas account for approximately 90% of usage, so a 10,000 word training corpus is more than sufficient for practical training applications.

To use this list as a training corpus in [Amphetype](http://code.google.com/p/amphetype/), paste the contents into the "Lesson Generator" tab with the following settings:

    Make **3** copies of the list

    Divide into sublists of size **3**

    Add to sources as **google-10000-english**

In the "Sources" tab, you should see **google-10000-english** available for training. Set WPM at 10 more than your current average, set accuracy to 98%, and you're set to train.

Enjoy!