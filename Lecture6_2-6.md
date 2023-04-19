# Lecture 6 - 2/6/2023
Catya Temkin

## Version Control Systems
- Simplify maintaining code 

### Centralized Systems 
![centralized system diagram](https://www.htown-tech.com/uploads/6/9/4/9/69493533/centralized-vs-distributed-version-control-system-2_orig.jpg)

- There is **one** unified history 
    - everyone has to agree on avalible versions
    - clients just have a set of "working" files
    - to commit changes, client must reconnect to the main server  
- Pros:
    1. Possible to look at past versions 
    2. Simplicity of a single server 
- Cons:
    1. Single server may go offline 
    2. Must be connected to server to commit (need access to internet)

### Distributed Systems
![distributed system diagram](https://www.htown-tech.com/uploads/6/9/4/9/69493533/centralized-vs-distributed-version-control-system-3_orig.jpg)

- Shared history
    - Clients make a copy of the systems history when checking out code
    - Clients check in/commits to their personal history 
- Pros:
    1. No need for internet to commit 
    2. No problem if server goes offline
- Cons:
    1. Redundancy (multiple copies of history)
    2. Potential for disagreement 
        - need way to resolve conflicts and share histories 
- Git is a distributed verson control system 
### Encoding the History of a Repository
- track the changes (delta)
    - can use tools called diff and patch
- **snapshots** are full copies of changed files
    - unchanged files are pointers to the previous version
- Git uses snapshots 
- The Git workspace has **3** different states/loactions
    1. Working directory 
    2. Staging 
    3. Repository (history)
- Useful and related Git commands
    - git status => view current status 
    - git log => sequence and information of past commits 
    - git add => move from working directory to staged
    - git restore --staged => move from staged back to working directory
    - git commit => move from staged to repository
    - git reset --soft HEAD^ => undo commit
    - git checkout => move from repository to working directory
