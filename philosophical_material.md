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

--

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
