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
Server :
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)

client:
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Rakshitha P, 212223220083')
    print(f'Received: {s.recv(1024)!r}')

## OUTPUT:

server:

![server](https://github.com/user-attachments/assets/d1662266-77ee-4f7f-8fea-8afda42e16ef)

client:


![client](https://github.com/user-attachments/assets/4d39eea7-b4f2-40db-ae34-b8097f50a965)


## RESULT:
The program is executed successfully
