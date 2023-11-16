---
layout: single  
title: Training Material
permalink: /resources/training-material/
author_profile: false
sidebar:
  nav: "uhpc_menu"
---

## Course Material

All the material is hosted [here](https://github.com/UNIVERSE-HPC/course-material) written in github flavored markdown with a few custom directives to indicate callouts, problem and solutions blocks. Each section also has its own metadata header section in YAML, which contains information on the name, the dependencies of each section, and the attribution information for that section of material. The format is described in more detail in the [CONTRIBUTING.md](https://github.com/UNIVERSE-HPC/course-material/blob/main/CONTRIBUTING.md)

## Course website

To render the material in a form suitable for running courses, we have written a website called [Gutenberg](https://github.com/OxfordRSE/gutenberg). You can see an example deployment of this website by the Oxford Research Software Engineering [here](https://train.oxrse.uk/). The website renders the material as static webpages, but also has a database and backend for hosting course "events". Events are comprised as a linear series of modules along with timing and location information and pointers to material. Students can enrol on courses, and tick off problems as they complete them, enabling instructors to track progress. Students can also comment directly on the material in order to obtain asynchronous, remote feedback from other students and instructors if required. 

## Courses and Modules

| Course | Module | Description |
| --- | --- | --- |
| [Software Architecture and Design](https://train.oxrse.uk/material/software_architecture_and_design) | [Procedural Programming](https://train.oxrse.uk/material/software_architecture_and_design/procedural) | Procedural Programming is based around the idea that code should be structured into a sequence of **procedures** that operate on data. This course will introduce you to the basics of procedural programming in either Python or C++.  |
| | [Object-Orientated Programming](https://train.oxrse.uk/material/software_architecture_and_design/object_orientated) | The Object Oriented Paradigm builds upon the Procedural Paradigm, but builds code around data. This course will introduce you to the basics of Object Oriented Programming in either Python or C++.  |
| | [Functional Programming](https://train.oxrse.uk/material/software_architecture_and_design/functional) | Functional Programming is based around the idea that programs are constructed by applying and composing/chaining **functions**. This course will introduce you to the basics of functional programming in either Python or C++.  |
| [Technology and Tooling](https://train.oxrse.uk/material/technology_and_tooling) | [The Bash shell](https://train.oxrse.uk/material/technology_and_tooling/bash_shell) | The Bash shell is a command-line interface used in Unix-based operating systems such as Linux and macOS. This course will introduce you to the basics of using the Bash shell.  |
| | [Version Control](https://train.oxrse.uk/material/technology_and_tooling/version_control) | This course introduces the basics of version control using the Git version control system. We will learn how to setup Git, and use it to track changes in our code.  |
| | [Packaging and Dependency Management](https://train.oxrse.uk/material/technology_and_tooling/packaging_dependency_management) | This course introduces the basics of packaging and dependency management in Python and C++. For Python, we introduce `venv` for virtual environments, and `pip` for package management and how to structure a modern Python package and publish it to PyPI. For C++, we introduce the CMake build system and how use it to manage dependencies and the build process.  |
| | [Best Practices](https://train.oxrse.uk/material/technology_and_tooling/best_practices) | This course covers how to style your Python code, and use linters to enforce a consistent style and highlight any code that can lead to commonly encountered bugs or problems.  |
| | [IDEs](https://train.oxrse.uk/material/technology_and_tooling/ide) | Integrated Development Environments (IDEs)provide programmers with a complete development environment to write, edit, debug, and deploy their code. This course introduces the popular VSCode IDE, both for Python and C++ development.  |
| | [Testing](https://train.oxrse.uk/material/technology_and_tooling/testing) | This course introduces the basics of automated testing and debugging in Python, using the Pytest framework.  |
| | [Containerisation with Docker](https://train.oxrse.uk/material/technology_and_tooling/docker) | This course aims to introduce the use of Docker containers with the goal of using them to effect reproducible computational environments.  |
| | [Snakemake Tutorial](https://train.oxrse.uk/material/technology_and_tooling/snakemake) | This tutorial introduces the text-based workflow system Snakemake.  |
| [Software Project Management](https://train.oxrse.uk/material/software_project_management) | [Collaboration on GitHub](https://train.oxrse.uk/material/software_project_management/collaboration) | This course will show you how to use Git for effective collaboration with others using the GitHub platform. After completion of the course, you will be able to contribute to projects on GitHub, including opening issues and pull requests.  |
| | [Continuous Integration](https://train.oxrse.uk/material/software_project_management/continuous_integration) | This course introduces the concept of continuous integration and how to set it up for a Python project using GitHub Actions.  |
| [High Performance Computing](https://train.oxrse.uk/material/high_performance_computing) | [Introduction to High Performance Computing](https://train.oxrse.uk/material/high_performance_computing/hpc_intro) | An introduction to high-performance computing (HPC), covering connecting to HPC resources and the slurm job scheduler.  |
| | [HPC Scalability Profiling](https://train.oxrse.uk/material/high_performance_computing/hpc_scalability_profiling) | This session introduces the concept of scalability and how to profile the scalability of your code with an increasing number of cores.  |
| [Introductory Courses](https://train.oxrse.uk/material/introductory_courses) | [Intro to Python](https://train.oxrse.uk/material/introductory_courses/python) | This course introduces the basics of programming in Python. We will learn how to run Python code, and how to use variables, functions, and control flow. We will also learn how to use Python for data analysis and visualization.  |