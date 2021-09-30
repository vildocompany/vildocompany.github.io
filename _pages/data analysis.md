---
permalink: /portfolio/data-analysis/
title: " "
wide: true
toc: true
toc_sticky: true
author_profile: false
---
# Data Analysis
---
Objective of data analysis is to extract insights from data; then assist in decision-making. 

This can be achieved by analysing data and asking the right question; gaining insights and answers from data.  Everything is then reported and presented with solution recommendation related to the problem at hand.

# Case Study - Ecommerce Customer Churn Analysis
---
So, what is churn?
Churn is defined as ‘number of users that has stopped using a service; in this case the service is ecommerce platform. 

The company behind the ecommerce platform wants to know their user churn condition. They wanted to know when and where people would drop their platform; if there are any clear differences in user characteristics between those who are classified as churn and aren’t.

**Info:**
Case is part of a study and 'company' mentioned is fictional; data used is a public data that can be accessed through: [dataset](https://www.kaggle.com/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction).
{: .notice--info}

**Note:**
This analysis is the first part of a 2-part project: second part [here].
{: .notice--warning}

## Computing Churn Rate
Starting off, the first thing to do is calculate the overall user churn rate of the company. This is achieved by dividing the total churn user with total user (`churn user / total user`). 
From the data we gather:
   - Total User: 5630
   - Churn User: 948
   - Retained User: 4682
   - Churn Rate: 16.84%
   - Retain Rate: 83.16%

> “ . . . there is a global opinion for an ideal churn rate to be 5%.”

Knowing this beforehand gives context to how high/low the company’s current churn rate is.

## Analysing User Churn-Tenure Relation
Since user churn is basically user retention (they are directly inversely proportional); a problem with user churn is the same as a problem with user retention. 

Retention itself is about ‘time frame of a user staying/keep returning’; the tenure of users. This means, user churn is directly related with user tenure. Having this in mind, analysing churn and tenure together will give us insight of how our user behave in the retention funnel. 

![Churn-Tenure Chart]({{ site.url }}{{ site.baseurl }}/assets/images/tenure.png){: .align-center}

Alternatively, the data can also be plotted to represent user retention; if total user in the timeframe is assumed as the initial user count.

[chart]

From the chart above, it is clear that **a lot** of churn users are on their 0-2 day on the platform; this is a recurring problem with digital platforms. 

Since the breakpoint for the churn rate is on 0-2 day, there are 2 possibilities where the problem is at: (1) sales funnel – completing purchase; (2) retention funnel – loyal user conversion. A brief skim through the data shows that all users have a minimum of `1` purchase complete; there are no problem with user’s first-purchase; it is a retention funnel problem.


## Finding User Characteristics
With the information we get from analysing Churn-Tenure data, we can split the users into 2 segments: (1) Churn Users – users that are churn and on their 0-2 day; (2) Retained Users – users that stays for longer.

Using the segments, it is possible to then determine the difference in characteristics of the 2 user segments (Churn User and Retained Users).



### Blockquotes

> Lorem ipsum dolor sit amet, test link adipiscing elit. Nullam dignissim convallis est. Quisque aliquam.

## List Types

### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3
{: rules="groups"}

## Code Snippets

```css
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
```

## Buttons

Make any link standout more when applying the `.btn` class.

```html
<a href="#" class="btn btn--success">Success Button</a>
```

<div markdown="0"><a href="#" class="btn">Primary Button</a></div>
<div markdown="0"><a href="#" class="btn btn--success">Success Button</a></div>
<div markdown="0"><a href="#" class="btn btn--warning">Warning Button</a></div>
<div markdown="0"><a href="#" class="btn btn--danger">Danger Button</a></div>
<div markdown="0"><a href="#" class="btn btn--info">Info Button</a></div>

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}
