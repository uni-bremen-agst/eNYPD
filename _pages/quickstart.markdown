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
    <class name="de.example.swt.controller.UsersBean" 
           scope="javax.faces.view.ViewScoped" 
           package="de.example.swt.controller">
        <attributeOrMethod>
            <method name="delete" return="void">
                <parameter>de.example.swt.model.User</parameter>
            </method>
        </attributeOrMethod>
    </class>
</classesType>
 
  
  ```
