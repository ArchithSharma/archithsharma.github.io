---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

*A full breakdown of coursework, honors, certifications, and skills is on the [Professional Development](/professional-development/) page.*

Education
======
* B.S. in Statistics & Machine Learning, Carnegie Mellon University, 2028 (expected), GPA: 3.5
  * Relevant coursework: Intro to Machine Learning, Statistical Computing, Statistics Graphics & Visualization, Concepts of Mathematics, Principles of Imperative Computation (C Programming)
  * Honors: CMU Summer Undergraduate Research Fellow (SURF, $4,500 award); Putnam Score of 2; Syracuse Basketball Analytics Competition winner; publication in the *Wharton Sports Analytics Journal* (Spring 2025); publication in the Dietrich College *WOVEN* Interdisciplinary Journal (forthcoming)
  * Certifications: Society of Actuaries Exam P (Mathematical Probability); DataCamp R Programming

Work experience
======
* Research Assistant, CMU Heinz College of Information Systems and Public Policy, October 2025 - Present
  * Ongoing research with Dr. Woody Zhu on deep-learning methods in earthquake detection
  * Developing an extension of CUSUM (Cumulative Sum Statistic for distribution change) to multiple data sources — see the [CUSUM Portal](/projects/cusum-portal/) project page
  * Supported by the CMU Summer Undergraduate Research Fellowship (SURF)

* Research Assistant, University of North Texas (UNT), August 2023 - May 2025
  * Conducted research with Dr. Junhyeon Kwon on bird population models for conservation action
  * Developed a synthetic simulation framework and ARMA & ARDL time-series tools using R and R Markdown — published as [Modeling American Kestrel Decline Using Spatiotemporal Subsampling to Improve eBird Data Reliability](/publication/2025-01-02-kestrel-decline-ebird-subsampling)

Projects
======
*The list below is pulled automatically from the [Projects](/projects/) page.*
  <ul>{% assign cv_projects = site.projects | where_exp: "p", "p.status != 'current'" | sort: 'order' %}{% for post in cv_projects %}
    {% include archive-project-cv.html %}
  {% endfor %}</ul>

Skills
======
Technical: R, Python, HTML, LaTeX, Java, C, C++, C#, MATLAB
Software: Tidyverse, PyTorch, Pandas, Object-Oriented Programming (OOP), Unity, Shiny
Analysis: Mathematical Modeling, Contextual Thinking, Data Wrangling
Soft Skills: Public Speaking, Organization, Building Relationships, Mathematical Thinking

Publications
======
*The list below is pulled automatically from the [Publications](/publications/) page.*
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Talks
======
*The list below is pulled automatically from the [Talks](/talks/) page.*
  <ul>{% assign cv_talks = site.talks | sort: 'order' %}{% for post in cv_talks %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>

Extracurriculars & Leadership
======
* Project Manager, Students Using Data for Social Good
* Board Member, Sports Analytics Club
* Founder & President, Birding@CMU
