# CoinShuffleReview
Review of [CoinShuffle++](http://wp.internetsociety.org/ndss/wp-content/uploads/sites/25/2017/09/ndss201701-4RuffingPaper.pdf).

# In A Nutshell

CoinShuffle is a Bitcoin mixing technique, based on CoinJoin, [presented in 2014](https://bitcointalk.org/index.php?topic=567625.0). CoinShuffle++ is its successor, [presented in 2016](https://bitcointalk.org/index.php?topic=1497271).

# Methodology

The review is done in a Q&A format. My process of fully digesting the paper was the following:

1. Ask questions.
2. Read Abstract and ask questions.
3. Read Conclusion and ask questions.
4. Skim the paper, get familiar with its flow.
5. Skim the paper, read interesting parts, look at figures and ask questions.
6. Read Introduction, ask questions and take notes for the authors.
7. Try to answer questions.
8. Read the rest of the paper, try to answer questions and take notes for the authors.
9. Read Abstract, Introduction and Conclusion again.
10. Skim the rest of the paper, read interesting parts and ask questions.
11. Try to answer most questions.
12. Send notes, answered and unanswered questions to the authors.

# Questions

# Notes

## Math

![](https://i.imgur.com/1iqvbmE.png)

That's a fancy way to say it.

## Banking Vs Crypto Anonymity

![](https://i.imgur.com/ZNOadnW.png)

It's often overlooked.

## Anonymity Network Dependency

![](https://i.imgur.com/7HdjVoy.png)

Indeed, it's not insignificant if the IP anonymity set consists of real or Tor IPs. From an implementation point of view this opens a can of worms. Yet, I suspect the first version of this can get away with not using Tor.
