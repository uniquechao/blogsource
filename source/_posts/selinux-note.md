title: selinux_note
date: 2015-11-24 11:26:44
tags: 
- linux
- selinux
categories:
- notes
  
---
## 1 Introduction
Security-Enhanced Linux (SELinux) is a mandatory access control (MAC) security mechanism implemented in the kernel. SELinux was first introduced in CentOS 4 and significantly enhanced in later CentOS releases. These enhancements mean that content varies as to how to approach SELinux over time to solve problems.
### 1.1. Some of the Problems
 In order to better understand why SELinux is important and what it can do for you, it is easiest to look at some examples. Without SELinux enabled, only traditional discretionary access control (DAC) methods such as file permissions or access control lists (ACLs) are used to control the file access of users. Users and programs alike are allowed to grant insecure file permissions to others or, conversely, to gain access to parts of the system that should not otherwise be necessary for normal operation.


![头像](http://i.imgur.com/Kb6JpJt.jpg)