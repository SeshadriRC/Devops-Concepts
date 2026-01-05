<img width="1021" height="551" alt="image" src="https://github.com/user-attachments/assets/4901f185-056e-47cf-a3e4-cedfb47cdf3c" />

**Server**
<img width="1100" height="691" alt="image" src="https://github.com/user-attachments/assets/51fdbd4f-77af-4183-9397-c2612800ddcc" />

- Here server has more Capacity 50Gb ram , 50 CPU's but app needs only 5gb ram and 5 cpu's so remaining resources going waste. so to address this issue we are using virtualization

**Virtualization**

<img width="808" height="402" alt="image" src="https://github.com/user-attachments/assets/a1f9420e-a252-4f69-a9a7-f612145a7f53" />

- Here we are taking one server and installing hypervisor on it. hypervisor is used to create VM's in Server. Nothing but a logical isolation
- Here we achieved efficiency using hypervisor
  <img width="1035" height="589" alt="image" src="https://github.com/user-attachments/assets/ed13e477-1123-4196-8b26-3cee08d5b8a2" />
- popular hypervisor are given in the above image
- VM has their own hardware, OS, memory, cpu. it won't depend on other vm's
- AWS will buy millions of servers and put them in a Datacenter. for eg: mumbai region. In all the physical servers hypervisors are installed.
- If in case user requested a VM then hypervisor will create a VM
    
<img width="1046" height="667" alt="image" src="https://github.com/user-attachments/assets/9eccc93b-b8a2-46f5-9558-c1550d0b9ead" />

  - AWS installed 100 physical servers on mumbai region, each server has 100 GB RAM , 100 GB of CPU
  - If user requested for 10GB Ram, 12 CPU then aws will choose the server which has those capacity and ask the hypervisor to create a VM and provide it.
