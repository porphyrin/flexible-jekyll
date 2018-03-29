---
layout: post
title: No-Show Analysis
date: 2018-03-24
description: What Metrics Correlate with Missing Medical Appointments?
img: medical_appt.jpg
tags: [Descriptive Analytics]
---
On average, a single medical appointment no-show costs the healthcare system 60 minutes of physician time, which
translates to a $200 worth of sunk cost.<sup>[1](#footnote1)</sup> Moreover, there is associated risk for the patient:
patients who miss appointments, and choose not to or are unable to reschedule them, miss preventative and diagnostic
care which may exacerbate health issues down the line.

To explore the issue of medical no-show appointments, we will explore a set of data from the summer of 2016 for a set
of hospitals in Espirito Santo State, Vitoria, Brazil.

## 1 Exploring the Data
Let's start by exploring the temporality of the data that we have available to us. From a quick look at our data, we can
see that we have 7 weeks worth of data, spanning the week of April 25, 2016 to June 6, 2016. To get a sense for what
the scheduled appointment volume looked like during these weeks, let's visualize the volume in a heatmap.

![alt text](https://github.com/porphyrin/porphyrin.github.io/blob/master/assets/img/volume_heatmap.jpg)

Testing testing.

<a name="footnote1">1</a>: SCI Solutions, 2017 - https://www.healthmgttech.com/wp-content/uploads/2017/04/h1705-IndustryWatch-SCI-Infographic.pdf