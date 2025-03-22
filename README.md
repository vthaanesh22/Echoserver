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
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
client:
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Rakshitha P, 212223220083')
    print(f'Received: {s.recv(1024)!r}')
```
## OUTPUT:

server:
![Screenshot 2025-03-22 085222](https://github.com/user-attachments/assets/8390001c-be97-438f-a8ab-124803a025c5)


client:


![image](https://github.com/user-attachments/assets/7fa272b9-2434-4f20-9d26-d9072ef56b1d)


## RESULT:
The program is executed successfully
