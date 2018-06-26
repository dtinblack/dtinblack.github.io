---
layout: post
title: Counting on A&E
description: "Application of Little's Law to complexity of queuing in A&E. "
modified: 2018-03-26
tags: [A&E, Little's Law, Emergency Department]
image:
  feature: features/mathematics-of-A&E.jpg
  credit: The Telegraph
  creditlink: https://www.telegraph.co.uk/news/health/news/9871612/AandE-departments-so-short-staffed-four-in-10-doctors-are-locums-warns-report.html
  background: backgrounds/general-background.jpg
mathjax: true
---

The closest I have got to experiencing the demands on Accident and Emergency (A&E) of a hospital is watching the TV series <a href="https://en.wikipedia.org/wiki/M*A*S*H_(TV_series))">MASH</a>, but recently I was right in the middle of it!

Waiting for attention I was interested in the way that the staff were managing the wide range of medical problems that were rolling through the door. There were:
people holding limbs in great pain, a head covered in sticking plasters, two to three people bright red and coughing, a queue of wheel chairs with a legs in plaster, and somebody hobbling around in too much pain to sit down. In the background Ambulances were rushing in and trollies were rattling along corridors.
All of this activity is, in a management sense, ‘unplanned’ e.g. people could arrive at A&E anytime of the day or night with a wide range of problems.  I started to wonder how a typical A&E is organised and operates to manage the situation and to meet the [4 hour waiting target](https://en.wikipedia.org/wiki/Four-hour_target_in_emergency_departments).

A few days later I was waiting in another queue this time in my local coffee shop. As I slowly moved along I did a quick sum<sup>1</sup> to work out how long I would have to wait and came up with the following calculation:

<center>(4 customers) x (1 min/customer) = 4 minutes.</center>

If the queue had been longer then I would have waited longer. Or if there had been more staff serving then the quicker the service and the shorter the waiting time. To apply the same approach to A&E I took some statistics from the
<a href="https://www.england.nhs.uk/statistics/statistical-work-areas/ae-waiting-times-and-activity/statistical-work-areasae-waiting-times-and-activityae-attendances-and-emergency-admissions-2015-16-monthly-3/" >data published monthly</a> on A&E performance where the average number of people attending A&E per hour is approximately 12 / hour
( on average there are 8,500 people attending A&E for each hospital in NHS England per month ). I also assumed that a typical A&E department can manage 10 cases per hour then the using the same approach as a the coffee shop I calculated:

<center> (12 A&E attendees )  x ( 6 minutes per attendees  ) = 72 minutes or approximately 1 hour</center>

which was close to my experience in A&E. The calculation confirms what we would expect: if the A&E department's capacity was increased by adding more doctors and nurses then the waiting time would reduce. Similarly if the number of people attending A&E was reduced then the waiting time reduces.

Of course the calculation is too simplistic to be applied to the complex operation of an A&E Department because it assumes <i>average</i> quantities. But
trying to answer the question: Why can it not be applied ? - highlights some of the underlying factors that are adding to the complexity of its operation.

Starting with the average arrival rate of A&E attendees,
<a href="http://researchbriefings.files.parliament.uk/documents/SN06964/SN06964.pdf" >A&E statistics</a> show that there is a wide variability during a typical week. For example Monday is the busiest day at A&E with attendance 13% above the daily average and also 13% above the next - busiest day, Sunday. Also, in 2013/14, 24% of A&E attendances arrived by ambulance or helicopter who require immediate attention. All of this starts to show the variability in the arrival rate of people requiring medical attention.

Similarly the wide range of patient's medical problems will affect an A&E department's capacity
to manage their diagnosis and subsequent treatment. For example if there was a major emergency situation, say a train crash or a flu epidemic, then the capacity of A&E would be overloaded. Another area is diagnosing the medical condition. For example 3% of patients attending A&E have severe life threatening conditions and must be seen immediately. Also, if about 40% of attendees are not seen within an an hour of arrival at A&E their condition could deteriorate to life threatening.

There are many more factors affecting the performance of A&E for example the well publicised [bed blocking](https://www.independent.co.uk/news/uk/politics/nhs-bed-blocking-delayed-transfer-care-theresa-may-funding-social-care-crisis-election-a7783936.html) and transfer to social care which can increase the time seen by the doctors and nurses. Other factors are not so obvious for example the impact of [weather](http://www.qualitywatch.org.uk/news/ae-departments-are-experiencing-perfect-storm-factors-leading-increase-waiting-times) - when average daily temperatures hit 20°C compared with 5°C, trips to A&E rise by nearly 20%. However, very cold weather does also cause longer waits.

Although the assumption of using average quantities to describe the operation of A&E is over simplistic,  asking the question "why do the assumptions break down ?" can gives a better understanding of the underlying factors that contribute to its performance. Based on my experience, the way that the staff manage the range of the medical problems that come through the doors of A&E is much more impressive than the TV characters  [Hawkeye](https://en.wikipedia.org/wiki/List_of_M*A*S*H_characters#Hawkeye_Pierce) and [Trapper John](https://en.wikipedia.org/wiki/List_of_M*A*S*H_characters#Trapper_John_McIntyre)!

<p><i>1. More formally the calculation is an example of
<a href="https://en.wikipedia.org/wiki/Little%27s_law">Little's Law</a> which states that the long-term average number of customers in a stable system L is equal to the long-term average effective arrival rate, λ, multiplied by the average time a customer spends in the system, W. For a different and more detailed discussion on the application of Little's Law to staffing levels in A&E see:
<a href="http://epmonthly.com/article/littles-law-the-science-behind-proper-staffing/">Little’s Law: The Science Behind Proper Staffing</a>
</i></p>
