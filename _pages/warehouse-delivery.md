---
permalink: /portfolio/warehouse-delivery/
title: " "
wide: true
toc: true
toc_sticky: true
---
# Warehouse Outbound Analysis
---
In supply chain, having a smooth transition between steps is crucial; each steps' performance will also affect the overall supply chain performance. This is especially true for the transition into last-mile delivery. As the name suggests, last-mile delivery is the the last step (outside of return shipment) to fulfillment; it is the closest to customer and is the deciding factor of how customer perceive the fulfillment quality.

**Note:**
For anonymity and to keep classified information undisclosed, the companies name are gonna be replaced and the data/analysis results will be censored.
{: .notice--warning}

On this case, a delivery company (A) is acting as a 3rd-party logistic for an ecommerce platform. Company A's responsibility is to process all the outgoing items from one of the ecommerce's warehouse; from when items checkouts from the warehouse to delivering it to customer's doorsteps. However, company A's team that are in charged of transitioning items that checkouts from the warehouse and prepare them for delivery, are overwhelmed in the first day; the team was falling behind and as a result items are shipped late waiting for the prep-team to finish their work. Clearly, there is something wrong with how the team is handling their work; and company A is trying to figure out what the problem(s) is(are) and how to solve them.

This analysis is done on behalf of company A, trying to figure out what is the key problem that is holding the prep-team back, and what are the possible solutions to fix the problem and kick-start the prep-team's performance; to not hold back the entire supply chain.

**Note:**
This analysis are done only with spreadsheet.
{: .notice--primary}

# Initial Setup 
---
The ongoing operational setups are:
1. Warehouse will start sending out items starting from 12:00
2. There will be an hour break on 18:00 - 19:00
3. Warehouse operation lasts until 24:00
4. Pre-team manpower is 8 people
5. Pre-team operational is in 2 shifts, from 11:00-18:00 and 18:00-finish (4 person each shift)

# Figuring Out The Problems
---
Since there is no specific problems to be solved, there is first a need to figure out what the problems are. One way is to go on site, asking around and observe the site; results were:
1. Schedule of outgoing items are inconsistent; lack of prior alert to how many items are outgoing from warehouse.
2. Lack of manpower; outgoing items from warehouse outnumber the manpower of the prep-team. 
3. Workflow on site is bad.


# Gathering Data
---
From the 3 suspected problems, it is possible to check problem 1 and 2 by analysing data. Since all items will have their shipment status updated on every process, there will be data on:
1. when the item goes out of the warehouse - this will help determine the actual timing pattern for outgoing item, when the items are handed over.
2. when the items are ready to ship - this will show how much time needed for items to be processed, shows if manpower is lacking or not.


# Warehouse Outbound Timings
---
There are 10 days of data that are gathered to be used as a sample; there are only several days of data because the project was initiated recently. From all the 10 days of data compiled into a heatmap of shipments separated by the hour the items are signed as 'out of the warehouse'.

**Note:**
For anonymity the figures below have been adjusted.
{: .notice--primary}

![map]({{ site.url }}{{ site.baseurl }}/assets/images/warehouse/warehouse-handover.png){: .align-center}

![map]({{ site.url }}{{ site.baseurl }}/assets/images/warehouse/ready-delivery.png){: .align-center}

From the charts above, there are some major take points that are importang:
1. Even though the warehouse starts operation at 12:00, the first item to sign out of warehouse are almost always at 14:00, 2hrs after warehouse starts operation. This means, the warehouse needs more or less 2hrs to start up their operation and finally send out items.
2. There are only 35% of total items that sign out before break time (18:00) the rest of the items come out after break time. In less time, (5hrs) 2nd shift prep-team needs to process 2 times more volume compared to 1st shift prep-team (6hrs). 
3. 
