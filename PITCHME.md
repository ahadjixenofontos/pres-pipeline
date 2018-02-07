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

---

@title[Positivism]

Positivity: 
> "... the degree to which the phenomena can be exactly determined."
> Lester Ward (1898)

**Positivism principles:**
- Verification: a statement is to be judged meaningful if and only if there is a method for verifying it. 
- Falsification: a statement is to be judged meaningful if and only if there is a method for falsifying it.

Note:
This building of an interpretation can be described as a feedback loop that connects observation to the development of theory, which leads to hypotheses on observations that should follow if the theory was put together well. 

In the first half of 1800s, Auguste Compte published a series of volumes called the Course in Positive Philosophy, in which he defines positivity as the degree to which the phenomena can be exactly determined.
In this way he was the first philosopher of science, and these ideas of making inference from observations are what today is about. 

So how exact of a science is data science? How do you set up your analysis such that you can make inference from it instead of be making it up? 

---

@title[Design: Ambiguity]

Natural languages 
<br>
v.
<br>
Programming languages

Note:
Natural languages, such as the ones that we speak, English, Greek, Spanish, are by nature, ambiguous. 
What everyone who programs knows is that programming languages are much less ambiguous, because computers need a concrete, no gaps, set of instructions on exactly what to do. 

We need to be very careful when we combine a question that want to ask of the data, a question which is formed in natural language with the programming required to implement the analysis that will hopefully get you to an answer. 

There is much opportunity to make assumptions when translating from an ambiguous language to an unambiguous one. 

---?image=images/data-analysis-overview-slide1.png

@title[Data analysis overview]

Notes:


+++?image=images/data-analysis-overview-slide2.png

+++?image=images/data-analysis-overview-slide3.png

+++?image=images/data-analysis-overview-slide4.png
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

