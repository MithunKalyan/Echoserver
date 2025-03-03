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
Server Code:
```
import socket
HOST,PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```

Client Code:
```
import socket
HOST,PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Mithun Kalyan P, 212223040142')
    print(f'Received: {s.recv(1024)!r}') 
```

## OUTPUT:
Server Side:
![Screenshot 2025-03-03 140756](https://github.com/user-attachments/assets/4a536543-710d-4147-b6c7-8a3814163274)

Client Side:
![Screenshot 2025-03-03 135754](https://github.com/user-attachments/assets/38bcfc20-4dc4-44f0-8b66-c60dbe1e72b0)

## RESULT:
The program is executed successfully
