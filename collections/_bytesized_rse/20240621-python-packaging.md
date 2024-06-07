---
title: Python packaging and pip
series: 2
episode: 8
image: "/assets/images/byte-sized-rse/20240621-packaging.jpg"
image_caption: <small>Photo by <a href="https://unsplash.com/@agenlaku">Agenlaku Indonesia</a> on <a href="https://unsplash.com/photos/three-brown-boxes-sitting-on-top-of-a-yellow-surface-pxz1DfpNEs0">Unsplash</a></small>
date: 21-06-2024 13:00 BST
time-range: <a href="https://www.timeanddate.com/worldclock/fixedtime.html?msg=Byte-sized+RSE+Season+2,+Session+8+-+Python+packaging&iso=20240621T13&p1=136&ah=1&am=30" target="_blank" rel="noopener noreferrer">13:00-14:30 BST (UTC+1)</a>
instructors: Jeremy Cohen and Steve Crouch
slides: 
slides_tutorial: 
podcast: 
---

<strong>Registration:</strong> <a href="https://forms.gle/UwNxx5GvtAtzxKXu5"
target="_blank" rel="noopener noreferrer">Register here</a>

In this final episode of season 2 of byte-sized RSE, we’ll be looking at Python packaging.
We’ll do this from both the user and package creator perspective.
There are different package infrastructures in Python and we’ll focus here on the core packaging ecosystem maintained by the Python Packaging Authority (PyPA) and the pip package installer tool.
 
We’ll begin by looking at the use of pip to install packages and what actually happens when you install a package.
Then we’ll look at the anatomy of a Python package and create a simple package ourselves, to see how one is structured and built.
 
**Prerequisites**: In order to be able to participate in the practical/interactive part of this session, you’ll need a computer with a regular CPython installation (i.e. not Anaconda) and pip available.
You’ll also need some basic familiarity with working on the command line and be familiar with a command line-based editor such as nano, vi or emacs to enable you to easily edit files.
The tutorial may also work using pip via Anaconda but this is not a supported setup for this session.
