---
layout: post
title: Gambling On Prostate Cancer
description: "The consequences of a ‘false positive’ result."
modified: 2017-12-26
tags: [False Positive, PSA, Prostate, Medical Tests]
---

<p>
Medical terminology is full of complicated terms. Words
such as rhinorrhea ( runny nose), cerumen ( ear wax ) and epistaxis ( nosebleed ) map out
a land where only a few can tread. But recently I have had to step into it when I came across the term 'false positive'.
</p>

I have reached an age where health is starting to dominate my thoughts; in particular my prostate has been painfully brought to my attention. My doctor summarised the situation "your days of peeing over the school yard wall are over!" Therefore to diagnose the problem I have had various tests and examinations including the [Prostate Specific Antigen](https://prostatecanceruk.org/prostate-information/prostate-tests/psa-test) ( PSA ) test which is used to detect prostate cancer. When searching the web to find out more about the test I came across the phrase “false positive” which seems like a riddle posed by Yoda for ‘Young Skywalker’ in Star Wars. How can something be “false” and yet “positive” ?

Developing a [medical test](http://www.lymphomation.org/CTTutorial.pdf) is subject to many constraints. For example, the test should ideally be non-invasive, easy to use, and low cost. Also, because of the complexity of the human body and the limited level of knowledge about how it works the results from a medical tests are rarely 100% accurate. Accuracy is important. For example if a test is 90%
accurate then the results of 90 tests out of 100 will correctly show whether a person has the disease or not.  But for the remaining 10 tests the results will be wrong.

To work out what false positive means with respect to myself and the PSA test I grabbed my pen and paper and settled down to work out the following example. First, there is a lot of
<a href="http://www.cancerscreening.nhs.uk/prostate/prostate-patient-info-sheet.pdf" >
controversy about the [accuracy of the PSA test](http://www.medicaldaily.com/psa-test-deemed-too-inaccurate-unspecific-prostate-cancer-screening-guidelines-308018)
</a> therefore it is very difficult to get a definitive number on its accuracy. However, for the purposes of this example I assumed that it is 33% accurate ( or 1 in 3 ).
It is important to note that if the test result is positive it does not mean that there
is a probability of 33% of having prostate cancer. What is usually missed is the [baseline information](https://en.wikipedia.org/wiki/Base_rate_fallacy), which is the information about the situation before any testing is carried out. Therefore,
to work out the probability of actually having prostate cancer I needed an estimate of the number of men in a population who will have prostate cancer - the baseline information. For this example I have used an estimate of 1 in 33 as a guide to who will have prostate cancer ( the chances of prostate cancer increases with age ).  

The following steps work towards answering question: if the result of a PSA test is positive what
is the probability of having prostate cancer ? :

To keep the numbers simple I have kept the population size down to 100 therefore, the following diagram shows 3 in every 100 who will have prostate cancer - approximately 1 in 33 ( the baseline information ):

<figure>
<img src="/assets/images/false_positive_prostate_cancer_1.jpg" alt="" align="middle">
</figure>

<center><font size="2">Population showing 3 in 100 with prostate cancer</font></center>

 The following diagram shows the results from applying the PSA test with an accuracy of 1 in 3 ( 1 in three tests it gives a correct diagnoses ) where the plus signs are positive results:

<figure>
<img src="/assets/images/false_positive_prostate_cancer_2.jpg" alt="" align="middle">
</figure>

<center><font size="2">Population after the results of the PSA test</font></center>

From the digram it can be seen that the test gives the correct result for one case of prostate cancer and gets the other two cases wrong. The two wrong cases are called false negatives ( when designing a medical test the number of false negatives are minimised to reduce the chances of missing the disease ).  The test gives positive results for 64 cases when there is no prostate cancer - which are the false positives.  In other words the test returns a positive result when there is no disease. Therefore the probability that I could have prostate cancer is 1 in 65, and not 1 in 3 - the odds of not having prostate cancer when the test is positive have improved !

A large number of false positive results indicates that there is a low probability of having the disease. When a test has a low accuracy then more medical tests have to be performed. For example following a positive result from a PSA test then further tests will be required, for example an [ultrasounds scan](https://www.radiologyinfo.org/en/info.cfm?pg=us-prostate) or a biopsy before a diagnosis is reached.

The PSA test is quick and cheap, it can costs between £30 - £50 per test, but it can be unreliable, However, there are new medical tests being developed to improve the accuracy in detecting prostate cancer, for example: [Imaging techniques uising MRI]( http://www.bbc.co.uk/news/health-38665618), [improved blood test](http://www.dailymail.co.uk/health/article-4511066/New-blood-test-prostate-cancer-accurate-PSA.html#ixzz51DocwbDV) and
[urine test](http://www.dailymail.co.uk/health/article-2573395/The-10-prostate-test-New-cancer-check-twice-accurate-no-need-embarrassing-examination.html).

Next time I discuss further medical tests with my doctor to diagnose the problems with my prostate I will be asking about its false positive result. It may not put my mind to rest
but it will reduce the terminology fog and then I can concentrate on managing the situation !

<p><i>For more information about the PSA test see: <a href="https://www.nhs.uk/Livewell/Prostatehealth/Pages/psa-test.aspx">Should I have a PSA ?</a> and for
a detailed description of the mathematics behind the example discussed in this post see:
<a href="/assets/downloads/Mathematics-Of-A-False-Positive-Test.pdf">Mathematics of a False Positive Test.</a>
</i></p>
