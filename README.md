# JSF-Hello-World
JSF – JavaServer Faces is a java MVC framework for web application. It help us to make user interface with less code and time.

# MVC and JSF

M – Model – Entity, Data, business layer.
V- View -JSp,jsf, xhtml page.
C- Controller – Managed bean.

HelloWorldBean.java
```java
package bean;

import java.io.Serializable;

public class HelloWorldBean implements Serializable{

	/**
	 * 
	 */
	private static final long serialVersionUID = 1L;
	
	private String fname;
	private String lname;
	public String getFname() {
		return fname;
	}
	public void setFname(String fname) {
		this.fname = fname;
	}
	public String getLname() {
		return lname;
	}
	public void setLname(String lname) {
		this.lname = lname;
	}

}

```
helloworld.xhtml
```xhtml
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:h="http://java.sun.com/jsf/html"
      xmlns:f="http://java.sun.com/jsf/core">
	<body>
		
		<h:form>
    	   <h:inputText value="#{helloworldbean.fname}"></h:inputText>
    	    <h:inputText value="#{helloworldbean.lname}"></h:inputText>
    	   <h:commandButton value="Next" action="success"></h:commandButton>
    	</h:form>
	
	</body>
</html>
```
successmsg.xhtml
```xhtml
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:f="http://java.sun.com/jsf/core"
      xmlns:h="http://java.sun.com/jsf/html">
	<body>
		<h1>Hello World From </h1>#{helloworldbean.fname}&nbsp;#{helloworldbean.lname}
	</body>
</html> 
```
