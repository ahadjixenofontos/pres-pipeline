unused material

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


---?image=images/monastery.jpeg

@title[Gender]

Note:
I'll start with two familiar examples, one is about gender and the other involves Margaret Atwood. They will serve to calibrate our intuition, because they are clearer to grasp, less ambiguous, than the ones we'll dive into when it comes to data analysis. 

The first time I realized I didn't actually know what context really is was while volunteering at a local Miami non-profit. They graple with the nuances of context a lot, because their work includes conversations around gender.  

The reason why context is especially important in gender conversations I think is illustrative. 
In the context of a Catholic monastery in Colombia, deviations from gender norms are understood one way,

---?image=images/miami-beach.jpeg

Note: 
 whereas in the context of South Beach, they are understood a different way. 
---

@title[Context is invisible]

The water that we are swimming in

---?image=images/handmaids-tale.jpeg

@title[Margaret Atwood]

Note:
Margaret Attwood quote about Handmaid's Tale context changing on Nov 9. 

---

@title[Revealing my biases]

To be honest I struggled with whether to reveal so much of myself in this talk, but then had the thought that this is the context that frames my thoughts. 
It would not be fair to ask you to listen to me, and maybe even accept my thoughts, without some insight into my biases, 
the influences that shaped them and which provided context for them.

---

> Heisenberg 

---

> Popper

---

@title[Philosophy of language]

Language creates reality. 	

Note:
I would be remiss to not mention that these ideas have been explored very deeply, in a field called the philosophy of language. It is incredibly fascinating. 

---



So you see, language is creating our reality. That's a deeper idea that we won't really go into today. 

http://www.pnas.org/content/pnas/110/35/14196.full.pdf

---
+++

How would your understanding of this section change if I had put that last slide first? 

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


+++

You assume/hope that your code implementation is correct
Example of evolutionary biologist who retracted the paper

---

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



---

@title[Barriers] 

+++?image=images/fast-train.jpeg

We want to go fast and take shortcuts.
Instant gratification.  



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
