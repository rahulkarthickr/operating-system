# Operating System

### Introduction

- An Operating System (OS) is system software that manages computer hardware and software resources
- It provides a user interface and essential services for application programs
- It mitigates the difficulty of complex tasks i.e., abstracts the hardware details using system calls 
- Some of the popular Operating Systems are Windows , MacOS , Linux , etc . , 

### Types of Operating Systems
- **Batch Operating System:** Processes similar together as a batch to save time
- Example: Payroll processing systems where tasks are scheduled to run at night without user intervention
- **Time-Sharing Operating System**: Allows multiple users to use a computer simultaneously by quickly switching between them
- Example: University servers where multiple students can access resources simultaneously

![os](/Diagram/os.png)

# Key Concepts

### Process

- Each individual process is a seperate program and allocated seperate memory for that particular process
  
### Threads
- Threads are like smaller entities or units that share same space and memory within each individual process
  
- Basically , threads are the subprocesses within the main process
  
### Process Synchronization

- It is the technique that prevents the confusion and interference of two or more threads working at the same time in a process
  
### Process Concurrency

- It is the processing of multiple tasks one after the other where they have one interaction at a time
- They seem to be executed simultaneously in milliseconds but they doesn't
  
### Deadlock

- Deadlock is the situation in which two or more processes waiting for each other process to release the resource for their processing
- To understand in further, let's see an example where we have two programs, **Program A** and **Program B** sharing same resource file
- **Program A** has to read from the resource file and store the result in **Program B**
- Then , **Program B** has to write the result in the resource file
- To execute the writing process , **Program B** has started using the resource file 
- So, **Program A** can't read from the resource file and send the data to **Program B** needed for its processing
- Now , **Program B** waits for the data from **Program A** and **Program A** waits for the completion of **Program B**
- Most of the **'Not Responding'** cases in Windows OS are due to **Deadlock**
  
### Memory Management

- In OS , the most important task is allocation and de-allocation of memory for a particular process
- It's mainly responsible for the system's processing efficiency
  
### Process Scheduling Algorithms 

- Basically , scheduling means arrangement of the current and upcoming processes in a system
- Let's say we have 8-core CPU system and there are 10 processes waiting in the queue
- When one process gets over , another process gets scheduled to that particular core
- These processes are scheduled using specific algorithms , called as **Process Scheduling Algorithms**
- Some of the popular process scheduling algorithms are :
  
  - **First Come First Serve (FCFS)**
  - **Shortest Job First (SJF)**
  - **Longest Job First (LJF)**
  - **Round Robin**
  - **Priority Scheduling**
    
### File System and Storage

- Maintenance of storage devices like Pen drive , SSD , HDD , RAM , etc . , is also a responsibility of an OS
- We can organize data within these storage systems with kernel level support
  
### Inter Process Communication (IPC)

- It is the system via which two or more programs can communicate and synchronize with each other
- It consists of client-server architecture in which the two-way interaction between client and server happens in the same system
- Let's take an example in which two games **Game 1** and **Game 2** are running simultaneously
- IPC allows the communication of both games and synchronization processes like loading the saved file of **Game 1** into **Game 2**

### Virtual Memory 

- Virtual memory is simply the extension of the physical memory
- For example , we are having 32 GB RAM in our computer
- Let's say we are editing a film in our computer and 32 GB RAM is not that sufficient for our process
- The system is able to append extra 32 GB RAM into our system from the SSD or Hard Disk
- Now , the system thinks that we are having 64 GB RAM but the system processor once after using the current 32 GB RAM
- It starts using the extra 32 GB RAM which is actually pre-allocated into SSD or Hard Disk of the system

### Multi-Threading 

- It is the mechanism which ensures the combined working of multiple threads in a process
- We can signal these threads for proper functioning without any intervention between them
- **Mutex** and **Semaphores** are the key concepts applied here

### Mutex

- If multiple threads use the same resource , there may be a chance of
  
  - doubling of values in the resource
  - occurence of some other garbage values in the resource
  - overwriting first thread over the second and vice versa
    
- To avoid all these problems , the concept of **Mutex** was introduced
- Mutex is simply locking of the resource file by one particular thread until its processing with the resource is completed
- This is done so that no other thread tries to open that particular resource file

### Semaphores

- Semaphore is the signaling process when one thread completes its processing indicating the other threads that it has done its processing
- And , the resource file is given to the upcoming threads one-by-one in order for their processing

### Kernel mode

- Kernel mode is the mode in which user is able to interact directly with the hardware
- In Linux , we are using `sudo` command for performing operations in the kernel level i.e. , kernel mode

### User mode
- User mode is the mode in which user is normally performing operations without using `sudo` command
- In this mode , the operations are not done in the kernel level

### I/O Management

- I/O Management is simply the management of Input and Output devices
- It is one among the important responsibilities of an OS

### Disc Scheduling Algorithms

- To understand in detail , let's take a practical scenario
- Large number of processes are waiting in a queue for performing writing operation in the Hard disk
- OS uses specific algorithms to order these processes and allowing them to perform their operation
- These specific algorithms are called **Disc Scheduling Algorithms**
- Some of the popular disc scheduling algorithms are :
  
  - **LOOK**
  - **SCAN  (Elevator)**
  - **Circular LOOK (C-LOOK)**
  - **Circular SCAN (C-SCAN)**
  - **First Come First Serve (FCFS)**
  - **Shortest Seek Time First (SSTF)**

### File Permission and Security

- File Permissions should be managed by the OS
- OS takes care of specific files and folders which can't be deleted easily
- If those are deleted , OS may crash and the system turns to unusable state

### Virtualization

- Virtualization in OS refers to the creation of virtual versions of the computer resources
- Some of the computer resources are hardware platforms , storage devices , network resources
- It allows multiple **Virtual Machines (VMs)** to run on a single physical machine , each with its own OS
- It enables efficient resource utilization , isolation , scalability of computer resources

### Networking

- Networking basics is managed by the OS
- We can make multiple requests and communicate with the OS using varoius networking protocols
- These networking protocols should be supported by the OS

### Real-Time Operating System (RTOS)

- It is used mainly in **Embedded Systems**
- Let's see a real-time example to understand in detail
- If we have connected RTOS with a machine , it shows the machine's readings in real-time
- It operates directly at the kernel level , resulting in minimal latency
- It ensures that operations are executed within strict time constraints , maintaining consistent performance without any delay

### Security and Protection

- OS ensure security and protection by managing user access through authentication and authorization
- They enforce access control policies and isolate processes to prevent unauthorized interference
- They also employ encryption , secure communication protocols , regular updates to safeguard against vulnerabilities and malware

### System Calls

- System calls are interface functions provided by the OS
- It allows user applications to request services such as file operations , process management , etc . ,
- They act as a bridge between user-level programs and the kernel , ensuring secure & controlled access to hardware and system resources

### Load Balancing

- Load balancing in OS involves distributing workloads across multiple resources , such as CPUs or servers
- It ensures optimal performance and prevent any single resource from being overwhelmed 
- For example , in a web server environment , load balancing can distribute incoming requests across several servers
- It also improves the response time and reliability of the resources

### Fault Tolerance

- Fault tolerance refers to the system's ability to continue operating properly even when there's a failure in some of the components
- For example , in a distributed file system , data may be replicated across multiple servers
- So that if one server fails , the data remains accessible from other servers , ensuring continuous availability and reliability

### Recovery

- It is the process of restoring the system to a stable state after a failure or crash
- This often involves recovering lost data , rolling back transactions , reinitializing system components , etc . ,

### Multi Core Processing

- It is the ability to use multiple CPU cores simultaneously to execute tasks more efficiently
- Each core can handle its own thread or process , leading to improved performance and responsiveness
- For example , video editing softwares can use multiple cores to render different parts of a video simultaneously

### Asynchronous I/O

- It allows processes to initiate I/O operations
- And continue executing other tasks without waiting for the I/O operation to complete
- When the I/O operation is completed , it notifies the process
- So that the process can handle the completion of the I/O operation and continue from where it left off
- Multi-threading can use either **Blocking I/O** or **Non-Blocking I/O** , depending on the implementation
- While , **Asynchronous I/O** is associated only with **Non-Blocking I/O** 

### Performance and Tuning
- It involves optimizing system resources and configurations to improve efficiency and responsiveness of the system
- It includes adjusting parameters such as CPU scheduling , memory management , I/O handling to minimize bottlenecks , etc . ,
