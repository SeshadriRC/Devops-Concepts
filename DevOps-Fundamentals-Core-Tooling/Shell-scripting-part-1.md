```
man ls
```

- vi and touch are creating files, but mostly touch command we will use for automation
```
vi 

touch - used for automations
```

- what is the purpose of #!/bin/bash

```
#!/  -> it is a shebang

```
- bash, ksh, sh, dash are executables
- one of the most widely used is **bash**

- The purpose of #!/bin/bash or #!/bin/sh (known as a shebang) at the beginning of a shell script is to inform the Linux kernel which interpreter should be used to execute the script (15:25-16:02).

Here's the difference between ksh, bash, and dash:

- Different Executables: These are different executables for shell scripts, each having its own syntax differences (17:41-19:13).
- Bash: Bash is one of the most widely used shells (19:20-19:26).
- Ksh (KornShell): Ksh has a different syntax for certain constructs, like for loops, compared to Bash. It is generally considered obsolete or less commonly used now (19:34-19:51).
- Sh (Bourne Shell): Historically, #!/bin/sh often redirected to #!/bin/bash due to a concept called linking in Linux. However, in some modern operating systems, sh might default to dash, which could cause issues if your script is written for Bash (20:12-24:09).

---

<img width="586" height="261" alt="image" src="https://github.com/user-attachments/assets/30e2f75c-b688-4e50-835f-3b6613fe1b47" />

```
:wq!
q!
cat
```

- how to execute this script
-  sh explicitly calls the sh interpreter, while ./ relies on the script's shebang to determine the correct interpreter.
```
sh <filename.sh>
./filename.sh
```

- how to grant permission

```
chmod
```

ch - change

<img width="1172" height="559" alt="image" src="https://github.com/user-attachments/assets/8356af86-4492-48df-b6be-11b029b5b8b0" />
