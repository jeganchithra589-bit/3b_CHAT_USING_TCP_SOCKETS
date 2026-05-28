## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

# client.py

```
import socket
s = socket.socket()
s.connect(('localhost', 12345))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server >", s.recv(1024).decode())
```
# server.py
```
import socket
s = socket.socket()
s.bind(('localhost', 12345))
s.listen(5)
c, addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()
    print("Client >", ClientMessage)

    msg = input("Server > ")
    c.send(msg.encode())
```
## OUTPUT

<img width="1920" height="1080" alt="Screenshot (285)" src="https://github.com/user-attachments/assets/60167c9a-e423-47d0-8e96-7ea225f1680e" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
