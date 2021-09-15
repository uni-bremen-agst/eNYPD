The structure of web applications, especially JSF applications, reveal documents of several types. In the details we have Xhtml, java, XML and other resources like scripts, images, libraries.
The figure below is a partial representation of a WAR-archive, everything in red is present in all web applications.

![WAR]({{site.baseurl}}/assets/images/war.pdf)

Each file or folder existing in this schema has a very specific purpose: 

 * lib
Content the library needed in the project.

 * xml File 

Xml files are used for setting up web applications, for example web file.xml, beans.xml, faces-config.xml, taglib.xml ...

 * classes 
Content the .class of the web applications.

 * Facelets 

The Facelets files themselves usually use the .xhtml extension and therefore often call as "xhtml" instead of Facelets.
