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
##NAME :GURUPRASATH R
##REG NO: 212223040053

# echo-server.py

```python
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
```

# echo-client.py
```python

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

![WhatsApp Image 2024-09-04 at 21 22 23_61f66238](https://github.com/user-attachments/assets/93191edf-ffa2-4061-b175-55a33ccac03f)

![WhatsApp Image 2024-09-04 at 21 22 22_7df4ff80](https://github.com/user-attachments/assets/745b6dd7-0265-4b9b-a43b-a817015933ba)


## RESULT:
The program is executed successfully
