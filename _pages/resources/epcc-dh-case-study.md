---
layout: single
classes: wide
title: Finding the right online tool for self-service HPC training
permalink: /resources/case-studies/epcc-dh-case-study
author_profile: false
sidebar:
  nav: "uhpc_menu"
---

As the need for HPC training grows, there is an increasing need for platforms that allow learners to progress asynchronously and independently through a course at their own pace. Not only can this autonomous learning reduce the pressure on HPC trainers, but the flexibility it offers can remove barriers to learning.  In this case study, Dr David Henty (EPCC, University of Edinburgh) shares his experience of testing multiple learning platforms (Blackboard Learn, FutureLearn, Github and CodeRefinery) to review their suitability for hosting open-source, online, self-service HPC courses. CodeRefinery was found to be a simple, easily configurable platform that best suited their needs and work is now ongoing to port a number of courses to this format.  This work was partially funded through the [EuroCC](https://www.eurocc-access.eu/) project, an EU project that aims to  build a European network of 33 national HPC competence centres to bridge the existing HPC skills gaps.

![epcc-logo-fullColour-rgb@1x](https://github.com/UNIVERSE-HPC/UNIVERSE-HPC.github.io/assets/106165178/e305af48-8b8f-49f7-8a56-5bf71ca65179)

Even before the pandemic we tested a range of different online teaching platforms as we were looking for new approaches to make our HPC material as open and accessible as possible to a wide range of learners and lecturers. Of course, since the move to more online working this has become increasingly important.  We were looking for a platform from which we could run an online version of our existing face-to-face "Hands-On Introduction to HPC" course, including a range of recorded lectures, articles and practical exercises. Most importantly we wanted other HPC centres to be able to run their own instances of the course, with exercises and other content tailored to their own users and local HPC systems. 

It is important to note that we were interested in self-service courses where learners study online material (e.g. articles or pre-recorded videos) in an asynchronous manner, perhaps with some support from other learners or designated tutors via chat boards. For synchronous online delivery, where a lecturer presents material live and learners can interact directly through chat, video or screen-sharing, platforms such as Zoom have proved very useful (at EPCC we use Blackboard Collaborate as it is fully supported through the University Of Edinburgh's Learn VLE, but it has similar functionality to Zoom).

### Blackboard Learn
Blackboard Learn is a Virtual Learning Environment widely used by Universities, including the University of Edinburgh where we use it for all accredited courses including our MSc in HPC Programmes. It integrates closely with the student record system which is ideal for an MSc programme, but this does restrict access to fee-paying students only.  It is not well suited to open source, community developed courses as although selected Blackboard Learn Courses can be made open to all, a facility we currently use for our free self-service ARCHER2 courses on parallel programming, this does not make the material easily available to other lecturers as they only have access to PDFs of lectures and exercises and not the source material. In addition, Blackboard Learn is itself a proprietary product so it would be difficult for another HPC centre to have their own instance of an entire course even if they had access to all the individual source materials. More importantly the ability to make courses open to non-matriculated students appears to be absent in the upcoming Learn Ultra upgrade so a replacement will soon have to be found. 

![FutureLearn_logo](https://github.com/UNIVERSE-HPC/UNIVERSE-HPC.github.io/assets/106165178/31b59bb1-fa73-48d8-90a2-a3e47538decf)

### FutureLearn 
Funded through our PRACE Training Centre, we previously developed a Supercomputing MOOC (Massively Open Online Course) under the FutureLearn platform which has been studied by many thousands of users [www.futurelearn.com/courses/supercomputing/](www.futurelearn.com/courses/supercomputing/). Although this provides a very professional look-and-feel that is designed to promote interaction between students, it is again a proprietary platform so it does not enable the material to be shared easily with other lecturers. This course was also purely conceptual with no practical exercises, and it is not clear how programming exercises could easily be accommodated into FutureLearn.

### Github 
The Carpentries courses, such as Software Carpentry, have all the materials stored online in a git repository with web pages created by standard templates, so it is easy to run a course with content tailored to local requirements and provide access to source code. This format is a great way to enable community driven course development. However, Carpentries courses are designed to be delivered face-to-face to a live audience and are generally aimed at novice users rather than those who have existing programming experience. Although the courses can easily be run online, the format does not lend itself to self-service courses as it is designed to be studied by following the material at the same pace as a live instructor.

![coderefinery 9da32dbc0a0d3d31](https://github.com/UNIVERSE-HPC/UNIVERSE-HPC.github.io/assets/106165178/d1146a1d-0f5f-46cf-9cc7-802c7d9ee09b)

### CodeRefinery
We became aware of the [CodeRefinery](https://coderefinery.org/) project through one of the other EuroCC NCCs (National Competency Centres) - NCC Sweden - who are actively involved in its development. It is based on the Carpentries model, but has a more modern look-and-feel and is designed for competent practitioners rather than novices, which better fits our HPC target audience. Although designed for synchronous delivery, the way that the material is laid out with easy navigation between sections makes it very suitable for self-service courses. What was missing was the ability to embed videos, but NCC Sweden kindly provided us with a simple way to do this. Like Carpentries, the CodeRefinery template is easily configurable. For example, it enables material to be conditionally included based on the values of environment variables so it will allow us to maintain many versions of our HPC course (dependent on target platform) in a single location but deploy a particular instance with minimal changes. Our hope is that this will allow HPC centres to easily contribute their own local developments to the main repository.

![archer 2 (new)](https://github.com/UNIVERSE-HPC/UNIVERSE-HPC.github.io/assets/106165178/2722e3b3-6eb0-4f56-aa4d-8c5aa6534310)

### Conclusions
We found it straightforward to put existing HPC material - articles, videos and practical exercises - into the CodeRefinery template. We are developing versions of our “Hands-on Introduction to HPC” course for two platforms hosted by EPCC (Cirrus and ARCHER2), so we can check that the local configuration options work as expected. To minimise the development effort, we are combining the existing online lectures and articles from the Supercomputing MOOC with the practical exercises from the existing face-to-face HPC Intro course. The initial version of the course is in beta-testing, but as soon as that is complete we will make it externally available - we have a target date of the end of August 2023. Keep an eye on the [ARCHER2 training pages](http://www.archer2.ac.uk/training) for updates where we will also enable users to obtain training accounts to run the practicals. In the meantime, however, you can access the beta-version at [https://epcced.github.io/Intro-to-HPC/](https://epcced.github.io/Intro-to-HPC/).

![Cirrus - cropped](https://github.com/UNIVERSE-HPC/UNIVERSE-HPC.github.io/assets/106165178/d214e7d0-b670-44fe-a81d-4b16471977e8)
