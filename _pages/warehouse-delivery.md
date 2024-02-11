---
permalink: /portfolio/warehouse-delivery/
title: " "
wide: true
toc: true
toc_sticky: true
---
<head>
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XTY9FB7TVT"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-XTY9FB7TVT');
</script>
</head>

# Warehouse Outbound Analysis
---
In supply chain, having a smooth transition between steps is crucial; each steps' performance will also affect the overall supply chain performance. This is especially true for the transition into last-mile delivery. As the name suggests, last-mile delivery is the the last step (outside of return shipment) to fulfillment; it is the closest to customer and is the deciding factor of how customer perceive the fulfillment quality.

**Note:**
Data has been adjusted for the sake of aninomity.
{: .notice--warning}

On this case, a delivery company (A) is acting as a 3rd-party logistic for an ecommerce platform. Company A's responsibility is to process all the outgoing items from one of the ecommerce's warehouse; from when items checkouts from the warehouse to delivering it to customer's doorsteps. However, company A's team that are in charged of transitioning items that checkouts from the warehouse and prepare them for delivery, are overwhelmed in the first day; the team was falling behind and as a result items are shipped late waiting for the prep-team to finish their work. Clearly, there is something wrong with how the team is handling their work; and company A is trying to figure out what the problem(s) is(are) and how to solve them.

This analysis is done on behalf of company A, trying to figure out what is the key problem that is holding the prep-team back, and what are the possible solutions to fix the problem and kick-start the prep-team's performance; to not hold back the entire supply chain.

**Note:**
This analysis are done only with spreadsheet.
{: .notice--primary}

# Initial Setup 
---
The ongoing operational setups are:
1. Warehouse starts operation at 12:00
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
1. when items goes out of the warehouse - this will help determine the actual timing pattern for outgoing item, when the items are handed over.
2. when items are ready to ship - this will show how much time needed for items to be processed, shows if manpower is lacking or not.


# Warehouse Outbound Timings
---
There are 10 days of data that are gathered to be used as a sample; there are only several days of data because the project was initiated recently. From all the 10 days of data compiled into a heatmap of shipments separated by the hour the items are; (1) Signed out by warehouse; (2) Marked as ready for shipment by prep-team.

**Note:**
For anonymity the figures below have been adjusted.
{: .notice--primary}

![map]({{ site.url }}{{ site.baseurl }}/assets/images/warehouse/warehouse-handover.png){: .align-center}

![map]({{ site.url }}{{ site.baseurl }}/assets/images/warehouse/ready-delivery.png){: .align-center}

From the charts above, there are some major take points that are important:
1. First item to sign out of warehouse is 2hrs after warehouse starts operation.
2. Prep-team needs 2hrs to after the first item signed out of warehouse to finish preparing and processing items.
3. There are only 35% of total items that sign out before break time (18:00) the rest of the items came out after break time. In less time, (5hrs) 2nd shift prep-team needs to process 2 times more volume compared to 1st shift prep-team (6hrs). 
4. After break, 19:00 - 21:00, is where most of the items are signed out; around 50% of the daily volume is allocated in this 3 hours.
5. After day 3, prep-team starts to finish work later and later; field staff said that they are exhausted from overworking the earlier nights.
6. At worst, prep-team finished their work the next morning at 09:00 AM, and delays delivery by 2 hours, because delivery starts at 07:00 AM.


# Manpower Problem
Analysing the timings of items signing out of warehouse and the timing of items being process and prepped, shows that theres clearly a lack of manpower; or to be more precise there is manpower allocation problems:
1. Even though shift 2 volume is double the volume of shift 1, but the amount of manpower available for the prep-team is the same for either shift. 
2. Shift 1 team starts their shift at 10:00, when the first item that will sign out of the warehouse is actually in 4 hours at 14:00. This is alot of manpower wasted.
Overall, the allocation of manpower is totally off timing compared to the timings of items signing out of warehouse.

# Solution
The clear solution here is to move allocate manpower properly, instead of dividing both shifts as equal number of people, shift 1 should have half the amount of people compare to shift 2; just as what the items volume. So from the 8 manpower, shift 1 should only have 3 people, and shift 2 should have 5 people.

Schedules for the shifts is also detrimental. Since the first items to sign out of the warehouse are usually around 14:00, shift 1 should at least start working around 13:00 and shift 2 should start their shift 19:00. If counting each shift to last 8hrs of work; shift 1 would be 13:00 - 21:00; shift 2 would be 19:00 - 01:00. The shifts being scheduled like this would allow both shifts to be working on the most busy hours; when most of the items would sign out of the warehouse (19:00 - 21-00).

# Results
Solutions above have been implemented and the results shows that the prep-team is no longer overwhelmed and no longer performing poorly. It also spare the prep-team from exhaustion. Finishing on time also makes sure that the delivery the next morning won't be delayed, because all items are in ready to ship condition.
