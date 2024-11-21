---
title: Containers with podman
series: 3
episode: 1
image: "/assets/images/byte-sized-rse/20241127-containers.jpg"
image_caption: <small>Photo by <a href="https://unsplash.com/@hdbernd">Bernd Dittrich</a> on <a href="https://unsplash.com/photos/a-stack-of-green-and-red-containers-sitting-on-top-of-each-other-rPM6qVp_tgk">Unsplash</a></small>
date: 27-11-2024 13:00 GMT
time-range: <a href="https://www.timeanddate.com/worldclock/fixedtime.html?msg=Byte-sized+RSE+-+Containers&iso=20241127T13&p1=136&ah=1&am=30" target="_blank" rel="noopener noreferrer">13:00-14:30 GMT</a>
instructors: Jeremy Cohen and Steve Crouch
slides: 
slides_tutorial: 
podcast: 
---

<strong>Registration:</strong> <a href="https://forms.gle/ryTFi5Yx9uJdg8bm9"
target="_blank" rel="noopener noreferrer">Register here</a>

Byte-sized RSE is back! In this first episode of season 3 of this series of short technical tutorials, we'll be looking at containers.
Containers provide a form of lighweight operating system-level "virtualisation" where a single operating system/kernel instance is able to support multiple isolated environments.
Within these environments, which are referred to as containers, applications are provided with a space that looks effectively like a separate computer system, even though multiple such containers may be running on a single operating system via a single kernel.
Containers can offer much better performance than full virtual machines while offering many of the benefits.
Container technologies have been around for some time and have been popularised most notably in recent years by the widespread use of Docker.
In this session, we'll be using a fully open source container engine, Podman, to demonstrate the use of containers.
However, if you're keen to work with Docker, the material that we cover in this session will work with Docker too.

**Prerequisites**: In order to be able to participate in the practical/interactive part of this session, you’ll need to install and test podman on your computer prior to the session.

There are detailed [instructions about installing podman](https://podman.io/docs/installation) on the podman website but we've also provided some futher information on podman, why we've chosen to use it and installing podman on Linux, macOS or Windows at: [https://www.universe-hpc.ac.uk/resources/byte-sized-rse/podman-info](https://www.universe-hpc.ac.uk/resources/byte-sized-rse/podman-info)
