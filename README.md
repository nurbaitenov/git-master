# git-master


### Rebase
```
git rebase - updates your branch to the latest main and reapplies you commits.
```

### Branch
```
It's a pointer to the latest commit in a line of development.
```

### Commit
```
Commit is a snapshot of a project at a specific point in time.
```

### Git reset vs git revert
```
git reset removes commits from the current branch by moving the branch pointer backward. It is mainly used for local commits that haven't been shared. git revert creates a new commit that undoes the changes of an earlier commit, making it the safer choice for shared branches.

In short:
reset - removes prev commit.
revert - creates new commit to undo previous commit.
```

What is Git?

Git is a distributed version control system (DVCS) that tracks changes in a project and stores its history as commits. It allows multiple developers to collaborate safely using branches and merges.

2. What is a repository?

A repository (repo) is a project that Git tracks, including its files and complete commit history. A repository can be local or remote (e.g., on GitHub).

3. What is a commit?

A commit is a snapshot of the staged changes in a project at a specific point in time. It is stored in the local Git repository.

4. What is a branch?

A branch is a pointer to the latest commit in a line of development. It allows developers to work independently without affecting other branches.

5. What is HEAD?

HEAD is a pointer to the branch or commit you are currently working on. It represents your current location in the repository.

6. What is the staging area?

The staging area is a temporary place where changes are prepared before creating a commit. Only staged changes are included in the next commit.

7. What does git add do?

git add stages modified or new files for the next commit. It does not create a commit.

8. What does git commit do?

git commit creates a snapshot of the staged changes and saves it in the local repository.

9. What does git push do?

git push uploads local commits to the remote repository and updates the remote branch if it can be updated safely.

10. What does git fetch do?

git fetch downloads the latest commits from the remote repository without changing your current branch.

11. What does git pull do?

git pull downloads the latest commits from the remote repository and merges them into your current branch.

12. What is git merge?

git merge combines the changes from one branch into another branch. It preserves the history of both branches.

13. What is a merge conflict?

A merge conflict occurs when Git cannot automatically combine changes because the same part of a file was modified in different branches. It must be resolved manually.

14. What is git rebase?

git rebase updates your feature branch to the latest version of another branch (usually main) and reapplies your commits on top of it. It creates a cleaner, linear history.

15. Why do we use rebase?

We use rebase to update our feature branch with the latest changes from main while keeping the commit history clean before opening a Pull Request.

16. What is the difference between merge and rebase?

git merge combines two branches together. git rebase moves your feature branch to the latest main and reapplies your commits on top of it.

17. What is git reset?

git reset moves the current branch back to an earlier commit, removing commits from the current branch. It is mainly used for local commits that have not been shared.

18. What is git revert?

git revert creates a new commit that reverses the changes introduced by a previous commit without removing it from the project's history.

19. What is .gitignore?

.gitignore is a file that tells Git which files and directories should not be tracked or committed. It is commonly used for secrets, generated files, and local configuration files.

20. What is git stash?

git stash temporarily saves uncommitted changes and restores a clean working directory. It is useful when you need to switch tasks without committing unfinished work.

21. What is a Pull Request (PR)?

A Pull Request is a request to merge one branch into another, usually into main. It allows teammates to review and approve code before it is merged.

22. Why do we use feature branches?

Feature branches let developers work on a specific task without affecting the stable main branch. After review, the branch is merged into main.

23. Why shouldn't we work directly on main?

Working directly on main increases the risk of introducing bugs into the shared codebase. Feature branches and Pull Requests provide review and testing before changes reach main.

24. Why is committing terraform.tfstate a bad idea?

terraform.tfstate may contain infrastructure details and sensitive information. It should be stored in a remote backend, such as GCS or S3, and excluded from Git using .gitignore.

25. Typical Git workflow

Create a branch, make changes, stage them with git add, commit with git commit, push the branch, update it with git fetch and git rebase if needed, open a Pull Request, and merge it into main after approval.




# Linux Network

1. Linux Networking

Linux networking allows the operating system to communicate with other devices over a network. It uses network interfaces, IP addresses, routing, DNS, and protocols such as TCP and UDP to send and receive data.

2. Network Interface (NI)

A network interface is the connection between a Linux machine and a network. It can be physical (Ethernet/Wi-Fi) or virtual (Docker bridge), allowing the system to send and receive network traffic.

3. Multiple Network Interfaces

A Linux machine can have multiple network interfaces for different purposes. For example, eth0 (or ens3) connects to the network, lo is used for local communication, and Docker creates docker0 for container networking.

4. Loopback Interface (lo)

The loopback interface (lo) is used for communication between applications running on the same machine. Traffic sent to 127.0.0.1 or localhost never leaves the server.

5. MAC Address

A MAC address uniquely identifies a network interface on the local network (Layer 2). It is a hardware identifier assigned to the network interface.

6. IP Address

An IP address identifies a device on an IP network, allowing other devices to communicate with it. It can be assigned dynamically by DHCP or configured statically.

7. Subnet Mask

A subnet mask determines which part of an IP address represents the network and which part represents the host. It helps Linux decide whether traffic should stay on the local network or be sent to the gateway.

8. Default Gateway

The default gateway is the router Linux uses to send traffic to other networks, such as the Internet. If a destination is outside the local subnet, Linux forwards the packet to the gateway.

9. DHCP

DHCP (Dynamic Host Configuration Protocol) automatically assigns network settings such as the IP address, subnet mask, gateway, and DNS server. Linux then configures these settings on the network interface.

10. DNS

DNS (Domain Name System) translates human-readable domain names, such as google.com, into IP addresses. This allows computers to locate and communicate with remote servers.

11. Routing Table

The routing table tells Linux where to send outgoing network packets. If no specific route matches the destination, Linux uses the default route through the gateway.

12. Port

A port identifies a specific application or service running on a machine. While the IP address identifies the machine, the port directs traffic to the correct application, such as SSH or Nginx.

13. TCP

TCP (Transmission Control Protocol) provides reliable, ordered communication between applications. It guarantees packet delivery by acknowledging and retransmitting lost packets.

14. UDP

UDP (User Datagram Protocol) provides fast communication without guaranteeing delivery or packet order. It is commonly used for DNS, streaming, and online gaming.

15. OSI Model

The OSI (Open Systems Interconnection) model is a conceptual networking model with seven layers that explains how data travels between devices. It helps engineers understand and troubleshoot network communication.

16. OSI Layers

Application → Presentation → Session → Transport → Network → Data Link → Physical. Each layer has a specific responsibility, from application protocols to physical transmission.

17. Application Layer

Provides network services to applications using protocols such as HTTP, HTTPS, SSH, and DNS.

18. Presentation Layer

Formats, encrypts, and compresses data before transmission. HTTPS uses TLS encryption at this stage.

19. Session Layer

Establishes, maintains, and terminates communication sessions between applications.

20. Transport Layer

Provides end-to-end communication using TCP or UDP and delivers data between applications.

21. Network Layer

Routes packets between networks using IP addresses. Routers primarily operate at this layer.

22. Data Link Layer

Transfers frames within the local network using MAC addresses. Switches primarily operate at this layer.

23. Physical Layer

Transmits raw bits over physical media such as Ethernet cables, fiber optics, or Wi-Fi.