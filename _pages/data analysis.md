---
permalink: /portfolio/data-analysis/
title: " "
wide: true
toc: true
toc_sticky: true
author_profile: false

gallery:
  - url: /assets/images/numerical%20correlation.png
    image_path: /assets/images/numerical%20correlation.png
    alt: "numerical correlation"
    title: "Numerical Correlation"
  - url: /assets/images/categorical%20correlation.png
    image_path: /assets/images/categorical%20correlation.png
    alt: "categorical correlation"
    title: "Categorical Correlation"
gallery2:
  - url: /assets/images/numerical-correlation-full.png
    image_path: /assets/images/numerical-correlation-full.png
    alt: "numerical correlation full"
    title: "Numerical Correlation Full"
  - url: /assets/images/categorical-correlation-full.png
    image_path: /assets/images/categorical-correlation-full.png
    alt: "categorical correlation full"
    title: "Categorical Correlation Full"
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

# Computing Churn Rate
Starting off, the first thing to do is calculate the overall user churn rate of the company. This is achieved by dividing the total churn user with total user (`churn user / total user`). 
From the data we gather:
   - Total User: 5630
   - Churn User: 948
   - Retained User: 4682
   - Churn Rate: 16.84%
   - Retain Rate: 83.16%

> “ . . . there is a global opinion for an ideal churn rate to be 5%.”

Knowing this beforehand gives context to how high/low the company’s current churn rate is.

# Analysing User Churn-Tenure Relation
---
Since user churn is basically user retention (they are directly inversely proportional); a problem with user churn is the same as a problem with user retention. 

Retention itself is about ‘time frame of a user staying/keep returning’; the tenure of users. This means, user churn is directly related with user tenure. Having this in mind, analysing churn and tenure together will give us insight of how our user behave in the retention funnel. 

![Churn-Tenure Chart]({{ site.url }}{{ site.baseurl }}/assets/images/churn-tenure.png){: .align-center}

Alternatively, the data can also be plotted to represent user retention; if total user in the timeframe is assumed as the initial user count.

![Retention Chart]({{ site.url }}{{ site.baseurl }}/assets/images/retention.png){: .align-center}

From the chart above, it is clear that **a lot** of churn users are on their 0-2 day on the platform; this is a recurring problem with digital platforms. 

Since the breakpoint for the churn rate is on 0-2 day, there are 2 possibilities where the problem is at: (1) sales funnel – completing purchase; (2) retention funnel – loyal user conversion. A brief skim through the data shows that all users have a minimum of `1` purchase complete; there are no problem with user’s first-purchase; it is a retention funnel problem.


# Finding User Characteristics
---
With the information attained from analysing Churn-Tenure data, the users can be split into 2 segments: (1) Churn Users – users that are churn and on their 0-2 day; (2) Retained Users – users that stays for longer. Going forward **‘Segment’** will refer to this segmentation and used as a base to analyse user characteristics.

## **Correlation**
To help with determining which feature to analyse, using correlation heatmap could help in checking each feature's correlation with target. ince the data's features are a mix of numerical and categorical value, there is a need to separate both types to their own dataframe and calculate their correlation separately. Uing Pearson’s Correlation for numerical data; Chi-Squared method for categorical data.

**Note:**
Correlation is by no means equal or the same as causation. This [article](https://www.abs.gov.au/websitedbs/D3310114.nsf/home/statistical+language+-+correlation+and+causation) explained more in-depth about correlatoin vs. causation.
{: .notice--warning}

{% include gallery caption="*The correlation results thats closer to 0 means weaker to no correlation; number that goes bigger (negative value or not) means a stronger correlation.*" %}

{% include gallery id="gallery2" caption="*Full correlation chart for reference." %}

From the correlation calculation there are few notable features, solely based on correlation score:

1. Preferred Order Category (0.33)
2. Cashback Amount (0.24)
3. Complain (0.22)
4. Marital Status (0.20)
5. Preferred Login Device (0.19)

However, choosing features solely based on correlation is not advisable. For example feature like `Marital Status` is something that's innate to customer and there is no action that could be taken. On the contrary, even though correlation scores are low; features like `Satisfaction Score` or `Hours Spend on App` are interesting characteristics of users that are related to how the user perceive the platform.

**Note:**
Correlation is by no means equal or the same as causation. This [article](https://www.abs.gov.au/websitedbs/D3310114.nsf/home/statistical+language+-+correlation+and+causation) explained more in-depth about correlatoin vs. causation.
{: .notice--warning}

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
