# Useful Utilities & Commands

### Process Status  

* The ps utility displays a header line, followed by lines containing information about all of your processes that have controlling terminals. 

```text
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



