---
title: FirstCall | Emergency Response Revolutionized
author: Stanley Lee
date: 2021-05-06T00:00:00.000Z
excerpt: >-
  With the growing community interest in Gatsby, we hope to create more
  resources that make it easier for anyone to grasp the power of this incredible
  tool.
hero: ./images/hero.png
---
<iframe width="560" height="315" src="https://www.youtube.com/embed/a_fWpdRpUqk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Background

In the past year over 240 million 911 calls occurred in the United States alone. With an average response time of 10 minutes, callers around the country are waiting while vital information can be transferred regarding an emergency. However, due to archaic infrastructure and a lack of consistent maintenance of first responder technology, it has fallen behind many modern apps today like Uber or Lyft.

#### **Despite many having phones that have advanced technology such as real time GPS, messaging, and LiDAR, 911 responders are unable to obtain any of this information.**

## Planning Process

We had a full week to work on FirstCall, so we wanted to operate similar to a professional tech company in order to create the highest quality project possible. Our team conducted daily stand-up meetings and did extensive planning. Our planning efforts can be seen in this [linked design doc](https://docs.google.com/document/d/18WF4zKyjAWL22-rYXKdr3AHuponK26pcgtRyF5EvT0o/edit).

![Gantt Chart](images/GZUBg6W.png "Gantt Chart for a Week-long Hackathon")

# Primary and Secondary Research

#### Secondary Research

Our research showed that there are needs from the caller side as well. A 2018 study conducted by researchers from Simon Fraser University found that people want features such as video calling but also believe "video calling should be as easy as calling 9-1-1 with a smartphone or a landline". Another research paper also talked about how the information 911 callers provide can impact, sometimes negatively, the actual response of paramedics and police officers. Thus, we aimed to create a simple to use system that allowed users to provide 911 dispatchers with clear, concise, and accurate information.

#### Primary Research

To add onto our prior research, we decided to conduct our own research at the beginning of hackathon. We created a survey of relevant research questions which we then distributed widely across our network. Our survey yielded a total of 28 responses across a diverse range of past 911 callers.

![User Surveys](images/P7XCkxF.png "User Surveys")

### Insights

* The vast majority of people use mobile smartphones to call 911. Callers would primarily benefit from GPS location and photographs.
* Most phones have internet capability and cameras but do not have heart rate or fingerprint scanners.
* Users requested being able to give 911 allergy and blood information in case EMT uses medication.

![User Personas](images/odl2vs0.jpg "User Personas")

# Visual Designs

We started with lo-fidelity prototypes to get rapid feedback from our developers before moving to solidified designs.

![](images/mJuajf6.png)

We then moved on the hi-fidelity prototypes that our developers could execute in a near 1:1 replica. 

![](images/3PJdSND.webp)

# Engineering Process

FirstCall is composed of two applications tied by a single server. Emergency responders use FirstCall Intelligence Terminal (FirstCall.it) and 911 callers use First Call Link yourself (FirstCall.ly).

FirstCall.it serves as a central hub for all first responders. It is primarily used by teams of dispatchers to help coordinate and organize all ongoing emergency calls. The application is a desktop web application with a secure login system, collaborative dispatching, and live UI updates.

FirstCall.ly is used by callers. It is a progressive web application (PWA) designed for mobile smartphones. The application utilizes unique identifiers (UUIDs) in order to securely generate custom websites per user.

A server ties the two applications together. This server is connected to a database on Firebase which is used to temporarily store information. Information needed only once is received from clients and sent from the server using API calls. Information that is repeatedly updated is received from clients and sent from the server using WebSockets to ensure instantaneous information flow. The server also utilizes Twilio and Google Cloud Machine Learning APIs in order to handle incoming phone calls.

![](images/GiOvLCk.webp)

# Takeaways and Learnings

We learned so much creating this project! This was our first ever week long hackathon (really any hackathon more than a weekend long) and it gave us a lot of extra time for planning and organization. We learned how to spread ourselves out over the course of the week, for the most part. This was also the first hackathon we ever did where we had Kanban boards, Gantt charts, Design Docs, and other product management tools. It was also the first where we conducted our own research studies and heavily dived into the Double Diamond Design process.

We want to first off improve the privacy and security of FirstCall. We already addressed it thoughtfully, but believe that a 911 response technology must have the most safe and secure system possible.Emergencies are also hard to imagine - there's so many kinds of them that it's hard to predict what's going to happen. We hope to expand FirstCall to tackle these emergencies that we didn't think of - by creating a more flexible system for first responders. We also hope to make the technology even more collaborative using our WebSocket technology, so we can create a tool akin to Figma or Google Docs to allow first response teams to work together efficiently.
