---
layout: archive
title: ""
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---
<div class="cv-download-links">
  <a href="{{ base_path }}/files/CV.pdf" class="btn btn--primary">Download CV as PDF</a>
</div>

{% include base_path %}

Education
======
* Ph.D in Distributed Systems, Sorbonne Université, 2025
* Master in CS, Software Engineering, TU Kaiserslautern, Germany, 2022
* Bachelor of Technology, APJ Abdul kalam technical university, India, 2017

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  

Work experience
======

*  2022-2025: PhD Researcher, LIP6, Sorbonne Université (UPMC), Paris 
    * Thesis: CALock: topological multi-granularity locking in hierarchies
    * Designed, implemented and verified a new locking protocol for parallel threads over hierarchical data. CAlock identifies an optimal grain size for locking in a hierarchy of data structures.
    * Implemented and verified several thread synchronization protocols in java and C++ as well graph database implementations in TinkerPop (gremlin) as proof of concept. Performed benchmarks for performance evaluation.
    * Collaboration in projects involving industry partners and research labs. Ongoing collaboration with Telecom sud-Paris to design, implement and formally verify a distributed graph database. Second ongoing work within LIP6 on the specification and verification of a distributed key-value store.

* 2021-2022: Research Intern, LIP6, Sorbonne Université (UPMC), Paris
    * Implementation of a cache for a CRDT datastore. Worked on designing and implementing an in memory cache and checkpoint store for AntidoteDB.
    * Undertook performance benchmarking in a distributed environment with Riak Bench.
    * Fixed several bugs in the general implementation of AntidoteDB and achieved a 40% performance improvement in the read path.
    * Tech Report: Persisting the AntidoteDB Cache


* 2020-2021: Full stack Web Engineer, LernFair e.v., Remote, Germany
    * Worked on the development of an online learning platform for school students to facilitate remote learning during Covid-19 lockdowns.
    * Implemented the frontend in ReactJS and the backend in NodeJS and GraphQL along with alpha and beta testing of features.
    * Implemented the service layer in a microservice architecture with content delivery through REST APIs.

* 2020-2021: Research Assistant, German Center for AI (DFKI), Kaiserslautern, Germany
    * Developed a custom tool for visual graph editing tool with automated graph structuring and enforcing  P&ID constraints on nodes and edges of the graph in AngularJS and D3.js.
    * Writing test suites for performance. testing on peak loads and high data volumes with python.
* 2017-2019: Software Engineer, Newgen Software Technologies, India
    * Development of custom workflow, content management and business process automation solutions for major Banks, Health care providers and insurance companies.
    * Developed custom dashboards and reports for telemetry and report generation.
    * Delivered technical training and support to business clients in the Asia pacific region.

<!-- Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3 -->

Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
<!-- Service and leadership
======
* Currently signed in to 43 different slack teams -->
