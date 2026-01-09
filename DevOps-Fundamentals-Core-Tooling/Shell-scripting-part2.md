
**Debug-node**

```
set -x
```

<img width="1193" height="571" alt="image" src="https://github.com/user-attachments/assets/057070c6-05ba-488e-8867-763112d7784c" />

<img width="1169" height="570" alt="image" src="https://github.com/user-attachments/assets/bb2648f6-9c44-4667-b24c-5c007fcd7edf" />

---

**To list out all the processes**

```
ps -ef
ps -ef | grep "amazon"
```

<img width="1917" height="435" alt="image" src="https://github.com/user-attachments/assets/9e1fec66-e4e8-453d-b584-926284ae4d4d" />


**pipe command**

<img width="953" height="294" alt="image" src="https://github.com/user-attachments/assets/48a9841f-6f8f-4526-9791-41087aae8c43" />


**stdin, stdout, stderr**   -> interview question

The video explains that in any system, there are different channels or log flows, specifically mentioning:

- STD in (Standard Input): The date command sends its output to STD in. The speaker notes that the pipe command (|) cannot receive information from STD in (24:45 - 25:57).
- STD out (Standard Output): Mentioned as another channel (24:52 - 24:56).
- STD error (Standard Error): Mentioned as another channel (24:52 - 24:56).

<img width="1071" height="553" alt="image" src="https://github.com/user-attachments/assets/a693ca8f-48bd-4b84-821b-692e7735aecb" />

---

**awk**

```
ps -ef | grep amazon | awk -F" " '{print $2}'
```
<img width="1907" height="884" alt="image" src="https://github.com/user-attachments/assets/a0f68b3e-23fc-4f38-ade7-6306c6ebc513" />

---
