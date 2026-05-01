TCP Network Programming Mini Project

This project demonstrates the fundamental concepts of **network programming using TCP sockets in C**, developed as a learning extension of the IE2102 Network Programming module.

---

Objective

To understand and implement core networking concepts such as:

- Client–Server architecture  
- Socket programming (`socket`, `bind`, `listen`, `accept`)  
- TCP communication (`send`, `recv`)  
- Iterative vs Concurrent servers  
- Process creation using `fork()`  
- Signal handling (`SIGCHLD`)  
- Zombie process prevention using `waitpid()`  

---

Project Stages

Stage 1 – Basic TCP Communication
- Single client-server communication  
- Echo server implementation  
- Blocking I/O model  

Stage 2 – Concurrent Server (fork)
- Multi-client support using `fork()`  
- Parent process accepts new connections  
- Child process handles client communication  
- Proper socket descriptor management (`sockfd` vs `connfd`)  
- Zombie process prevention using `SIGCHLD` and `waitpid()`  

---

Key Concepts Demonstrated

- TCP is stream-based (no message boundaries)  
- Difference between listening socket and connection socket  
- Blocking system calls (`accept`, `recv`)  
- Signal interruption (`EINTR`)  
- Process lifecycle and cleanup  

---

Technologies Used

- C Programming  
- POSIX Sockets  
- Linux (Kali / Ubuntu)  

---

How to Run

```bash
gcc server.c -o server
gcc client.c -o client

./server
./client
