In the literature surrounding this task, the terms “sentiment analysis” (SA) and “opinion mining” (OM) are used more or less interchangeably, which is inconvenient and seems unintuitive–surely “sentiment” and “opinion” are two different things?

The most famous and influential paper in this area, Pang and Lee (2008)<sup>1</sup>, includes a lengthy section on this terminology problem, but concludes that, as the then already existing literature used both terms, they should be used synonymously. The other highly cited survey paper Liu does the same, classing sentiment as a form of opinion along with evaluation, appraisal, attitude, and emotion, and states that, "Sentiment analysis and opinion mining mainly focuses on opinions which express or imply positive or negative sentiments", which doesn’t seem to clear much up. With a combined c.10,000 citations, it’s hard to argue with the influence of these two papers, and most subsequent surveys follow the approach of treating the two terms synonymously and interchangeably (see for example, Vinodhini and Chandrasekaran (2012), Medhat et al. (2014), Ravi and Ravi (2015),  Balazs and Velásquez (2016)). However, it remains unsatisfying to have to write the cumbersome “sentiment analysis and opinion mining” everytime we wish to refer to this task.

A recent survey, Yadollahi et al., attempts to sort out this mess, proposing a taxonomy of related problems. It’s an admirable attempt to do what nobody has done yet, but for me, poses more questions than it answers. For example, why should opinion mining be a hyponym of sentiment analysis? After all, Liu has it the other way around, and I can’t really see why one should be hypernomous of the other anyway.

Maybe the dictionary definition can help? A quick search of five online dictionaries does not resolve the confusion, with “opinion” appearing in the definition of “sentiment” in 3/5 cases, and “sentiment” in one of the other’s definition of “opinion”. So, maybe these two words are similar enough to be treated synonymously after all?

Only Collins is able to define both these words without using one of them in the definition of the other, the difference for them appearing to be that unlike opinion, sentiment is concerned (at least to some extent) with “feelings”. 

What about Wordnet? Here, sentiment and opinion are synonyms, while both are hyponyms of belief. If a taxonomy of terms is to be established, maybe this makes more sense as its basis.

Delving deeper into English linguistics, we find that, while not mentioning sentiment or opinion explicitly, in discussing stative verbs used to describe ‘private’ states, Quirk (1985) differentiates between intellectual states and states of emotion or attitude. Could this be the basis of a taxonomy?


There is already NLP work considering private states, such as Wilson and Wiebe (2005), and Rambow and Wiebe (2015), which differentiates between sentiment (can be directed at an entity or a state of affairs) and belief (with only states of affairs as targets).

Conclusion:
A better system of terminology may exist, but it’s probably too much to go against 10,000 citations. For current work, I’m just going to have to go with the clunky <em>Sentiment Analysis and Opinion Mining</em> (<em>SA & OM</em>).
