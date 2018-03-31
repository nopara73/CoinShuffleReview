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

# Abbreviations

| Abbreviation  | Phrase |
| ------------- | ------------- |
| BCM  | Byzantine Cycle Mode  |
| CoinShuffle  | CS  |
| CoinShuffle++  | CS++  |
| CCJ  | Chaumian CoinJoin  |
| ZL  | ZeroLink  |
| DM  | DiceMix  |

# Questions

## The authors are not citing BCM. Can that improve upon CS++?

## What is the best algorithm to mix unequal inputs?
### Notes
Right now all Bitcoin mixing technique are mixing in rounds with a common, pre-defined denomination. But it is possible to add additional anonymity by adding additional mixing. An obvious improvement would be to add additional mixing to the change outputs, but there are better ways to do this. I previously [attempted](https://medium.com/@nopara73/math-problem-c5fa3ed151ea) to find an optimal algorithm, but I failed.

## Answer

## Is CS++ extendable to mix unequal inputs?
### Notes
In CCJ the server can easily build the transaction in an optimal way, but CS++ needs to come to decentralized consensus.

## Would replacing DM with Tor is possible and would it make it simpler?

## Can blind signatures improve upon CS++?

No.

## Can CS++ be done in a fully P2P way?

## How does CS++ compares to ZL and CCJ?

ZL is a framework that makes sure round based mixing techniques don't get deanonymized due to other means. CS++ and CCJ can both be used with ZL.

CS++ pros:
- More decentralized, it may even be possible to be built in a fully decentralized way. Decentralization provides censorship resistance.
- Better researched and has higher quality academic specification.
- Its mixing don't rely on an external anonymity network, rather it presents its own: DM. It relies on an anonymity network only for IP masking, if this anonymity network fails or isn't implemented in the first place it's not a big problem.

CCJ pros:
- Faster, although it doesn't matter, because the most time will always be spent on to wait for peers.
- Much simpler.
- More interactive feedback can be provided to the user.
- Easy to change, its implementation flaws rarely require upgrading every client, but only the coordinator.

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
