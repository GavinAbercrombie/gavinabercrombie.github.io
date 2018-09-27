---
title: What is the gold in gold standard labels for NLP?
---

Some meandering thoughts on labelling for supervised text classification.

I’ve recently had a couple of experiences presenting work on supervised text classification to people from other fields who expressed bafflement that we would ever consider evaluating anything with labels that we know not to be entirely reliable. I myself was pretty surprised by the idea that there could exist labels for any task that can be considered to be 100% reliable. I’m just so used to considering labels to invariably be both noisy and systematically biased. Which poses this question:

<blockquote><em>Even though annotated corpora represent a gold standard, the question is, what is the gold in the standard?</em></blockquote> 
<div style="text-align: right">Oxford handbook of Cognitive Science<sup>1</sup></div>

There are two typical ways of obtaining labels for supervised classification: 
(1)  Automatic collection of some element of metadata that is assumed to represent the value of the category in question. Typical examples of the this in NLP are hashtag terms for tweet classification and star ratings for sentiment analysis of Amazon reviews. 
(2) Manual labelling by external annotators–either supposed experts in the domain/task or non-experts crowdsourced using platforms such as Amazon Mechanical Turk or Crowdflower.

Method 1 is prone to some noisiness resulting from things like human error, carelessness and mischief, as well as systematic bias due to the way in which different types of people use or apply the elements that are used as labels. For example, it has been shown that Amazon users are systematically more or less generous with the number of stars they award products depending on which country they are from.<sup>2</sup> This type of label is convenient and cheap to obtain, but there are often untested assumptions about the extent to which they really the represent the target phenomenon (e.g., sentiment, sarcasm) in question. 

Using method 2 meanwhile, we encounter other problems. No matter how expert the experts are, most problems in NLP are hard, and total annotator agreement is extremely rare. There can be several reasons for this ‘hardness’ including syntactic and semantic ambiguities inherent in natural languages and the necessity of having access to contextual information and shared knowledge necessary to resolve these ambiguities. Additionally, for many tasks, annotators don’t have access to knowledge of the ‘private states’<sup>3</sup> of emotion or attitude of the people who wrote the text that are necessary for 100% confidence in the accuracy of the labelling. 

So, if we don’t, and indeed can’t, have access to the ‘ground truth’, what do our labels represent? Which method produces labels that are closer to this truth? And what does it mean for a classifier to be able to predict them? 

There are pros and cons to both methods. The automatically collected labels have often been applied by the authors of the text–the only people who can be certain of the meaning, but are subject to the biases mentioned previously. Manually annotated labels may be free of those biases but contain other systematic biases, and are applied by people who usually don’t have full access to the context in which the text was produced.

In my current work, we have three sets of labels: one set obtained by method 1, and two sets by method 2: the ‘gold standard’ annotations, and those of a second annotator (used for validation). Inter-annotator agreement is very similar to rates of co-occurrence between the automatically collected and the manually annotated labels, so it’s hard to say which ones are closer to the elusive ground truth. 

But, to justify having gone to the bother of creating them, we hope our gold standard is ‘better’. And experiments suggest that they may be: when trained and tested using only text features, classifiers predict more of the manual labels ‘correctly‘ than the vote labels (but only just). We claim that the manual labels are more reflective of the phenomena of interest (the  sentiment of speakers in debates), while the automatically collected labels primarily represent something else (speakers’ voting intentions).

So, in the absence of ground truth labels, it must be the nature and objectives of the task that give meaning to the gold standard labels:

<blockquote><em>The value of the gold derives from the task definition for the annotation effort, which in turn derives from combined judgements about practicality and utility on the part of developers.</em></blockquote>
<div style="text-align: right">Oxford handbook of Cognitive Science</div>

That probably sounds pretty unsatisfactory if you’re used to hard logic and reasoning, but in NLP it’s generally all we have and it seems to work okay for many practical applications. As an aside, this problem has been addressed, particularly for computer vision, and a number of approaches have been proposed for taking into account the level of noise in the labels.

<h3>References</h3>

1. Nirenburg, S. and McShane, M., 2016. Natural language processing. The Oxford Handbook of Cognitive Science, p.337.
2. Hardt, D., & Wulff, J. (2012). What is the meaning of 5*'s? An investigation of the expression and rating of sentiment. In KONVENS (pp. 319-326).
3. Quirk, R., 1985. A comprehensive grammar of the English language. Longman.
