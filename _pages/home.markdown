---
title: "Welcome to eNYPD"
permalink : /
layout: home
author: 
  - Bernhard Berger

---

Welcome to the home of *eNYPD*. It's name stands for *Entry Points Detector*
which is the actual purpose of *eNYPD*. Based on an application's used frameworks
*eNYPD* detects methods in Java-based software systems that can be controlled by
external users. This information is crucial for different kinds of security analyses,
such as Threat Modeling, input validation analyses, or security metric calculation.

Since the detection and extraction depends on the employed frameworks and requires
framework knowledge it is not an easy step. To help with out own anaylses and other
researchers, we implemented *eNYPD*. *eNYPD* is a static analysis to parse different
application artifacts, such as deployment descriptors, template files, and source
code to identify all existing entry points. *eNYPD* is based on [Soot](https://github.com/soot-oss/soot)
a greate OpenSource framework for static analyses.
