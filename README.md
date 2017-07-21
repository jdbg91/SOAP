# SOAP Web Service

Use wsimport command. Wsimport tool is located on C:\JDK\path\bin

## Import Web Service without authentication

~~~
wsimport -keep http://domain.com/soapws?wsdl [-s C:\destiny\path]
~~~

## Import Web Service with authentication

Create an text file with the following content:

~~~
http://username:password@domain.com/soapws?wsdl
~~~

Put the file on C:\Users\Name\.metro\auth or user -Xauthfile option:

~~~
wsimport [-Xauthfile C:\auth\file\path\file.txt] -keep http://domain.com/soapws?wsdl [-s C:\destiny\path]
~~~

---

Those steps will create a package with some Java classes which can be use to connect to the web service.
