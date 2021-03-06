---
title: "Usage"
layout: home
author: Wete
author_profile: true
---


* Abstract 

Which parts of a software system can be accessed
by an attacker is a common question in software security.
The answer to this question defines where to look for input
validation vulnerabilities, which parts of a system to respect
during Microsoft’s Threat Modeling, or how to calculate security
metrics. Identifying entry points of an application is, therefore,
a frequently occurring problem. Additionally, identifying entry
points is relevant when analysing many framework-based appli-
cations since they no longer have a simple main method.
While different analyses implement entry point detection, the
presented tool E NYPD explicitly focuses on answering this ques-
tion for Java-based systems in an analysis-independent manner. It
extracts information on entry points statically and persists this
information to a separate file. Therefore, it allows reusing the
information in different analyses, and researchers do not need
to implement a custom entry point detection for each analysis.
The presented tool is explained using Jakarta Server Faces,
a user-interface technology for Web-based business applications
implemented using Java. The paper presents the implemented
extraction approach, the internal data model, and the results
stored. Finally, in an evaluation, the statically assessed results of
E NYPD are compared to a dynamically determined set of entry
points. This comparison allows us to demonstrate the correctness
of the extracted information.

* Web Application Archive (WAR)
   * [WAR](../war-contents)
* XML-schema  
   * [XML-schema definition](../xml-schema-contents)
* eNYPD implementation  
   * [Implementation](../implementation)
* Quickstart  
   * [Installation and running example](../quickstart)
