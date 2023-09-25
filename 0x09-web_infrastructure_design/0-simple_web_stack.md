# 0. Simple web stack

![0-simple_web_stack](https://github.com/MennaAnwar/alx-system_engineering-devops/assets/79084467/3afba729-6b40-42d2-adc0-e4c1bdbd18ea)

## Specifics About This Infrastructure:

* ### What is a server?
  A server is a computer hardware or software that provides services to other computers, which are usually referred to as *clients*.

* ### What is the role of the domain name?
  The role of a domain name is to provide a human-readable way to access Internet resources.
  When you enter a domain name into a web browser, the browser sends a request to a Domain Name System (DNS) server.
  The DNS server then translates the domain name into the corresponding IP address, and the browser connects to the resource at that address.

* ### What type of DNS record `www` is in `www.foobar.com`?
`www.foobar.com` uses an **A record**. This can be checked by running `dig www.foobar.com`.<br/>**Note:** the results might be different but for the infrastructure in this design, an **A** record is used.<br/>
<i>Address Mapping record (A Record)—also known as a DNS host record, stores a hostname and its corresponding IPv4 address.</i>

* ### What is the role of the web server?
  The web server is a software/hardware that accepts requests via HTTP or secure HTTP (HTTPS) and responds with the content of the
  requested resource or an error messsage.

* ### What is the role of the application server?
  To install, operate and host applications and associated services for end users, IT services and organizations and facilitates the
  hosting and delivery of high-end consumer or business applications

* ### What is the role of the database? 
  To maintain a collection of organized information that can easily be accessed, managed and updated

* What is the server using to communicate with the computer of the user requesting the website?
  Communication between the client and the server occurs over the internet network through the TCP/IP protocol suite.

## Issues With This Infrastructure

* ### There are multiple SPOF (Single Point Of Failure) in this infrastructure:
  For example, if the MySQL database server is down, the entire site would be down.

* ### Downtime when maintenance needed:
  When we need to run some maintenance checks on any component, they have to be put down or
  the server has to be turned off. Since there's only one server, the website would be experiencing a downtime.

* ### Cannot scale if there's too much incoming traffic:
  It would be hard to scale this infrastructure becauses one server contains the
  required components. The server can quickly run out of resources or slow down when it starts receiving a lot of requests.
