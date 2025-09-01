---
title: "Projects"
date: 2025-09-01
draft: false
---
# Projects
This is a list of programming projects I've worked on. It may be incomplete, but my [github](https://github.com/amcsz) has most of the code I've written.

---

### TJCT Autograder v2
##### Links: [docker setup](https://github.com/TJ-Computer-Team/devenv), [website](https://github.com/TJ-Computer-Team/autograder2), [coderunner](https://github.com/TJ-Computer-Team/coderunner)

I created a new autograder system for our school's computer team in place of the old one. It is similar to codeforces and holds in-house contests regularly for our school.

The outfacing website was written in Django, with PostgreSQL to store user data. The internal system uses celery to manage submission tasks, which allows control over the number of concurrent tasks running at any given time. The coderunning service was written in rust for performance, and uses nsjail to sandbox user submissions in an isolated environment.

In [production](https://tjctgrader.org/), the website is run using two GCP virtual machines, one for the website and one for the coderunner, with nginx serving as a reverse proxy for both the website and for communication between the website and coderunner VMs.

---

### cserver
##### Links: [github](https://github.com/amcsz/cserver)

A WIP web server, written in c.