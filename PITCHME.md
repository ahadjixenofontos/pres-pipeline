@title[Title slide]

# How to build a data analysis pipeline
<br>
### Athena Hadjixenofontos, PhD 
#### Director of Engagement
#### Center for Computational Science

<br>
ahadjixenofontos@miami.edu

---

@title[Roadmap]
#### Roadmap

1. Birds eye view of data analysis
1. Conceptualize the study: what is the question you want to answer? It will be abstract
	1. eg medical care access and disease
1. Subjectivity in science OR The importance of context OR Validity is in the eye of the beholder
    1. Obvious examples
    1. Subtle examples
1. Mapping the steps of data analysis (conceptual) on to the parts of a pipeline (operational)
1. Forms of bias
1. Assumptions in data collection 
1. The quality control process is also context dependent
1. Assumptions in statistical modeling
1. Not all roads lead to Rome OR There are more than one ways to write an algorithm
1. Visualization decisions
1. Sharing makes code better


---?image=images/paper.jpeg

@title[A thing I thought I knew]

**Context**:
A thing I thought I knew.

Notes:
We hear the word context a lot. The historical context of the times, quotes being taken out of context, but at least for me, a deeper relationship with the word context didn't develop until I was about 22, and a first year graduate student. 

I'll start with two familiar examples, one is about gender and the other involves Margaret Atwood. What does gender and Margaret Atwood have to do with data analyses? I am using them as the initial examples to calibrate our intuition, they are clearer to grasp, less ambiguous, than the ones we're about to dive into, and they are also just what I have. 

---?image=images/wooden-bowl.jpg

@title[Gender]

Notes:
The first time I realized I didn't actually know what context really is was while volunteering at a local Miami non-profit. They graple with the nuances of context a lot, because their work includes conversations around gender.  

The reason why context is especially important in gender conversations I think is illustrative. 
In the context of a Catholic monastery in Colombia, deviations from gender norms are understood  one way, whereas in the context of a Unitarian church in South Miami, they are understood a different way. 

It would appear that context impacts the interpretation of an observation, which I think is the first layer of this deep onion we are peeling today.

Science is all about the interpretation of observations. 
We think of it as an objective truth, we see numbers and we assume that since something is quantified it must be unbiased. 
Even though we know that interpretations of observations are only meaningful within a specific context. 

---

@title[Context is invisible]

The water that we are swimming in

---?image=images/handmaids-tale.jpeg

@title[Margaret Atwood]

Margaret Attwood quote about Handmaid's Tale context changing on Nov 9. 

---

@title[Revealing my biases]

To be honest I struggled with whether to reveal so much of myself in this talk, but then had the thought that this is the context that frames my thoughts. 
It would not be fair to ask you to listen to me, and maybe even accept my thoughts, without some insight into my biases, 
the influences that shaped them and which provided context for them. 

---

@title[Positivism vs ]

---

@title[Design: Language and ambiguity]


I mentioned the word ambiguous earlier. That's a concept that is very familiar to programmers, largely because they have experience 
with tools that are less ambiguous, programming languages. 

So you see, language is creating our reality. That's a deeper idea that we won't really go into today. 

http://www.pnas.org/content/pnas/110/35/14196.full.pdf

---

@title[Design: Points of reference]

Controls. Setting expectation. 

---

@title[Design/Implementation: Real data is messy]

Quality control metrics.
Some of them will flow out of expected biases of data collection. 
Some of them will be a complete surprise to you, which is why it's really important to dig deep.  

---

Clean data is good data. 
Sometimes cleaning data means throwing it all out. 
There is no baby in this bathwater. 


---?image=images/data-analysis-overview-slide1.pdf

@title[Data analysis overview]

Notes:


+++?image=images/data-analysis-overview-slide2.pdf

+++?image=images/data-analysis-overview-slide3.pdf

+++?image=images/data-analysis-overview-slide4.pdf


---

@title[Implementation: uncertainty and statistics]

Population parameters vs sample estimates
Statistical bias: estimate differs from underlying parameter value

+++

Correlation vs causation
Xkcd correlation panels

+++

Statistical power
Should really be in design section

+++

Statistical significance

+++

Communicate uncertainty in your visualizations

+++

**Your design, analysis, implementation and visualization decisions provide the context for the interpretation of your results.**

+++

Meta means after
Meta analyses 

+++

All models are wrong but some are useful

+++

How would your understanding of this section change if I had put that last slide first? 

---

@title[Biases and assumptions]

We don't see things as they are, we see them as we are. 
-Anais Nin

+++

Perception is limited to what our senses (and sensors we design) can perceive
https://www.facebook.com/quartznews/videos/191332488127750/

+++

Biases in data collection. 
Ascertainment bias. 

+++

Cognitive biases. 
Covered in multiple other sources. 

+++

Knockout mouse line where gene was knocked out from all tissues but turns out that some tissues still express that protein 
Tool that you expect will work a certain way but doesn’t
If you continue using it as if it does what you assume you’ll misinterpret the results 

+++

Dogma changing assumptions 
No new neurons
Neurogenesis is now an entire field
And may have a role in learning and memory 
For a long time people were completely blind to those neurons and their effects 

+++

Assumption that to keep someone’s heart beating you needed to cut the chest open and do t manually so for a long time we were unnecessarily cutting the chest open 
That assumption was wrong 
You can just do cpr 

+++

We categorize, that’s what we do 
Based on general associations we’ve learned about those variables but they don’t always hold true 
They are useful because testing all of them takes time and resources 
Identify and test the key ones for your study 

+++

Assume that your code implementation is correct
Example of evolutionary biologist who retracted the paper

---

@title[Interpretation]

Example of misplaced causality
My mom does this a lot. Undue inference. 
Won't be so obvious when you are dealing with things that are not intuitive. 

Successful big tech and company culture or managerial styles

---

Controls. Controls. Controls.
<br>
Controls.
Controls provide the context. 

http://www.apa.org/monitor/jan05/visual.aspx
Sounds straightforward right?
What if the association was with the average color of the picture than with a racial bias?


The group that is associated with guns should then also be identified in a population of people
who have white hunters associated with guns
How do we know that it was the white male college student's association of black men with guns that generated the result? 
What else could have done it?

---

@title[So what do I do?]

You don’t know what you don’t know
But what you can know is that you don’t know
To be aware of your biases
This goes against our culture
Gap between business world

What are you blind to? Easy to ask but difficult to answer because hindsight is 20/20

The point isn’t to catch yourself because it’s guaranteed that you won’t
Try your best and be aware that “your way is not the best” even when you do become an expert 

---

@title[Miami-Dade County 311 data]



---

Barriers 

+++?image=images/fast-train.jpeg

We want to go fast and take shortcuts.
Instant gratification.  

+++?image=images/business-man.jpeg

Culture of knowing. 
Business vs science circles.

+++?image=images/inquisitive-kid.jpeg

It's exhausting! Not humans' default state of being to be inquisitive about their biases.  

+++

When you start diggint, you realize that there's always more to know! 
More ways in which you can make your study less biased, more objective, more interpretable. 
Where does it end? 
I cannot help you with that. 

Notice I didn't say "objective", I said "more objective". I don't know that untainted objectivity is attainable. 

+++

If you truly want to let the data speak for itself, you need to get yourself out of the way. 
Won't always be possible. And that's also (in some cases) okay. 

---

Develop your data analysis intuition. 
Practice. 

---


<br>
My <span style="color:blue">words in color.</span>
<br>
---

@title[]

* bullet
    * sub-bullet
<br>
1. first element 
1. second element
    1. subelement 

---?image=images/bunny.jpg

@title[Image as background]

<br>
Goodnight. I am a sleepy bunny. 
<br>

+++

@title[Image in slide]

<img src="images/bunny.jpg" width="150" height="150">
<br>
There's a bunny on this slide. 
<br>

---

@title[Code slide]

```
import numpy as np

dat = open('file.csv', 'r')
emtpy = numpy.zeros(10)

```
@[1]
@[2-4]

