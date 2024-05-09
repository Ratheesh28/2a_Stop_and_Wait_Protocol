# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
  i=input("Enter the data: ")
  c.send(i.encode())
  ack=c.recv(1024).decode()
  if ack:
      print(ack)
      continue
  else:
      c.close
      break
```
## Server
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   print(s.recv(1024).decode())
   s.send("Acknowledgement Received".encode())
```
## OUTPUT
## Client:
![318390935-c61548a3-524b-4eb4-9759-484fe37e53bf](https://github.com/Ratheesh28/2a_Stop_and_Wait_Protocol/assets/138849186/ffd2cdbe-5399-4bf1-9465-ff6b2c0fc264)
## Server:
![318391145-2d5a89d8-35f3-4773-9934-01f08dc46ed3](https://github.com/Ratheesh28/2a_Stop_and_Wait_Protocol/assets/138849186/3dc81573-8086-438d-b0f4-b0536383953e)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
