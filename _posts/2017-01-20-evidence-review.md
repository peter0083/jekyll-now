---
layout: post
title:  "Level of Evidences in Evidence-based Medicine: A Quick Overview"
date:   2017-01-20
tag:
- pharmacy
- drug
- healthcare
- therapeutic
- data science
- stat
- medicine
- EBM
comments: false
---

### Introduction

Patients and friends often approach me with articles they read online about effectiveness or novel indications of drug X or herb Y then ask me about my opinion on these findings. I  have to take a step back and give them a quick tutorial on "not all data are created equal". I feel it is important for empower patients and the public a sense of what different levels of evidence means so they will not be preys of false advertisement. 

Recently, I witnessed a cyber-bully incidence that a group of healthcare professionals posted a blog entry to debunk false claims of plum extract. These highly trained professionals were bombarded with harsh comments by plum-extract fans and sales. Fans and sales used primarily google search to find plum-extract research articles without realizing that the level of evidence was the articles they cited was low. **sad**

In UBC MDS program, we have yet to cover data modelling and inference for randomized controlled trials. This blog post will serve as a high-level preview for my fellow classmates and prospective students.

### How are evidence/data ranked in the medical world?

Here is a music parody made by a UBC pharmacy professor, *Dr. James McCormack*, explaining evidence in an artistic way.

[![IMAGE ALT TEXT](http://img.youtube.com/vi/QUW0Q8tXVUc/0.jpg)](https://www.youtube.com/watch?v=QUW0Q8tXVUc&feature=youtu.be "Viva La Evidence")

Different questions and research topics will have slightly different ranking for evidence and data. (1) I will focus on the evidence for therapy because I have more training in this category.

#### Lowest evidence (level 5): Expert opinion without explicit critical appraisal, or based on physiology, bench research or "first principles"

Expert opinions that draw on our understanding of physiology, test-tube, or animal models are not as strong as many people think. (3) For example, a herbal supplement salesperson claimed that Dr. John Doe supported the use of her product (a mix of different extracts) because Dr. John Doe found this product was effective in his tissue culture experiment. (1) However, many drugs and therapies shown effective in animal or test-tube models may still fail in the human studies. Dr. Doe's opinion is valued but people should not translate his success in tissue culture directly to humans. We cannot rule out possibility of Dr. Doe's personal bias. He could have been an investor of this supplement but he did not disclose this information.


#### level 4: Case series 

Individual cases and reports may carry some weight in evidence hierarchy but, again, it is not the most valuable data. (3) One case report may show that one patient suffering from terminal liver cancer fully recovered after taking this mysterious Dr. John Doe's extract. Statistically, we may suspect that this particular miracle case is simply an outlier. It is not logical for a hospital to start giving all terminal liver cancer patients Dr Doe's extract. 


#### level 3: Case-control studies and systematic reviews of case-control studies

A case-control study is a type of observational study. You probably wonder what is an observational study. An observational study draws inferences from a sample to a population where the independent variable is not under the control of the researcher because of ethical concerns or logistical constraints. (4)

Here is a diagram explaining case-control study from Wikipedia. 

<img src="https://upload.wikimedia.org/wikipedia/en/thumb/b/b5/ExplainingCaseControlSJW.jpg/602px-ExplainingCaseControlSJW.jpg">

Because case-control studies, being observational in nature, are limited by the possibility of having confounding factors (5)

#### level 2: Systematic reviews of cohort studies and individual cohort studies

Cohort studies are a type of longitudinal study (think longitudinal data from Dr. Wu's DSCI 562!). They are better than case-control studies but are also suspectible to confouding factors and bias. 

#### best evidence! level 1: Systematic reviews of randomized controll trials (RCTs) and individual randomized controlled trials (RCTs)

Randomized controlled trials (RCTs) are the best type of data to make inference about a therapy. (5) During randomization, you are minimizing bias and confounding factors of your patient populations. (5) However, RCTs are not always possible in researches. For example, it is simply unethical to gather enough patients for a rare disease to run randomized controlled trials. 

### Take-home messages

<img src="http://i574.photobucket.com/albums/ss187/livinlowcarbman/wilf-logo.jpg?t=1302805457">

This ranking of data and evidence is not written in stone because RCTs are not always possible. I hope this short blog post will get you to start thinking about the quality of evidence presented to you in different situations. 

Reference:

1. Howick J. Oxford Centre for Evidence-based Medicine - Levels of Evidence (March 2009) - CEBM [Internet]. CEBM. 2009 [cited 20 January 2017]. Available from: http://www.cebm.net/oxford-centre-evidence-based-medicine-levels-evidence-march-2009/

2. https://therapeuticseducation.org/videos

3. Burns PB, Rohrich RJ, Chung KC. The levels of evidence and their role in evidence-based medicine. Plastic and reconstructive surgery. 2011 Jul;128(1):305.

4. https://en.wikipedia.org/wiki/Observational_study

5. https://en.wikipedia.org/wiki/Case-control_study

6. https://en.wikipedia.org/wiki/Cohort_study