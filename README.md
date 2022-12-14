# File Sharing System
Created a secure File Sharing System where the multithreaded server listens for requests from multiple clients and sends the requested files.

## Implementation
1. Three Peers A,B and C are created
2. On running both peerA.py, peerB.py, peerC.py it is asked that whether you want to act as a client or a server
3. When one peer chooses to acts as a server, the other two peers can act as clients and connect to the server
4. The clients can then start sending the files to the server
5. The clients can run infinitely until the user explicitly enters "EXIT" and the multithreaded server will continue to listen for the clients 

## How To Run The Code On Remote Raspberry Pis And Your Local Machine :
The steps are the same for running the files on your local machine except that the files to be run on your local machine are placed in the "Run_on_local" folder. The differences between the two sets of files are as follows :  
  
In the python files (peerA.py, peerB.py, peerC.py) of Run_on_local :  
* The host ip is retrieved using "socket.gethostbyname()" function  
  
In the python files (peerA.py, peerB.py, peerC.py) placed outside Run_on local which are to be run on remote raspberry pis :  
* The host ip is explicity mentioned as "10.35.70.9" which had to be done so that a client program running on one raspberry pi can connect to another raspberry pi running a server program  
  
### Steps  
1. Install tqdm using the command :   
    For Mac and raspberry pi : pip3 install tqdm  
    For Windows : pip install tqdm
2. Run the file peerA.py on a terminal window run the following command :  
    For Mac and raspberry pi : python3 peerA.py  
    For Windows : python peerA.py
3. Run the file peerB.py on a second terminal window  
    For Mac and raspberry pi : python3 peerB.py                              
    For Windows : python peerC.py
4. Run the file peerC.py on a third terminal window  
    For Mac and raspberry pi : python3 peerC.py                              
    For Windows : python peerC.py
5. If you choose to run the peer as a SERVER, the password is : server
6. If you choose to run the peer as a CLIENT, the password is : client
7. Enter the filepath on the client side
8. After the file is transferred, the client starts again from step 5  
9. If the client wishes to exit, enter : EXIT
10. The multithreaded server will keep on running and listening for clients to connect
