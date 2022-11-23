# WD-41-day-1

Question 1: Write a blog on Difference between HTTP1.1 vs HTTP2

Answer: HTTP stands for hypertext transfer protocol & it is used in client-server communication. By using HTTP user sends the request to the server & the server sends the response to the user. There are several stages of development of HTTP but we will focus mainly on HTTP/1.1 which was created in 1997 & the new one is HTTP/2 which was created in 2015.

HTTP/1.1: For better understanding, let’s assume the situation when you make a request to the server for the guvi.html page & server responds to you as a resource guvi.html page. before sending the request and the response there is a TCP connection established between client & server. again you make a request to the server for image img.jpg & the server gives a response as an image img.jpg. the connection was not lost here after the first request because we add a keep-alive header which is the part of the request so there is an open connection between the server & client. there is a persistent connection which means several requests & responses are merged in a single connection. These are the drawbacks that lead to the creation of HTTP/2: The first problem is HTTP/1.1 transfer all the requests & responses in the plain text message form. The second one is head of line blocking in which TCP connection is blocked all other requests until the response does not receive. all the information related to the header file is repeated in every request.

HTTP/2: HTTP/2 was developed over the SPDY protocol. HTTP/2 works on the binary framing layer instead of textual that converts all the messages in binary format. it works on fully multiplexed that is one TCP connection is used for multiple requests. HTTP/2 uses HPACK which is used to split data from header. it compresses the header. The server sends all the other files like CSS & JS without the request of the client using the PUSH frame.

Difference between HTTP/1.1 and HTTP/2 are:

HTTP/1.1
->Ithe usest works on the textual format.	
->There is head of line blocking that blocks all the requests behind it until it doesn’t get its all resources.
->It uses requests resource Inlining for use getting multiple pages
->It compresses data by itself.

HTTP 2
->It works on the binary protocol.
->It allows multiplexing so one TCP connection is required for multiple requests.
->It uses PUSH frame by server that collects all multiple pages 
->It uses HPACK for data compression.

Question 2: Write a blog about objects and its internal representation in Javascript

Answer:Object:
In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup, for example. A cup is an object, with properties. A cup has a color, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

Creating Objects in JavaScript:
1. By object literal
2. By creating instance of Object directly (using new keyword)

1. By object literal:
The syntax of creating object using object literal is given below:
     object={property1:value1; property2:value2;.....}

Property and value is separated by colon(:).
Example:
 var person={
    name:AAA,
    Age:10,
    school:Higher secoundar school
    };
    
2. By creating instance of Object directly (using new keyword):
The syntax of creating object directly is given below:   
    var objectname= newObject();
    
Here, new keyword is used to create object.

Example:
 var emp=new Object();
 emp.name="AAA";
 emp.id=10;
 
Accessing JavaScript Objects:
The syntax for accessing the property of an object is:

objectName.property

or

objectName[“property”]

Accessing ‘fname’ from example 1 using dot operator,
      person.fname;
      
Accessing ‘name’ form example 2 using [],
      emp["name"];



 
    
    
    
   

