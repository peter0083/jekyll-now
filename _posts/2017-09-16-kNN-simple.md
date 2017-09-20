---
layout: post
title:  "k-Nearest Neighbours Algorithm Explained in Plain English (No Code!)"
date:   2017-09-16
excerpt: "k Nearest Neighbour for Everybody"
tag:
- machine learning
comments: true
---


================
================
Peter Lin
2017-09-16

------------------------------------------------------------------------

### k-Nearest Neighbours Algorithm Explained in Plain English (No Code!)

Imagine a case: In a parallel universe far far away, where Donald Trump is a philanthropist known for his mission to bring equality to the world by providing accessible higher education. In that universe, you are a data scientist working for the Trump University finance team.

![future_data_scientist](blogpost_files/figure-markdown_github-ascii_identifiers/tom-cruise-minority-report.jpg)


Image courtesy of `DenofGeek.com`.

:exclamation: *Your task*:

Trump University finance team wants to waive the tuition fees for students who truly need the financial aid. Students who need financial aid will self-report their financial status to the school and the school will compute two scores, `tuition_need` and `unmet_need`. Your task is to predict the liars from the honest students.

:minidisc: *Your data*:

In the past, Trump University randomly audited the self-reported students and sent auditors and detectives to find out their true financial need. In order to standardize the audit process, they would like to apply machine learning to this problem. To achieve this goal, the team gives you 100 student files from the year 2016. For each student file, the finance team provides you two features (`tuition_need` and `unmet_need`) and a label (truth vs lie).


| variable     | data type                  |
|--------------|----------------------------|
| tuition_need | numeric, 1~10              |
| unmet_need   | numeric, 1~10              |
| label        | categorical (truth vs lie) |

As a data scientist, your first step is to visualize the task given.

First, you can draw a graph.

![](blogpost_files/figure-markdown_github-ascii_identifiers/2016%20graph-1.png)

Each 2016 student is a data point. We can plot the 100 student data on a graph.

**Green triangles** are the liars. **Red dots** are the honest students.

Now if you have a prospective student with `tuition_need= 8`and `unmet_need= 6`, based on the graph we just plotted, how far away is the new data point from the truth and lies?

The prospective student is shown as a **blue square**.

![](blogpost_files/figure-markdown_github-ascii_identifiers/2016+2018%20data%20plotted-1.png)


:shipit: What is your prediction?

You might say, "based on the graph, the point is very close to a group of liars, so I predict that this student does not report his or her financial need honestly". The distance of this point to its closest neighbours will help us to make predictions. What we just did, using distance and neighbours to make a prediction, is actually k-Nearest Neighbours Algorithm!

In a 2-feature model, you can see the point being classified easily in the 2D graph. What if you have more features that make the model 3D, 4D or 1000D? You will need your laptop to do the sorting for you.

What does the letter 'k' in k-Nearest Neighbours Algorithm mean? 'k' is the number of neighbours you specify to make a prediction. For example, if you have 100 data points on the graph, you do not have to calculate the distance between the point of interest and the 99 other points. You just need some points close to it; hence, the name "nearest neighbours".

Let's try...

![](blogpost_files/figure-markdown_github-ascii_identifiers/kNN%20in%20action-1.png)


The neighbours near the point of interest will vote for a prediction. If you decide to look at the 3-nearest neighbours to the point of interest, you might get a prediction based on 8 possible voting patterns:

|            | 1                     | 2                   | 3                   | 4                   | 5                 | 6                 | 7                 | 8               |
|------------|-----------------------|---------------------|---------------------|---------------------|-------------------|-------------------|-------------------|-----------------|
| scenarios  | [truth, truth, truth] | [truth, truth, lie] | [truth, lie, truth] | [lie, truth, truth] | [truth, lie, lie] | [lie, truth, lie] | [lie, lie, truth] | [lie, lie, lie] |
| prediction | truth                 | truth               | truth               | truth               | lie               | lie               | lie               | lie             |

Democracy does not always work. You should pick an odd number. If `k=2` and you get one vote for truth and one vote for a lie, how are you going to make a prediction? If you do need to pick an even-number `k`, you should have a tie-breaker rule!

Back to our example, this student reports `tuition_need= 8`and `unmet_need= 6`. The 3 closest data points are \[lie, lie, lie\]. We can make a prediction that the self-reported numbers may be inaccurate. Machine learning still needs common sense and our prediction is not absolute. We should bring this prediction to the finance team for their expert input and further investigation.

In summary, k-Nearest Neighbours Algorithm is a very handy tool to classify data points and learn their patterns. Its result is also easy to interpret and this algorithm is widely applicable.

If you are interested in knowing more about k-nearest neighbours algorithm, please see the list of references below. :eyeglasses:

References

1. What are industry applications of the K-nearest neighbor algorithm? [Internet]. Quora. 2017 [cited 16 September 2017]. Available from: https://www.quora.com/What-are-industry-applications-of-the-K-nearest-neighbor-algorithm

2. Classification w/ K Nearest Neighbors Intro - Practical Machine Learning Tutorial with Python p.13 [Internet]. YouTube. 2017 [cited 16 September 2017]. Available from: https://www.youtube.com/watch?v=44jq6ano5n0

Image Courtesy

1. The Mummy: Tom Cruise linked with lead in new film [Internet]. Den of Geek. 2017 [cited 16 September 2017]. Available from: http://www.denofgeek.com/movies/the-mummy/37980/the-mummy-tom-cruise-linked-with-lead-in-new-film
