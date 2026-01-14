- Below is the nodejs application we are going to deploy on aws

[git-repo](https://github.com/verma-kunal/AWS-Session)

# Testing locally

- first step is to clone the git repo using **git clone** command.
  
- env variables
<img width="787" height="425" alt="image" src="https://github.com/user-attachments/assets/4846727d-8cae-49e2-81cb-00294d65c626" />

- npm is for nodejs, pip is for python
- below is the vscode ui, once we run **npm install** we can see node modules. it is necesary for the application and additional module needed in future as well

<img width="1172" height="488" alt="image" src="https://github.com/user-attachments/assets/fe4b2345-f28c-4d25-8243-ec3b7eda88ee" />
<img width="818" height="461" alt="image" src="https://github.com/user-attachments/assets/e00670f8-af97-43b2-840e-2aef896839f9" />

- Now run the app ```npm run start```

<img width="900" height="265" alt="image" src="https://github.com/user-attachments/assets/e4bce483-a012-44c8-94c6-7453e1e7426c" />

- now we can see app is running fine locally

<img width="1471" height="851" alt="image" src="https://github.com/user-attachments/assets/62e66b10-0161-4a4f-b612-2222328cee08" />

---

# In AWS

1. IAM user creation
2. EC2 creation
3. Follow the steps in git repo and run the application

## Create IAM user

- add user

<img width="1496" height="430" alt="image" src="https://github.com/user-attachments/assets/4d026ec0-735a-439b-b387-02d7913e977d" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cdbfe879-a81c-4eaa-b757-961f488b2cef" />

- set a custom password

<img width="1466" height="733" alt="image" src="https://github.com/user-attachments/assets/bdb5daad-6fde-48d8-8437-04314019a6ba" />

- set permissions ( attach policies directly )

<img width="1529" height="510" alt="image" src="https://github.com/user-attachments/assets/7ed4100b-529e-436d-bda7-1d25374ee674" />

- here we provided admin privileges, then click next

<img width="1067" height="269" alt="image" src="https://github.com/user-attachments/assets/4d172a75-0e9b-4ae7-a69f-77e88e7ac81f" />

- Review and create

<img width="1446" height="768" alt="image" src="https://github.com/user-attachments/assets/2bc45a76-37bb-4151-8454-9457e7465c13" />
<img width="1403" height="609" alt="image" src="https://github.com/user-attachments/assets/6e37334d-966b-4da9-8252-3c83540aece9" />
<img width="1460" height="808" alt="image" src="https://github.com/user-attachments/assets/888ad958-639c-466e-992a-5a953501a3a6" />
<img width="1480" height="669" alt="image" src="https://github.com/user-attachments/assets/d8eeb570-535d-4798-9f84-a4fc3487e7f3" />
<img width="1105" height="590" alt="image" src="https://github.com/user-attachments/assets/bd3f4d11-5494-491e-b229-9417e6b7db76" />
<img width="1475" height="352" alt="image" src="https://github.com/user-attachments/assets/333cf59a-e191-49b4-a2eb-d17d9d7e37af" />

---

## Create EC2

- give the name

<img width="1049" height="224" alt="image" src="https://github.com/user-attachments/assets/24a2296e-74f7-4185-8476-5cea403e9cbd" />

- we are going with ubuntu image

<img width="1087" height="443" alt="image" src="https://github.com/user-attachments/assets/f731292d-17a7-4d97-adbd-d16a77ff1e04" />

- we are selection ```t2.micro``` instance type

<img width="1204" height="486" alt="image" src="https://github.com/user-attachments/assets/fa624ff0-33e4-4749-82a6-3c2526d66382" />

- here we r creating a new key pair

<img width="1073" height="265" alt="image" src="https://github.com/user-attachments/assets/465df2d6-eb18-40a0-9768-b6c53c5e0d54" />

- netowrking settings, allow ssh thats enough

<img width="1230" height="638" alt="image" src="https://github.com/user-attachments/assets/9f7a0b1a-6115-4397-9a4f-97f1911dfb57" />

- configure storage

<img width="1329" height="573" alt="image" src="https://github.com/user-attachments/assets/24e123c6-0218-46fc-a9b4-cca1eb8656df" />

- EC2 instance is created, we can login now

<img width="1251" height="700" alt="image" src="https://github.com/user-attachments/assets/4ad6d0dd-2f63-4dc3-a430-802270075c0d" />

---

- Follow the steps in github repo and run the application

<img width="893" height="472" alt="image" src="https://github.com/user-attachments/assets/f7b8ca86-af0d-4696-ad47-e81993ca9782" />

- once we try to access by using public ip **(public-ip:3000)**, then site won't reachable
- so we need to expose port 3000 to the internet
- go to SG and edit the inbound rules and save it

<img width="1401" height="728" alt="image" src="https://github.com/user-attachments/assets/8f9b1ef4-0e78-46d2-a4c8-c2834bc46e84" />
<img width="1377" height="656" alt="image" src="https://github.com/user-attachments/assets/ffe1c40b-243e-4d04-a514-fd4ca5fc84b3" />

- launched the app

<img width="1476" height="553" alt="image" src="https://github.com/user-attachments/assets/9a09ce85-98d4-4cb3-9c8e-d8bc1f0bb3c9" />

