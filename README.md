Download Link: https://assignmentchef.com/product/solved-cs-39006-assignment-3-concurrent-server-implementation-assignment
<br>
<strong>Objective: </strong>

The objective of this assignment is to implement a concurrent server where multiple clients can requests for same or different services and the server serves them concurrently. The implementation will help you to understand the functionality of the ​select() system call used for servicing multiple requests over different sockets.




<strong>Problem Statement:</strong>

Your task is to implement a server and two clients with two different service requests. The server can receive two different service requests from the clients as follows.

<ol>

 <li><em>Request for a bag of words</em>​, where the server will forward a set of words from a file txt ​one after another over a stream socket. The file ​word.txt ​contains a set of words, one each at every line. Once the server receives a request for the words, it reads the words from the file and forwards them one after another, each as a null terminated string. The end of service is marked with an empty string (a string only with a null character). Once the client receives that empty string, it prints the number of words received and exits.</li>

 <li><em>Request for the IP address corresponding to a domain name</em>​, where the client requests for the IP address of a domain, say <u>​</u><a href="http://www.iitkgp.ac.in/">iitkgp.ac.in</a>,​ over a datagram socket. The server looks up for the IP address by using the system call ​gethostbyname(). The server returns this IP address to the client. The client prints the IP address and exits.</li>

</ol>




You have to implement two clients, one corresponding to each of the services as mentioned above. Note that the client requesting bag of words works over a stream socket, whereas the client requesting for the IP address works on a datagram socket.




The server can receive multiple service requests simultaneously from different clients, and it needs to respond to each client with the corresponding response.




<strong>Submission Instruction: </strong>

You should write three C programs – ​selectserver.c (contains the server program), bowclient.c (for bag of words requests) and dnsclient.c​ (for IP address requests). Keep these three files in a single compressed folder (zip or tar.gz) having the name &lt;roll number&gt;_Assignment3.zip or &lt;roll number&gt;_Assignment3.tar.gz. Upload this compressed folder at Moodle course page by the deadline (24th Jan 2019 2:00 PM).