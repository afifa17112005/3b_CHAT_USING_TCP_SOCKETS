# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
Name:A.Afifa Reg.no: 212223040008
## PROGRAM:
## CLIENT:
```import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER:
```import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT:
## CLIENT:
![326075576-cf17f7a9-8c0f-43ca-b4e7-bfb6837630d7](https://github.com/afifa17112005/3b_CHAT_USING_TCP_SOCKETS/assets/147080931/df5269eb-d751-4af9-9f05-9969a1d64758)

## SERVER:
![326163730-eae4ba2a-8dd3-4dae-b2a7-0c6d1c305bf8](https://github.com/afifa17112005/3b_CHAT_USING_TCP_SOCKETS/assets/147080931/4a8b3094-6215-4448-b99b-e0a3cd69d003)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
