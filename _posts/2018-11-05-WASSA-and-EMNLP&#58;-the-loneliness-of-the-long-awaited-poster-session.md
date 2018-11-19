---
title: WASSA and EMNLP&#58; the loneliness of the long awaited poster session
---

Just back from presenting a paper at WASSA,<sup>1</sup> here are some thoughts on the workshop and wider conference.

<h2>Venue</h2>

Both the conference and the workshop took place at Square, a conference centre right in the centre of town. Considering the massive amount of attendees (c. 2,500), they didn't do too bad a job of organising everything. Coffee break snacks were not up to LREC 2018 standards, but then that was Japan.

One area where organisation broke down a little was in the poster sessions – more on that later.

The view from the 3rd floor:

![Square and Brussels](/assets/brussels.jpg)

Another thing was security, which noone seemed to be bothered about at any other conference I've been to. Here there were bag searches on every entry. I think this may be a Belgium thing.


<h2>WASSA</h2>

Despite some ongoing technical hitches with the screens, the workshop opened with an invited talk by Elen Riloff on identifying affective events and the reasons for their polarity. She suggested that around 40% of events have affective polarity, and presented work on classifying these according to a set of 'human needs', such as physiological, health & safety, financial and social needs.

Following this were the paper presentations, of which the interesting points for me were the following:

The first of many mentions this week of AllenNLP's ELMo word embeddings tool in Ilić et al.'s sarcasm detection paper.<sup>2</sup>

Saroufim et al.<sup>3</sup> pointed out that word embeddings can fail to work for sentiment analysis tasks as words may map to other words of opposite polarities. So they trained wordf embeddings with encoded sentiment, and it seemed to work.

Emily Öhman presented a gamified tool for crowd-sourced emotion anotation<sup>4</sup> based on Plutchik's wheel:

![Plutchik's Wheel](/assets/Plutchik-wheel.svg)

There were several presentations on the WASSA shared task which concerned predicting emotion without obvious 'triggers' such as emoticons or words like 'happy'. Ultimately, it seems you need to work for a company with a lot of resources and data if you want to win this, or at least it helps.

Related somewhat to both sentiment and language drift, fellow IT&C at KU graduate Jan Lukes showed us that the polarity of words can change over time<sup>5</sup>, and that models trained on historical data tend to perform poorly. He used [reservoir sampling](https://en.wikipedia.org/wiki/Reservoir_sampling) of tweets from different time periods and then a fixed feature set across these to ensure that novel expressions wouldn't effect results.

The work most similar in aim to that of my project was that of Bhatia and P, who used LDA and sentiment analysis to perform 'topic specific sentiment analysis'<sup>6</sup> in an attempt to identify the political ideology of members of Congress. Why wouldn't LDA work for me again? Because LDA tends to discover neutral topics rather that policies to which one might have an opinion. Here they use party labels to represent ideology, but, in our case at least, we're not interested in predicting party affiliation – we already know it. Want we want to find out is *within*-party variation on policy topics, so the approaches used here are not really suitable.

<h3>WASSA poster session</h3>

This is where things got chaotic. Inevitably, the presentations overran, and what was already programmed to be a short session (70 mins) ended up as more like half an hour. On top of this, there was no designated WASSA area, so we hung our posters randomly in a coffee break area that already had a very home-time feel to it. As a consequence, I only spoke to a handful of people. Here's my poster and a few members of the sparse crowd:

![my poster](/assets/wassa_poster.jpg)

<h3>EMNLP</h3>

At the main conference, the most interesting session for me was the Evolution / Sociolinguistics track. Here, among other things:

Ian Stewart presented work on factors that influence the growth and decline of non-standard words.<sup>7</sup> A big factor in the stickiness of a new word is apparently its dissemination across multiple topical or grammatical categories. 

Familiar face Dirk Hovy showed how features of dialect continuum enable a lot of cool stuff to be done to identify and visualise regional variations even when named entities are removed from text. Some fancy retrofitting technique makes things even better.<sup>8</sup>

And Eric Holgate gave a talk on inference of swear word intentions, which can be used to improve performance in hate speech detection.<sup>9</sup> 

<h2>Social event and dinner</h2>

![Museum](/assets/dinner.jpg)

The social event/dinner was held in spectacular surroundings in the Oldmasters Museum and featured champagne, caviar, salmon and several Breugel paintings, which could inspire my next poster. Some people even complained that it was *too good*:

<blockquote class="twitter-tweet" data-cards="hidden" data-lang="eu"><p lang="en" dir="ltr">It does not need to be that fancy, <a href="https://twitter.com/emnlp2018?ref_src=twsrc%5Etfw">@emnlp2018</a> <a href="https://twitter.com/hashtag/emnlp2018?src=hash&amp;ref_src=twsrc%5Etfw">#emnlp2018</a>. Please, future conferences, save the money and make the fee cheaper. It&#39;s tax payers money for many attendees. <a href="https://t.co/fIr1OV4A2t">pic.twitter.com/fIr1OV4A2t</a></p>&mdash; Roman Klinger (@roman_klinger) <a href="https://twitter.com/roman_klinger/status/1058787726617653255?ref_src=twsrc%5Etfw">2018(e)ko azaroaren 3(a)</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


<h3>References</h3>

In Proceedings of the 9th Workshop on Computational Approaches to Subjectivity, Sentiment and Social Media Analysis.
Association for Computational Linguistics:

1. Abercrombie, G. and Batista-Navarro, R. 2018. *Identifying Opinion-Topics and Polarity of Parliamentary Debate Motions*. 

2. Ilić, S., Marrese-Taylor, E., Balazs, J.A. and Matsuo, Y., 2018. *Deep contextualized word representations for detecting sarcasm and irony*.

3. Saroufim, C., Almatarky, A. and AbdelHady, M., 2018. *Language Independent Sentiment Analysis with Sentiment-Specific Word Embeddings*.

4. Öhman, E., Kajava, K., Tiedemann, J. and Honkela, T. 2018 *Creating a Dataset for Multilingual Fine-grained Emotion-detection Using Gamification-based Annotation*.

5. Lukeš, J and Søgaard, A. 2018 *Sentiment analysis under temporal shift*.

6. Bhatia, S. and P, D., 2018. *Topic-Specific Sentiment Analysis Can Help Identify Political Ideology*.

In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing:

7. Stewart, I. and Eisenstein, J. 2018 *Making "fetch" happen: The influence of social and linguistic context on nonstandard word growth and decline*.

8. Hovy, D. and Purschke, C. 2018 *Capturing Regional Variation with Distributed Place Representations and Geographic Retrofitting*.

9. Holgate, E., Cachola, I., Preotiuc-Pietro, D. and Li, J.J. 2018 *Why Swear? Analyzing and Inferring the Intentions of Vulgar Expressions*.