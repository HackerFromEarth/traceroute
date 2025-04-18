# traceroute
As part of a course I took during education:

Implementing a traceroute application using ICMP request and reply messages.

Traceroute is a computer networking diagnostic tool which allows a user to trace the route from a host running the traceroute program to any other host 
in the world. Traceroute is implemented with ICMP messages. It works by sending ICMP echo (ICMP type ‘8’) messages to the same destination with increasing 
value of the time-to-live (TTL) field. The routers along the traceroute path return ICMP Time Exceeded (ICMP type ‘11’) when the TTL field becomes zero. 
The final destination sends an ICMP reply 
(ICMP type ’0’) messages on receiving the ICMP echo request. The IP addresses of the routers which send replies can be extracted from the received packets.
The round-trip time between the sending host and a router is determined by setting a timer at the sending host. 

Your task is to develop your own Traceroute application in python using ICMP. 
Your application will use ICMP but, in order to keep it simple, will not exactly follow the official specification in RFC 1739.
