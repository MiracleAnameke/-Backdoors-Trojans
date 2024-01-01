# Backdoors & Trojans

## Introduction
This lab exercise involves understanding and utilizing backdoors and Trojans to gain unauthorized access to a computer system. You will use Tini as a backdoor program and mFileBinder as a wrapper program to create a backdoor Trojan horse. The lab is designed to provide insight into how backdoors and Trojans work and the potential vulnerabilities they exploit.

## Before You Begin
- Set up the Windows Server 2008 as the victim computer and Windows 7 as the hacker computer.
- Ensure both virtual machines are on the same subnet and have IP addresses assigned.
- Understand the importance of ethical hacking and ensure all activities are conducted in a controlled environment.

## Setting Up the Lab
1. **Assign IP Addresses**: Assign `10.81.10.1` to the hacker computer and `10.81.10.2` to the victim computer.
2. **Network Configuration**: Configure both computers' network adapters to Host-only.
3. **User Account Setup**: On the victim computer, create a user account with your FOL username and assign administrator privileges.

## Lab Procedure & Screenshots

### Exploit #1: Backdoor Access with Tini
- **Objective**: Gain backdoor access to the victim computer using Tini.
- **Execution**: Execute Tini on the victim computer and connect from the hacker computer using telnet.
- **Screenshot 1**: Take a screen capture showing the Task Manager window Processes tab (Tini & cmd.exe).
  
  <img src="https://i.imgur.com/sRw4lOu.png" height="400px" width="auto" alt="Task Manager with Tini and cmd.exe"/>

- **Screenshot 2**: Take a screen capture of the netstat command ensuring the process id (PID) is included.
  
  <img src="https://i.imgur.com/uaPlstk.png" height="400px" width="auto" alt="Netstat with PID"/>

### Exploit #2: Directory Listing via Backdoor
- **Objective**: Verify the backdoor connection and access to the victim's file system.
- **Execution**: Use the telnet connection to list the contents of the directory where Tini resides.
- **Screenshot 3**: Take a screen capture of the directory listing in the command prompt.
  
  <img src="https://i.imgur.com/B2rhM4c.png" height="400px" width="auto" alt="Directory Listing"/>

### Exploit #3: Verifying Connection
- **Objective**: Confirm that the backdoor connection has been established from the hacker's computer.
- **Execution**: Use the netstat command on the victim computer to verify an established connection.
- **Screenshot 4**: Take a screen capture of the netstat command ensuring the process id (PID) is included.
  
  <img src="https://i.imgur.com/8AwIjdH.png" height="400px" width="auto" alt="Netstat Verifying Connection"/>

### Exploit #4: Persistent Access via Startup
- **Objective**: Ensure persistent backdoor access by adding Tini to the startup menu.
- **Execution**: Copy Tini to the startup directory of the victim computer and restart.
- **Screenshot 5**: Take a screen capture of Task Manager showing your user name as the owner of tini.exe.
  
  <img src="https://i.imgur.com/MpNBaAg.png" height="400px" width="auto" alt="Task Manager with Tini at Startup"/>

### Exploit #5: Creating and Using a Trojan Horse
- **Objective**: Create and execute a Trojan horse combining Tini with a benign program.
- **Execution**: Use mFileBinder to bind Tini with felix.exe, run the bound file, and verify Tini is listening.
- **Screenshot 6**: Take a screen capture that shows the netstat –nao | find "7777" command output and also shows felix on the desktop.
  
  <img src="https://i.imgur.com/VYAArki.png" height="400px" width="auto" alt="Netstat and Felix Trojan"/>

## Conclusion
By completing this lab, you have explored the functionalities of backdoors and Trojans, gaining insights into their operation and potential vulnerabilities they exploit. Always remember the importance of using these skills within ethical and legal boundaries.
