### How to build a data analysis pipeline

<br>
#### Athena Hadjixenofontos, PhD 
##### Director of Engagement
##### Center for Computational Science
<br>
ahadjixenofontos@miami.edu
<br>
---

@title[Roadmap]
### Roadmap

- Intuitive examples
- The stages of data analysis
- Statistics in context
- Assumptions and bias 
- Decision-making for the analysis of Miami-Dade County 311 calls 


---?image=images/paper.jpeg

@title[Context]

**context**
<br>
*noun* | con·text
<br>
2: the interrelated conditions 
<br>
in which something exists or occurs

Note:
We hear the word context a lot. The historical context of the times, quotes being taken out of context, but at least for me, a deeper relationship with the word context didn't develop until I was about 22, and a first year graduate student. 

I'll start with two familiar examples, one is about gender and the other involves Margaret Atwood. They will serve to calibrate our intuition, because they are clearer to grasp, less ambiguous, than the ones we'll dive into when it comes to data analysis. 

---?image=images/monastery.jpeg

@title[Gender]

Note:
The first time I realized I didn't actually know what context really is was while volunteering at a local Miami non-profit. They graple with the nuances of context a lot, because their work includes conversations around gender.  

The reason why context is especially important in gender conversations I think is illustrative. 
In the context of a Catholic monastery in Colombia, deviations from gender norms are understood one way,

---?image=images/miami-beach.jpeg

Note: 
 whereas in the context of South Beach, they are understood a different way. 

---

Context has consequences 
<br>
for the interpretation of an observation. 

Note:
So context has consequences for the interpretation of an observation, which I think is the first layer of this deep onion we are peeling today.

Science is all about the interpretation of observations. 
We think of it as an objective truth, we see numbers and we assume that since something is quantified it must be unbiased. 
Even though we know that interpretations of observations are only meaningful within a specific context.  


---?image=images/data-analysis-overview-slide1.png

@title[Data analysis overview]

Note:


+++?image=images/data-analysis-overview-slide2.png

+++?image=images/data-analysis-overview-slide3.png

+++?image=images/data-analysis-overview-slide4.png

---

@title[Design]

## Design phase 
##### Don't take shortcuts. 

+++?image=images/path-in-focus.jpeg

> If I have seen further than others, it is by standing upon the shoulders of giants. 
> - Sir Isaac Newton

Note:
Where is the field? What is your starting point? Have others asked similar questions before you? What was their process?

By reading the literature you will not only stand on the shoulders of giants in terms of choosing the appropriate methods, you will also develop an intuition for what can go wrong, and how to fix it. 

You will be better able to anticipate the obstacles that will come up. 

+++

A good question is:
- informed by the literature
- answerable with the data available to you
- answerable with the methods available to you 
- falsifiable

+++?image=images/notepad.jpeg

Example:
<br>
- General domain: employee engagement
- Available data: unstructured text data from CVs, emails, performance reviews
- Available methods: any, including NLP, regression etc.  

####Can you think of an example of a good question?

+++

<img src="images/diagonals.jpg">

Beware of your assumptions. 
<br>
They define the questions that you will think to ask. 

Note:
My favorite example here is the birth of the field of neurogenesis. 
For a long time, the dogma was that the last time that new neurons are born is during development.
Neurogenesis is now an entire field
And may have a role in learning and memory 
For a long time people were completely blind to those neurons and their effects 

+++?image=images/camera.jpeg

Give yourself a point of reference. 

Note:
Going back to our previous example with employee engagement based on employee personality, let's say that you came up with an awesome way to describe employee personality based on the text data that is available. 
How do you know that the personality that you detected is indeed the true personality of that person? 

+++ 

Setting a baseline is easier in some cases than in others. 
<br>
Be deliberate and thorough. 
<br>
#### This is how you give yourself a clear context for the interpretation of your results. 

Note: 
You really need to think through, before you embark on your analysis, "if I see this, what will it mean?" 
Do you need additional information to be able to interpret your observation? 
Can you bring that information into your analysis? 

This is also the purpose of a pilot study, where you can figure all of this out before spending lots of times and money on a big scale study that turns out to be inconclusive. 

+++

#### Seeing Black: Race, Crime, and Visual Processing

#### The study

N = 41
<br>
**Population studied:** white, male, UC Berkeley and Stanford university students
<br>
**Approach:** expose participants to face stimuli, then object stimuli (took shape over 41 frames)

Note:
Psychology and the social sciences in general, are notorious for bad study design and as the fields that struggle with replication the most. They were the last to catch on and start using the scientific method, and with good reason! The number of variables that become relevant when we are talking about human behavior is intractable and the systems are complex. This is in contrast to systems that are deterministic, controlled by a small number of variables and can be modeled explicitly. Physicists and engineers actually have it easy, because they are the most likely to work with these systems in which you can model every component explicitly. 

The conversation about how to think of complex systems can fill years and years of courses and study, so they key thing to take away from our conversation today is that designing a project that involves complex system will be different than working in a deterministic context, and you need to account for that in your design. 

Automatic stereotyping is the idea that the mere presence of a person can lead one to think about the concepts with which that person's social group has become associated. 

In this study, a group of four researchers designed an experiment where they sought to establish that exposure to black faces can decrease the perceptual thresholf for recognizing crime-related objects, to test the possibility that the stereotypic association between blacks and crime influences visual processing. 

face stimuli: color photographs of 50 Black or 50 White young adult male faces, or no face/random lines stimulus for 30 ms
object stimuli: 2 types object images (gun or knife) and (book or camera) 

+++?image=images/guns.png

+++

#### The results

<img src="seeing-black-results.png">
What else could have generated these results?

Note:
After subliminal exposure to Black face primes, fewer frames were required to detect crime-relevant objects in comparison with crime-irrelevant objects t(13) = 2.96, p = 0.01

Were all the images equal in 

Did the photographs have more angry faces in one group than in the other? 
Other differences? Better dressed? Different backgrounds?

Was it a difference in attentional bias rather than a true difference in visual processing? 
What influences attentional bias? How do you measure it?

+++

### Think it through. 

+++

Statistical power
Should really be in design section

+++

Quality control metrics.
Some of them will flow out of expected/known biases of data collection. 

+++

Database format

---

@title[Implementation]

Clean data is good data. 
Sometimes cleaning data means throwing it all out. 
There is no baby in this bathwater. 
Some of them will be a complete surprise to you, which is why it's really important to dig deep.  

+++

Descriptive statistics

+++

Preliminary relationships

+++

Dimensionality reduction

+++

Modular building

---

@title[Inference]

Population parameters vs sample estimates
Statistical bias: estimate differs from underlying parameter value

+++

Example of misplaced causality
My mom does this a lot. Undue inference. 
Won't be so obvious when you are dealing with things that are not intuitive. 

Successful big tech and company culture or managerial styles

+++

Correlation vs causation
Xkcd correlation panels

+++

Statistical significance

+++

Meta means after
Meta analyses 

+++

Machine learning

+++

All models are wrong but some are useful

+++

Communicate uncertainty in your visualizations

---

**Your design, analysis, implementation and visualization decisions provide the context for the interpretation of your results.**

---

@title[Biases and assumptions]

We don't see things as they are, we see them as we are. 
-Anais Nin


+++

Knockout mouse line where gene was knocked out from all tissues but turns out that some tissues still express that protein 
Tool that you expect will work a certain way but doesn’t
If you continue using it as if it does what you assume you’ll misinterpret the results 

+++

Assumption that to keep someone’s heart beating you needed to cut the chest open and do t manually so for a long time we were unnecessarily cutting the chest open 
That assumption was wrong 
You can just do cpr 

+++

Perception is limited to what our senses (and sensors we design) can perceive
https://www.facebook.com/quartznews/videos/191332488127750/

+++

Example of interpretation in the context of ascertainment bias

+++

Cognitive biases. 
Covered in multiple other sources. 

+++

We categorize, that’s what we do 
Based on general associations we’ve learned about those variables but they don’t always hold true 
They are useful because testing all of them takes time and resources 
Identify and test the key ones for your study 

+++

You assume/hope that your code implementation is correct
Example of evolutionary biologist who retracted the paper

---

@title[Bottom line]

You don’t know what you don’t know
But what you can know is that you don’t know

Note:
To be aware of your biases
This goes against our culture
Gap between business world

What are you blind to? Easy to ask but difficult to answer because hindsight is 20/20

The point isn’t to catch yourself because it’s guaranteed that you won’t
Try your best and be aware that “your way is not the best” even when you do become an expert 


---

@title[Barriers] 

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

+++

Develop your data analysis intuition. 
Practice. 

---

@title[Miami-Dade County 311 data]


---

<br>
My <span style="color:blue">words in color.</span>
<br>

---

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

