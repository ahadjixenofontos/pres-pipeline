### <font color="#008080"> How to build a data analysis pipeline </font>

<br>
Athena Hadjixenofontos, PhD
<br>
Director of Engagement
<br>
Center for Computational Science
<br><br>
ahadjixenofontos@miami.edu
<br>

---

@title[Roadmap]
## <font color="#008080"> Roadmap </font>

- What is context?
- The stages of data analysis
- Design
- Implementation
- Inference
- Assumptions and bias 
- Miami-Dade County 311 calls 


---?image=images/bowl.jpg

@title[Context]

<span style="color:teal">**context** </span> 
<br>
*noun* | con·text
<br>
<span style="color:teal">1:</span> the parts of a discourse that surround a word or passage and can throw light on its meaning
<br>
<span style="color:teal">2:</span> the interrelated conditions in which something exists or occurs

Note:
We hear the word context a lot. The historical context of the times, quotes being taken out of context, but a deeper relationship with what that actually means is part of our objective today. 

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
<img src="images/data-analysis-overview.001.jpeg" height="550">

@title[Pipeline overview]

Note:
As anyone who's ever done research, whether in an academic context or in the R&D department of a company can tell you, there's a lot that has to happen before you get to a place where you can make inference. 

A pipeline for your data analysis includes the following, very broadly defined stages:
In the design phase, you sharpen the question, make sure you have what you need to answer it
In the implementation phase, you dive in deep with the data, explore it, clean it, play with it and develop your intuition about it
In the inference stage, you build models, evaluate them, create visualizations and communicate the insights

The decisions you make along the way will be informed by the context of your data analysis. Two people can start at exactly the same place in terms of what data and methods are available to them and ask very similar questions, but the sight differences in their objectives will translate to different actions being appropriate at each stage. 

---

@title[Design]

## Design phase 
##### Don't take shortcuts. 

+++?image=images/path-in-focus.jpeg

Note: 
The first thing you often do is read the literature. Where is the field? How have the questions you are interested in been asked before? 

The question that you seek to answer with your data analysis exists in the context of a long history of other people who have asked very similar questions. What approaches did they take? What's different about now? What obstacles did they encounter and how did they overcome them? 

This is a great way to bring the picture into focus, hone in on what you really actually are asking.

+++

> If I have seen further than others, it is by standing upon the shoulders of giants. 
>  <br> <font color="#008080">Sir Isaac Newton </font>

+++

> If I asked my customers what they wanted, they would have said "a faster horse". 
> <br> <font color="#008080">Henry Ford </font>

Note: 
There is some art in how you form the question. You don't want it to be so general that it is meaningless, but you also don't want it to be so specific that it traps you inside a specific solution. 

In general, it is better to state the problem and keep that statement free of any methods or specific approaches. 

It is the difference between:
"How do my employees personalities influence their performance?"
and
"How can I use text data to predict my employees performance based on their personalities?"

+++

A <font color="#008080"> good question </font> is:
- informed by the literature
- answerable with the data available to you
- answerable with the methods available to you 
- falsifiable

Note: 
Reading the literature will take you from talking about employee personalities, in a very general and abstract sense, to thining about dimensions of personality that can be measured with the Five-Factor Personality Test and the other established and validated ways of measuring what you are interested in. 

If there is no established way to measure what you are interested in you are either still thinking about it too abstractly, or you have one more step that you have to complete before you can embark on your analysis. 

If you are using survey instruments check things like the face validity of your survey, which is usually judged by an expert, but also features such as the test-retest reliability and the internal consistency of the measures that are captured by the survey. 

+++?image=images/notepad.jpeg

<font color="#008080">Example: </font>	
<br>
- General domain: employee performance
- Available data: unstructured text data from CVs, emails, performance reviews
- Available methods, infrastructure: any, unlimited

Note: 
Let's spend a couple minutes thinking about this example. What else would you want to collect, if you had the freedom to? 

+++

Beware of your assumptions. 
<br>
They define the questions that you will think to ask. 

Note:
My favorite example here is the birth of the field of neurogenesis. 
For a long time, the dogma was that the last time that new neurons are born is during development.
A pair of researchers, Altman and Das, published evidence of adult neurogenesis in the best journals, in the 60's, but they were largely ignored by the scientific community. 

That wasn't enough to overturn the dogma that adult brains don't make new neurons. More researchers published evidence in the 70's, and drama ensued. Careers were destroyed by a combination of criticism and lack of support. The very things that we hold in highest regard, not extending inference of findings based on model organisms to humans, worked against us in this case. The first studies were done in birds, and a very influential researcher Pasko Rakic published a paper in Science, convincing researchers that adult neurogenesis was restricted to birds and rodents, and didn't happen in primates. It took another 20 years for the field to recover. Neurogenesis is now an entire field, and we know that it may have a role in learning and memory. 

Hindsight is 20-20. It's not that it's hard to keep an open mind, it's the idea of how far do you take a notion for it to require "an open mind?". What does the data say? Has there been data collected on adult neurogenesis in primates? That was a question that we maybe wouldn't even think to ask if not prompted by the studies in birds and rodents. 


+++?image=images/gage-neurogenesis.png

Note:
In this paper from 1995, a group of researchers looked at the dentate gyrus, which is a region of the hippocampus that undergoes neurogenesis. 
They show that cells isolated from that region can be cultured in vitro, and they can survive, proliferate and express neuronal and glial markers. They also labelled the cultured cells so that they could track them, and transplanted them back in the brain of a rat. Two months later they found labelled cells that had matured and differentiated into neurons. 

+++?image=images/camera.jpeg

Give yourself a point of reference. 

Note:
Going back to our previous example with employee engagement based on employee personality, let's say that you came up with an awesome way to describe employee personality based on the text data that is available. 
How do you know that the personality that you detected is indeed the true personality of that person? 
(wait for their answer)

Experimental scientists call these controls. How do you know that a high performer is a high perfomer? 
Even more crucial if you have an intervention as part of your data. How do you know that the system you set up will produce a negative result when you expect a negative result and a positive one when you expect a positive result? If you see a negative result is it because the intervention, even when present, doesn't work or is it because the intervention wasn't actually present to begin with?

+++ 

Setting a baseline is easier in some cases than in others. 
<br>
<br>
It is <font color="#008080">essential</font> in giving yourself a clear context for the interpretation of your results. 

Note: 
You really need to think through, before you embark on your analysis, "if I see this, what will it mean?" 
Do you need additional information to be able to interpret your observation? 
Can you bring that information into your analysis? 

This is also the purpose of a pilot study, where you can figure all of this out before spending lots of times and money on a big scale study that turns out to be inconclusive. 

Be deliberate and thorough. 

+++

#### Seeing Black: Race, Crime, and Visual Processing

<br>
<br>
**Population:** 41 white, male, UC Berkeley and Stanford university students
<br>
<br>
**Approach:** subliminal exposure of participants to face stimuli for 30ms, then exposure to object stimuli

Note:
Psychology and the social sciences in general, are notorious for bad study design and as the fields that struggle with replication the most. They were the last to catch on and start using the scientific method, and with good reason! The number of variables that become relevant when we are talking about human behavior is intractable and the systems are complex. This is in contrast to systems that are deterministic, controlled by a small number of variables and can be modeled explicitly. Physicists and engineers actually have it easy, because they are the most likely to work with these systems in which you can model every component explicitly. 

The conversation about how to think of complex systems can fill years and years of courses and study, so they key thing to take away from our conversation today is that designing a project that involves complex system will be different than working in a deterministic context, and you need to account for that in your design. 

Automatic stereotyping is the idea that the mere presence of a person can lead one to think about the concepts with which that person's social group has become associated. 

In this study, a group of four researchers designed an experiment where they sought to establish that exposure to black faces can decrease the perceptual thresholf for recognizing crime-related objects, to test the possibility that the stereotypic association between blacks and crime influences visual processing. 

face stimuli: color photographs of 50 Black or 50 White young adult male faces, or no face/random lines stimulus for 30 ms
object stimuli: 2 types object images (gun or knife) and (book or camera) 

+++
<img src="images/guns.png" height="350" >

+++
<img src="images/seeing-black-results.png" height="500" >
<br>
What else could have generated these results?

Note:
After subliminal exposure to Black face primes, fewer frames were required to detect crime-relevant objects in comparison with crime-irrelevant objects t(13) = 2.96, p = 0.01

Were all the images equal in 

Did the photographs have more angry faces in one group than in the other? 
Other differences? Better dressed? Different backgrounds?

Was it a difference in attentional bias rather than a true difference in visual processing? 
What influences attentional bias? How do you measure it?

+++

#### Statistical power

... or the probability that you will be able to distinguish between a true effect of a certain size and chance. 
<br>
<br>
**Exercise:** 
<br>
Plot power curves for a two-tailed t-test, using pwr in R

Note:
Switch to RStudio

+++

#### Quality Control

Identify QC metrics that you will use, ahead of time if possible. 
<br>
<br>
Think back to our employee performance example. 
<br>
Do we expect any features of data collection to impact the quality of data that we get? 

Note:
Rate of missingness is a big one, does it matter for your analysis whether or not you have lots of missing data? Does it indicate that something went wrong with the rest of the data that belongs to that same observation or are all values for that observation independent? 

+++

#### Database format
Think about:
- Appropriate data types
- Being able to easily query it!
- Minimizing wrangling

Note:
If you have any say in how the database that receives the data is designed, then use that to help you avoid as much tricky data wrangling as possible. 
A data scientist should not also be a data engineer, in my opinion, it's just too much work for one person, but they should work closely together. 

Export a small sample of what it looks like, take it through a draft of your pipeline and see what you can improve. 

If you don't think about this last point ahead of time, you will be adding steps to your pipeline where you are formating your data in preparation for being able to dive into it. 

+++

### Think it through. 

---

@title[Implementation]

## Implementation phase 
##### Go to town! 

+++

<img src="images/data-analysis-overview.002.jpeg" height="550"> 

+++

<img src="images/data-analysis-overview.003.jpeg" height="550"> 

+++

<img src="images/data-analysis-overview.004.jpeg" height="550"> 

+++

<img src="images/data-analysis-overview.005.jpeg" height="550"> 

+++

The goal of quality control is to gain trust in your data. 

+++

Dig deep by following the bread crumbs.  
<br>
<br>
Some of the clues that your data is unreliable may be a surprise and difficult to uncover. 

Note: 
Data is messy. That's okay. It's not a reflection on you (well it may be, if you didn't take the design phase seriously) and in any case, you want to be the one to find out 

+++

### Descriptive statistics
Check the distributions of all key variables. 
	- Averages, standard deviation, range, frequency tables
	- Outliers 
	- Rates of missingness
Drop observations if appropriate. 
Preliminary visualization of relationships between variables.
	- Scatterplots, boxplots, braplots, frequency tables 

+++

### <spanDimensionality reduction
- For multidimensional data, you have options:
	- Use a decision tree to identify which variables are important
	- Look at the correlation between all variables and use a metric to decide which to drop
	- Backward or forward feature selection if you are using regression
	- Latent factor analysis
	- Collapse the dimensions onto their major axes of variation

Note:
Random Forests are a special case of that first bullet. They are biased towards continuous variables, so you need to keep that in mind if you have binary or categorical variables that you expect will be important to keep. 

The method you choose depends on the data that you have, and what you set as your priorities.
Resulting dimensions are less interpretable. 

+++?image=images/ms-pca.jpg

+++

### Take away:
Your choice of how to deal with multiple dimensions will impact how the information is undestood and interpreted. 

The effect is even more pronounced in high-dimensional data, where your choices will include which dimensions to highlight and which to ignore. 

+++?image=images/dimensions_xkcd.png

+++

Build a modular pipeline. 
<br>
Your choices of where to break up the various operations will impact the ease with which you or other researchers can repurpose your tools for other analyses.

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

**Example**
Some personality traits predict behaviors, to varying extents.

**Message** 
Resist the urge to fill in the blanks. 

Note:
In our employee personality and performance example, it would be a jump to go from talking about the traits that you have measured, infer behavior and then somehow try to link those behaviors to their performance! 

If you found that employees with high individualism, which is the tendency to focus on oneself and one's personal goals, perform better at public presentations, it would be a leap to assume that it's because they prefer to engage in behaviors that make them stand out from others, even though that behavior is correlated with individualism in the literature. 

Fortunately, leaps are also known as hypotheses, so you could devise a follow up study to see if that is indeed true. 

Academics tend to care more about mechanism than business people. It's the difference between wanting to know WHY individualists perform better at public speaking, and only wanting to know THAT individualists perform better at public speaking - which is actionable information. 

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

