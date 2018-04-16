In the literature surrounding this task, the terms “sentiment analysis” (SA) and “opinion mining” (OM) are used more or less interchangeably, which is inconvenient and seems unintuitive–surely “sentiment” and “opinion” are two different things?

The most famous and influential paper in this area, Pang and Lee (2008)<sup>1</sup>, includes a lengthy section on this terminology problem, but concludes that, as the then already existing literature used both terms, they should be used synonymously. The other highly cited survey paper, Liu (2012),<sup>2</sup> does the same, classing sentiment as a form of opinion along with evaluation, appraisal, attitude, and emotion, and states that, "Sentiment analysis and opinion mining mainly focuses on opinions which express or imply positive or negative sentiments", which doesn’t seem to clear much up. With a combined c.10,000 citations, it’s hard to argue with the influence of these two papers, and most subsequent surveys follow the approach of treating the two terms synonymously and interchangeably (see for example, Vinodhini and Chandrasekaran (2012),<sup>3</sup> Medhat et al. (2014),<sup>4</sup> Ravi and Ravi (2015),<sup>5</sup> Balazs and Velásquez (2016).<sup>6</sup> However, it remains unsatisfying to have to write the cumbersome “sentiment analysis and opinion mining” everytime we wish to refer to this task.

A recent survey, Yadollahi et al.,<sup>7</sup> attempts to sort out this mess, proposing a taxonomy of related problems.

![Taxonomy of sentiment analysis tasks.]({{ "/assets/sentimenttaxonomy.png" | absolute_url }})

It’s an admirable attempt to do what nobody has done yet, but for me, poses more questions than it answers. For example, why should opinion mining be a hyponym of sentiment analysis? After all, Liu has it the other way around, and I can’t really see why one should be hypernomous of the other anyway.

Maybe the dictionary definition can help? A quick search of five online dictionaries does not resolve the confusion, with “opinion” appearing in the definition of “sentiment” in 3/5 cases, and “sentiment” in one of the other’s definition of “opinion”. So, maybe these two words are similar enough to be treated synonymously after all?

Only Collins is able to define both these words without using one of them in the definition of the other, the difference for them appearing to be that unlike opinion, sentiment is concerned (at least to some extent) with “feelings”. 

What about Wordnet?<sup>8</sup> Here, sentiment and opinion are synonyms, while both are hyponyms of belief. If a taxonomy of terms is to be established, maybe this makes more sense as its basis.

Delving deeper into English linguistics, we find that, while not mentioning sentiment or opinion explicitly, in discussing stative verbs used to describe ‘private’ states, Quirk (1985)<sup>9</sup> differentiates between intellectual states and states of emotion or attitude. Could this be the basis of a taxonomy?


There is already NLP work considering private states, such as Wilson and Wiebe (2005),<sup>10</sup> and Rambow and Wiebe (2015),<sup>11</sup> which differentiates between sentiment (can be directed at an entity or a state of affairs) and belief (with only states of affairs as targets).

Conclusion:
A better system of terminology may exist, but it’s probably too much to go against 10,000 citations. For current work, I’m just going to have to go with the clunky <em>Sentiment Analysis and Opinion Mining</em> (<em>SA & OM</em>).

<h3>References</h3>

1. Pang, B. and Lee, L., 2008. <em>Opinion mining and sentiment analysis</em>. Foundations and Trends® in Information Retrieval, 2(1–2), pp.1-135.
2. Liu, B., 2012. <em>Sentiment analysis and opinion mining</em>. Synthesis lectures on human language technologies, 5(1), pp.1-167. 
3. Vinodhini, G. and Chandrasekaran, R.M., 2012. <em>Sentiment analysis and opinion mining: a survey</em>. International Journal, 2(6), pp.282-292.
4. Medhat, W., Hassan, A. and Korashy, H., 2014. <em>Sentiment analysis algorithms and applications: A survey</em>. Ain Shams Engineering Journal, 5(4), pp.1093-1113. 
5. Ravi, K. and Ravi, V., 2015. <em>A survey on opinion mining and sentiment analysis: tasks, approaches and applications. Knowledge-Based Systems</em>, 89, pp.14-46.
6. Balazs, J.A. and Velásquez, J.D., 2016. <em>Opinion mining and information fusion: a survey</em>. Information Fusion, 27, pp.95-110.
7. Yadollahi, A., Shahraki, A.G. and Zaiane, O.R., 2017. <em>Current state of text sentiment analysis from opinion to emotion mining</em>. ACM Computing Surveys (CSUR), 50(2), p.25.
8. https://wordnet.princeton.edu/
9. Quirk, R., 1985. <em>A comprehensive grammar of the English language</em>. Longman.
10. Wilson, T. and Wiebe, J., 2005, June. <em>Annotating attributions and private states</em>. In Proceedings of the Workshop on Frontiers in Corpus Annotations II: Pie in the Sky (pp. 53-60). Association for Computational Linguistics.
11. Rambow, O. and Wiebe, J., 2015. Sentiment and belief: How to think about, represent, and annotate private states. Tutorials, pp.7-11.
