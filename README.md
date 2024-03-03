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



## OUTPUT:

![ethical4](https://github.com/Gajalakshmivelmurugan/Echoserver/assets/144871940/0713ad4c-4a22-4597-bd06-f1633d9e7c93)

![hacking2](https://github.com/Gajalakshmivelmurugan/Echoserver/assets/144871940/4bcbe366-6782-43a1-a149-4a8e599dcd58)


## RESULT:
The program is executed successfully
