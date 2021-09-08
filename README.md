# eNYPD

eNYPD is name stands for Entry Points Detector which is the actual purpose of eNYPD. Based on an application’s used frameworks eNYPD detects methods in Java-based software systems that can be controlled by external users. 
This information is crucial for different kinds of security analyses, such as Threat Modeling, input validation analyses, or security metric calculation.

### Quickstart

You can run eNYPD with the command line: java -jar eNYPD-0.0.1-SNAPSHOT-jar-with-dependencies <path to rt.jar> <path to war file>. 
   The QuickStart archive is an illustrative example how to use eNYPD. It is possible to obtain the entry points by running: 
  java -jar eNYPD-0.0.1-SNAPSHOT-jar-with-dependencies rt.jar QuickStart.
  Entry points are created and placed in xml files located in "QuickStart-1.0/eNYPD/Bean".

### Installation

Releases are available at [github](https://github.com/uni-bremen-agst/eNYPD/releases/tag/v1.0.0).
