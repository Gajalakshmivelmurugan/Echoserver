# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
Name:Gajalakshmi.V
reg no:212223040047

### SERVER CODE:

import socket


HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
### CLIENT CODE:

import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)


print(f"Received {data!r}")

```

## OUTPUT:
![etical1](https://github.com/Gajalakshmivelmurugan/Echoserver/assets/144871940/92552dba-8967-4c98-b994-ea5bca845858)
![hacking4](https://github.com/Gajalakshmivelmurugan/Echoserver/assets/144871940/91cb8dd3-816c-4b9d-8c9b-da035424cfac)


## RESULT:
The program is executed successfully
