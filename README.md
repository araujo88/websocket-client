# websocket-client
A simple web client which sends HTTP/1.1 GET requests given a hostname/IPv4 address and port and then prints the responses (if more than one, chunked) on screen as well as server data (name, aliases, IPv4 addresses and IPv6 addresses). Implemented using websocket.h library from C/Unix.

Usage: 
 - Using hostname: ``` ./client.o -hostname www.example.com -port 80 ```
 - Using IP address (IPv4): ``` ./client.o -ipaddr 74.6.231.21 -port 80 ```

The last example sends a GET request to www.yahoo.com.

In both examples the default port for internet traffic is utilized (PORT 80).
