---
permalink: /portfolio/warehouse-delivery/
title: " "
wide: true
toc: true
toc_sticky: true
author_profile: false
---
# Delivery Manpower Analysis 
---
For companies that offer delivery or courier services, knowing the areas where they do their delivery is essential. Determining which areas are dense with customers and which aren't, and which areas that give more opportunity and growth, will help the company reduce cost and improve revenue.

**Note:**
For anonymity and to keep classified information undisclosed, the companies name are gonna be replaced and the data/analysis results will be censored.
{: .notice--warning}

On this case, a delivery company (A) is acting as a 4th-party logistic for another company (B). Both companies are operating on the same general area but have split delivery area for a long time; company A handles more area than company B. However, company B wants to increase their own operation size, thus company B proposes to take over specific areas from company A. Even though it is a 'proposal', company A as a 4th-party have no option but to accept; however is trying to counter propose which area to be handed over.

This analysis is done on behalf of company A, trying to find the best delivery area split for them; considering the delivery volume they get from company B and their own delivery volume on the specific area.

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
