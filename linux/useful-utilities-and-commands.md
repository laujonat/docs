---
description: >-
  A process refers to a program in execution; it’s a running instance of a
  program. It is made up of the program instruction, data read from files, other
  programs or input from a system user.
---

# Process Management

## Viewing Active Processes

* The ps utility displays a header line, followed by lines containing information about all of your processes that have controlling terminals. 

#### Listing Processes

```text
# ps = process status
# a = show processes for all users 
# u = display the process's user/owner 
# x = also show processes not attached to a terminal

$ ps aux
```

* SSH in and then use the ps command to list running processes in conjunction with the `(grep|egrep)` command to filter that result list down to what you need.

```text
$ ps aux | egrep <thing>
```

* For example, connect to `localhost` with `ssh`. Running our command, we can see a user is connected to our local system. 

```text
$ ssh localhost
Last login: Sat Sep  7 22:49:42 2019

$ ps aux | egrep ssh
user  74065   0.3  0.0  4258648    208 s011  R+   11:13PM   0:00.00 egrep ssh
user  30622   0.0  0.0  4381564   1148   ??  S     6:50PM   0:00.23 sshd: user@ttys011
root  30569   0.0  0.0  4325312   5984   ??  Ss    6:49PM   0:00.05 sshd: user[priv]
user  30568   0.0  0.0  4396884   5876 s007  S+    6:49PM   0:00.27 ssh localhost
```

#### Killing Processes

* The output from the second column from the `ps aux` is the `PID`

```text
$ kill 30568 # kill user ssh localhost process
```

* Kill multiple `ssh-agent` processes.

```text
$ ps aux | grep 'ssh-agent' | awk '{print $2}' | xargs kill -9
```

#### **Source**

* [https://www.tecmint.com/linux-process-management/](https://www.tecmint.com/linux-process-management/)

