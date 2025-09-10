# 2a_Stop_and_Wait_Protocol
## name:joshitha shree bs
## reg no:212224230107
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## sender(server)
## PROGRAM
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
     print(ack)
     continue
    else:
     c.close()
     break
```
## OUTPUT
<img width="852" height="82" alt="Screenshot 2025-09-10 110621" src="https://github.com/user-attachments/assets/b5c19632-e3cb-4efc-822f-ad607869b988" />

## receiver(client)
## program
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recieved".encode())
```
## output
<img width="835" height="72" alt="Screenshot 2025-09-10 110637" src="https://github.com/user-attachments/assets/197ac33b-2d1c-471e-89c5-b78f751d831f" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
