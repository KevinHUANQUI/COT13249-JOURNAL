Week 1  Introduction to Linux, SSH and Basic Setup 
<img width="512" height="459" alt="image" src="https://github.com/user-attachments/assets/947800a1-ae3a-419b-93d5-d9faca605d79" />
<img width="367" height="353" alt="image" src="https://github.com/user-attachments/assets/6ab4b4c4-4774-4d9f-92b5-ce9ebf8768d8" />

This week I learned the basics of working with Linux systems, including using the terminal, creating files and folders, and connecting remotely using SSH. 
What I Did 
In this week, I followed practical steps to set up a Linux environment using Ubuntu and VirtualBox. I also learned how to connect to another machine using SSH through PuTTY. 
 
I practiced several commands such as: 
 
- mkdir → to create folders  
- cd → to navigate between directories  
- ls and ls -l → to list files and view permissions  
- touch → to create files  
- nano → to edit files  
- chmod +x → to make a file executable  
## My Understanding 
I learned that Linux is heavily command-line based, and most actions are performed using commands instead of a graphical interface. 
<img width="583" height="267" alt="image" src="https://github.com/user-attachments/assets/d683cdcb-f265-430e-9a9d-30c18ff065a5" />
<img width="602" height="300" alt="image" src="https://github.com/user-attachments/assets/1601f6fd-be27-4e99-935c-1e897ada76c3" />
In addition, I generated an SSH key and connected it to my GitHub account. I used the command: 
 
ssh-keygen -t ed25519 -C "my email" 
 
Then I added the public key to GitHub so I could authenticate securely when using Git. This allowed me to connect PuTTY with GitHub without needing a password every time. 
 <img width="560" height="368" alt="image" src="https://github.com/user-attachments/assets/f483691a-812a-4e4b-af3a-8cea4f4b976c" />
<img width="595" height="393" alt="image" src="https://github.com/user-attachments/assets/edce0a9f-2c13-40d1-a251-ac7a34863896" />

 Finally, I used FileZilla to transfer files between Windows and Linux by connecting through SSH. In this imagen I sent cv.doc from my windows machine to ubuntu  
 
My Understanding 
Linux is controlled mainly through commands.  
SSH allows secure remote access.  
FileZilla uses SFTP (over SSH) to transfer files securely between systems. 

 
Reflection 
 
The most difficult concept for me this week was understanding how public and private keys work in SSH. At first, I didn’t understand why there are two keys and how they connect. It was confusing because I thought both keys were used the same way. I fixed this by practicing the setup and realising that the public key is shared with GitHub, while the private key stays on my machine and must be kept secure. 
 
In terms of comparison, SSH key authentication is more secure than password-based login. Passwords are easier to use but less secure, while SSH keys are harder to set up but provide stronger protection. SSH keys are used in real systems where security is important, especially for servers and cloud environments. 
 
One possible attack is brute force on SSH passwords, where attackers try many password combinations. This attack does not work well if SSH keys are used instead of passwords. However, if the private key is leaked or stolen, an attacker could gain access. This means security depends on how well the private key is protected. 
 

## Difficulties 
At the beginning, I found it confusing to understand the command structure and remember all the commands. I also struggled with file permissions, especially understanding what "rwx" means and how chmod works. 

I found it hard to remember commands at first.  
I was also confused about file permissions and SSH key setup. 

Another issue I faced was connecting using SSH and making sure the service was running. I had to use commands like

References

Ubuntu Server 2026, Download Ubuntu Server, viewed 2 April 2026, https://ubuntu.com/download/server
Oracle VM VirtualBox 2026, Oracle VM VirtualBox, viewed 2 April 2026, https://www.virtualbox.org/
GitHub 2026, Generating a new SSH key and adding it to the SSH agent, viewed 2 April 2026, https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
