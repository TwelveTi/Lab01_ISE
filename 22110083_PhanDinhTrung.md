# Lab #1,22110083, Phan Dinh Trung, INSE330380E_02FIE
# Task 1: Software buffer overflow attack
**Question 1**:
- Compile asm program and C program to executable code. 
- Conduct the attack so that when C executable code runs, shellcode will be triggered and a new entry is  added to the /etc/hosts file on your linux. 
  You are free to choose Code Injection or Environment Variable approach to do. 
- Write step-by-step explanation and clearly comment on instructions and screenshots that you have made to successfully accomplished the attack.
**Answer 1**: Must conform to below structure:

We will draw the stack frame of the c program to see how it works and also look for vulnerabilities in the code.


![image](https://github.com/user-attachments/assets/adfb3572-870d-40bc-81be-8fae40508913)

As the given c program, it does not check the length of the string to copy. So we can use to override and modify the return address so that it points to the location of the shellcode.asm file

The requirement of the post is to add 127.1.1.1 google.com to etc/hosts

![image](https://github.com/user-attachments/assets/fefdfa4e-9915-438b-ad48-db8304d365bc)

this is the initial state of etc/hosts.


