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

The closest I have got to the chaos of a hospital in the middle of a battle is watching the TV series <a href="https://en.wikipedia.org/wiki/M*A*S*H_(TV_series))">MASH</a>, but sitting in my local A&E I was starting to feel what it would be like!

Sitting in Accident and Emergency ( A&E )<sup>1</sup> waiting for attention I watched
how the staff were managing the wide range of medical problems - I was impressed! There were:
people holding limbs in great pain, a head covered in sticking plasters, two to three people bright red and coughing, a queue of wheel chairs with a legs in plaster, and somebody hobbling around in too much pain to sit down. In the background Ambulances were rushing in and trollies were rattling along corridors.
All of this activity is, in a management sense, ‘unplanned’ e.g. people could arrive at A&E anytime of the day or night with a wide range of problems.  To distract me from my pain I started to wonder how a typical A&E is organised and operates to manage the situation and to meet the [4 hour waiting target](https://en.wikipedia.org/wiki/Four-hour_target_in_emergency_departments).


A few days later I started to search for a framework to guide my analysis of an A&E Department when I came across <a href="https://en.wikipedia.org/wiki/Little%27s_law">Little's Law</a>
which describes the relationship between the <i>average</i> length of a queue, the <i>average</i> waiting time and the <i>average</i> arrival of, in the case of A&E, sick or injured people.  More formally, Little's Law can be expressed algebraically by: $$L=\lambda$$$$W$$ where $$L$$ represents the <i>average</i> number of customers waiting to be seen by the medical staff in A&E, is equal to
<i>average</i> arrival rate of sick or injured people, $$λ$$, multiplied by the <i>average</i> time that they are seen by the doctors and nurses, $$W$$.  This law represents
what we would experience when standing in a queue - if a lot of people are in a queue ($$L$$ is large)  because there are long delays in the doctors seeing people ($$W$$ is large); if few people arrive at A&E  queue ($$λ$$ is small) then the average number of people waiting to bee seen by the doctors and nurses is small ($$L$$ is small). The law has many applications ranging from
<a href="http://web.mit.edu/sgraves/www/papers/Little's%20Law-Published.pdf">storing wine</a>,
housing market, toll booths to designing the underlying technology of the Internet.

To add life to the mathematical formula I started to play with some numbers and
using some
<a href="https://www.england.nhs.uk/statistics/statistical-work-areas/ae-waiting-times-and-activity/statistical-work-areasae-waiting-times-and-activityae-attendances-and-emergency-admissions-2015-16-monthly-3/" >data published monthly</a> on A&E performance I computed the following:


1. Average number of people attending A&E per hour ( $$λ$$ ) is approximately 12 / hour
( on average there are 8,500 people attending A&E for each hospital in NHS England per month ).
2. Assume that a typical A&E department can manage a maximum of 15 cases per hour ( $$L$$ ).

Rearranging Little’s Law to give the average waiting time $$W = L / λ$$  gives approximately 1.5 hours.
The formula confirms what we would expect: if the A&E department's capacity was increased by adding more doctors and nurses ( $$W$$ ) then the waiting time would reduce. Similarly if the average number of people attending A&E ( $$λ$$ ) reduces then the waiting time reduces.

Of course Little’s Theorem is too simplistic to be applied to the operation of an A&E Department because it assumes <i>average</i> quantities. But
trying to answer the question: Why can it not be applied ? - the answers produce some of the underlying factors that are adding to the complexity of its operation.

Starting with the average arrival rate ( $$λ$$ ),
<a href="http://researchbriefings.files.parliament.uk/documents/SN06964/SN06964.pdf" >A&E statistics</a> show that there is a wide variability druing a typical week. For example Monday is the busiest day at A&E with attendance 13% above the daily average and also 13% above the next - busiest day, Sunday. 11am
on Monday is the single busiest hour. 9.5% of attendances are between the hours of midnight and
7am, while 58% occur between 9am and 6pm. Also, in 2013/14, 24% of A&E attendances arrived by
ambulance or helicopter who require immediate attention. All of this starts to show
the variability in the arrival rate of people requiring medical attention.

Similarly the wide range of patient's medical problems will affect an A&E department's capacity
to manage their diagnosis and subsequent treatment. For example if there was a major emergency situation, for example a train crash or an explosion, then the capacity ( $$W$$ ) of the A&E Department would be overloaded. Another area is diagnosing the medical condition. For example 3% of patients attending A&E have severe life threatening conditions. Also, if about 40% of attendees are not seen within an an hour of arrival at A&E their
condition could deteriorate to life threatening. Also, diagnosing a problem quickly and accurately can be
difficult for many reasons. In my case the A&E staff had to translate my own diagnosis of “I have a pain in my stomach and I can’t pee !” into medical terminology of “acute urinary retention” and the appropriate action taken before my condition deteriorated into more severe problems.

There are many more factors affecting the performance of A&E for example the well publicised [bed blocking](https://www.independent.co.uk/news/uk/politics/nhs-bed-blocking-delayed-transfer-care-theresa-may-funding-social-care-crisis-election-a7783936.html) and transfer to social care which can increase the capacity ( $$W$$ ). Other factors are not so obvious for example the impact of [weather](http://www.qualitywatch.org.uk/news/ae-departments-are-experiencing-perfect-storm-factors-leading-increase-waiting-times) - when average daily temperatures hit 20°C compared with 5°C, trips to A&E rise by nearly 20%. However, very cold weather does also cause longer waits.

Although the assumptions of describing the operation of A&E using average quantities is over simplistic asking the question "why do the assumptions break down ?" can give a clearer picture of underlying factors that contribute to its complexity and affect its operation. As for my experience the way that the staff manage the complexity to ensure that people are seen on time is even more impressive compared to  [Hawkeye](https://en.wikipedia.org/wiki/List_of_M*A*S*H_characters#Hawkeye_Pierce) and [Trapper John](https://en.wikipedia.org/wiki/List_of_M*A*S*H_characters#Trapper_John_McIntyre)!

<p><i>1. Although A&E Departments were renamed to
<a href="http://www.theguardian.com/politics/2003/jan/12/health.nhs">Emergency Departments</a>
in 2004 it is interesting to note that the public have still use term 'A&E' - is it because it is easier to
pronounce than ED ?</i></p>

<p><i>
For a different and more detailed discussion on the application of Little's Theorem to staffing levels in A&E see:
<a href="http://epmonthly.com/article/littles-law-the-science-behind-proper-staffing/">Little’s Law: The Science Behind Proper Staffing</a>
</i></p>
