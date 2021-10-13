# websocket-client
A simple web client which sends HTTP/1.1 GET requests given a hostname/IPv4 address and port and then prints the responses (if more than one, chunked) on screen as well as server data (name, aliases, IPv4 addresses and IPv6 addresses). Implemented using websocket.h library from C/Unix.

Compilation: ``` gcc client.c -o client.o ```

Usage: 
 - Using hostname: ``` ./client.o -hostname www.example.com -port 80 ```
 - Using IP address (IPv4): ``` ./client.o -ipaddr 74.6.231.21 -port 80 ```

The last example sends a GET request to www.yahoo.com.

In both examples the default port for internet traffic is utilized (PORT 80).

Example of a server response (www.example.com:80):

```
Method: -hostname
Creating socket ...
Socket created!
Connecting to server www.example.com...
name: www.example.com
IPv4 address: 93.184.216.34
IPv6 address: 5db8:d822::
Connected!
Request:
GET / HTTP/1.1
Host:www.example.com:80
Connection: close


Sending request ...
---------------------------------------------------------------


Response 0:
HTTP/1.1 200 OK
Accept-Ranges: bytes
Age: 488150
Cache-Control: max-age=604800
Content-Type: text/html; charset=UTF-8
Date: Wed, 13 Oct 2021 03:21:56 GMT
Etag: "3147526947"
Expires: Wed, 20 Oct 2021 03:21:56 GMT
Last-Modified: Thu, 17 Oct 2019 07:18:26 GMT
Server: ECS (agb/A445)
Vary: Accept-Encoding
X-Cache: HIT
Content-Length: 1256
Connection: close

<!doctype html>
<html>
<head>
    <title>Example Domain</title>

    <meta charset="utf-8" />
    <meta http-equiv="Content-type" content="text/html; charset=utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <style type="text/css">
    body {
        background-color: #f0f0f2;
        margin: 0;
        padding: 0;
        font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
        
    }
    div {
        width: 600px;
        margin: 5em auto;
        padding: 2em;
        background-color: #fdfdff;
        border-radius: 0.5em;
        box-shadow: 2px 3px 7px 2px rgba(0,0,0,0.02);
    }
    a:link, a:visited {
        color: #38488f;
        text-decoration: none;
    }
    @media (max-width: 700px) {
        div {
            margin: 0 auto;
            width: auto;
        }
    }
    </style>    
</head>

<body>
<div>
    <h1>Example Domain</h1>
    <p>This domain is for use in illustrative examples in documents. You may use this
    domai

Response length: 1448
---------------------------------------------------------------
```
