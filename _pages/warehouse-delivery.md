---
permalink: /portfolio/warehouse-delivery/
title: " "
wide: true
toc: true
toc_sticky: true
---
# Warehouse Delivery Analysis
---
In supply chain, having a smooth transition between steps is crucial; each steps' performance will also affect the overall supply chain performance. This is especially true for the transition into last-mile delivery. As the name suggests, last-mile delivery is the the last step (outside of return shipment) to fulfillment; it is the closest to customer and is the deciding factor of how customer perceive the fulfillment quality.

**Note:**
For anonymity and to keep classified information undisclosed, the companies name are gonna be replaced and the data/analysis results will be censored.
{: .notice--warning}

On this case, a delivery company (A) is acting as a 3rd-party logistic for an ecommerce platform. They got responsibility to process all the outgoing items from one of the ecommerce's warehouse; from when items checkouts from the warehouse to delivering it to customer's doorsteps. However, company A's team that are in charged of transitioning items that checkouts from the warehouse and prepare them for delivery, are overwhelmed in the first day; the team was falling behind and as a result items are shipped late waiting for the prep-team to finish their work. Clearly, there is something wrong with how the team is handling their work; and company A is trying to figure out what the problem(s) is(are) and how to solve them.

This analysis is done on behalf of company A, trying to figure out what is the key problem that is holding the prep-team back, and what are the possible solutions to fix the problem and kick-start the prep-team's performance; to not hold back the entire supply chain.

**Note:**
This analysis are done only with spreadsheet.
{: .notice--primary}

# Analysing Delivery Volume
---
The most important thing in deciding which area to be kept or handed over, it is important to know the historical delivery volume and potential volume the specific area have. Other than sheer volume, there are other important parameters that needs to be considered. In this analysis, the parameters that are used to decide on the delivery area are:
1. Volume - sheer delivery and pickup volume
2. Volume density - delivery volume per km-square
4. Delivery distance - km per delivery point in average
5. Pickup distance - km per pickup point in average
6. Delivery per stop - average volume of delivery per delivery point
7. Pickup per stop - average volume of pickup per pickup point

These parameters are observed per postal code acting as the area segregator.
![volumeanalysis]({{ site.url }}{{ site.baseurl }}/assets/images/fedex/teaser1.png){: .align-center}

On this case, it is actually not to try to keep the area with the densest volume from company B, because those areas are the most disputed and company B wanted the most. In fact it is to try to find areas where company A have a lot of their own volume, outside of company B's volume, but then still have respectable volume from company B. This way that specific area, for company A, will have a combined volume and density of their own volume and company B's volume. 

# Determining Area
---
From compiling and calculating each parameters into consideration, the area to be kept and handed over are set accordingly. On this project, several scenarios of proposal are given, this is to give options and make negotiation smoother.

![proposalareas]({{ site.url }}{{ site.baseurl }}/assets/images/fedex/teaser2.png){: .align-center}

The resulting proposal are in a form of which postal code are to be kept by company A, and which postal code are to be handed over to company B.

# Determining Area
---
To help management and business team visualize the area and get a better understanding of the are in question, the volume and areas are mapped with google mymaps.
![map]({{ site.url }}{{ site.baseurl }}/assets/images/fedex/map.png){: .align-center}

**Note:**
For anonymity and to keep classified information undisclosed, the area split and volume are not shown, the map is just a dummy.
{: .notice--warning}

The map above represents the overall disputed area, which each polygon represents the area the postal code represents. Pins shows where delivery and pickup points are, and are color coded to show the volume range of each point.
