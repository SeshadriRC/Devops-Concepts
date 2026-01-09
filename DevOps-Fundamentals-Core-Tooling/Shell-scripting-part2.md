
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

- The awk command is a powerful pattern scanning and processing language used in shell scripting to filter and manipulate data from the output of other commands or files (29:00). Unlike grep, which provides entire lines or statements, awk can extract specific columns or fields from the output (27:58).

```
ps -ef | grep amazon | awk -F" " '{print $2}'
```
<img width="1907" height="884" alt="image" src="https://github.com/user-attachments/assets/a0f68b3e-23fc-4f38-ade7-6306c6ebc513" />

<img width="1489" height="608" alt="image" src="https://github.com/user-attachments/assets/3525bf60-07ac-44cd-b228-901e9551cf5b" />

---

**set -e**

- This command ensures that your script will exit immediately if any command fails or exits with a non-zero status (which typically indicates an error) (33:03-33:08).

**set -o pipefail**

- This command is used in conjunction with set -e to handle errors within pipelines (commands connected by |). If any command in a pipeline fails (exits with a non-zero status), set -o pipefail ensures that the entire pipeline's exit status is non-zero, causing the script to exit if set -e is also active
  
- It is a common best practice to use both set -e and set -o pipefail at the beginning of your shell scripts (32:20-32:32). This provides robust error handling, ensuring that your script stops at the first sign of a failure, whether it's a standalone command or a command within a pipeline (37:45-37:50).

<img width="1198" height="651" alt="image" src="https://github.com/user-attachments/assets/16cf8fc1-447c-4db7-84bb-3e1879fd8b4e" />

---

**curl**

- retrieves the information from internet


```
curl -X GET googl.com
```

---

**wget**

<img width="1161" height="653" alt="image" src="https://github.com/user-attachments/assets/393b1848-1cc1-4c47-bc8f-6b015e5c8f8d" />


- curl will directly show the page, whereas wget will download the file from the internet. so thats the difference between wget and curl

---

**sudo**

```
sudo find / -name pam          / means root directory of linux system
```

<img width="811" height="312" alt="image" src="https://github.com/user-attachments/assets/e25e3314-bfee-49ee-bcdd-536f285a54e6" />


---

**if else**

- **fi** means we are closing the **if** condition

<img width="584" height="355" alt="image" src="https://github.com/user-attachments/assets/13087620-1df2-4072-ad77-482eaa35c1f5" />
<img width="888" height="417" alt="image" src="https://github.com/user-attachments/assets/b2f45ba9-fdbb-49c2-a510-b0b0d532edbd" />

---

**for loop**

- A for loop (1:06:00) is a control flow statement in shell scripting (and many other programming languages) that allows you to execute a block of commands repeatedly for each item in a list or sequence. It's used to automate repetitive tasks.

<img width="712" height="412" alt="image" src="https://github.com/user-attachments/assets/48aac9ad-c542-414f-86af-d201c72a04e9" />

- first it will execute the condition, it will perform the action, then it will go for incrementation and finally it will complete the for loop using done statement
