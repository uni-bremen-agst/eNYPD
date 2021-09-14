


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
* Quickstart  
   * Installation 
  Releases are available at [github](https://github.com/uni-bremen-agst/eNYPD/releases/tag/v1.0.0).
  After downloading the version of eNYPD above. 
  You can run eNYPD with the command line: 
  
  java -jar eNYPD-0.0.1-SNAPSHOT-jar-with-dependencies <path to rt.jar> <path to war file>. 

  * Running Example 
 [Here](https://github.com/uni-bremen-agst/eNYPD/tree/example) is an WAR- archive, we use it as illustrative example to show  how eNYPD works. 

  It is possible to obtain the entry points by running: 
  
  java -jar eNYPD-0.0.1-SNAPSHOT-jar-with-dependencies rt.jar QuickStart-1.0
  
  Entry points are created and placed in xml files located in "QuickStart-1.0/eNYPD/Bean". 
  
  As Example the Entry point for the "CommandButton" "Delete" in "users.xhtml": 
  
  
  
  ```xml
  
  <p:column style="text-align:center" >
        <p:commandButton value="Delete"
                        action="#{usersBean.delete(u)}"
                        update="users"/>
  </p:column>
  
  ```
  

  is 
  
 ```xml

<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<classesType xmlns="...">
    <class name="de.example.swt.controller.UsersBean" scope="javax.faces.view.ViewScoped" package="de.example.swt.controller">
        <attributeOrMethod>
            <method name="delete" return="void">
                <parameter>de.example.swt.model.User</parameter>
            </method>
        </attributeOrMethod>
    </class>
</classesType>
 
  
  ```
