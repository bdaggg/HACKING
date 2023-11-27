# kevgir

In this project I will solve the machine named 'kevgir'. first I scan the open ports on the machine and find the open ports 


![openport](https://github.com/bdaggg/kevgir/assets/110742864/8cbe0bc3-dd03-4afe-a2a5-a366d5d91d40)





I then do a detailed scan of the services used on open ports on the machine to find version information. 


![detailscan](https://github.com/bdaggg/kevgir/assets/110742864/6d047900-cdc1-4d9c-a2af-49eb3ca171d8)





I noticed that the Apache tomcat service is used on port 8080. when I looked at the service from the browser, I thought that I might be able to infiltrate the system from here.
After some research, I realized that I can log in to the service with a username and password. and I decided to see if I could access the username and password information with a brute force attack. 
Searching the Metsploit database, I found a brute force attack tool built for this process. 


![1](https://github.com/bdaggg/kevgir/assets/110742864/6bcfa2c3-6358-44bb-8265-70ba89c00521)





I selected the tool and made the necessary adjustments. 


![2](https://github.com/bdaggg/kevgir/assets/110742864/98c907cd-b736-42a9-bc42-3975eb540f32)





I said everything is fine and I started the tool and the tool found the username and password for me. username is tomcat and password is tomcat. this is actually the default username and password


![3](https://github.com/bdaggg/kevgir/assets/110742864/58e204de-6df1-468d-bf4a-1857424285c6)





I was able to log in to the tomcat service using the username and password.


![4](https://github.com/bdaggg/kevgir/assets/110742864/260d6cc1-4d3e-4f4d-b32e-aac84bf5501c)





I think I have an idea of what to do next. now that I am logged into the apache service, if I can get a meterpreter shell from the system and run it, I will be logged into the system from my terminal. i can use the msfvenom tool or I can use a tool in the metasploit database that does this for apache. i decided to use a tool in the metasploit database.


![5](https://github.com/bdaggg/kevgir/assets/110742864/2edc061b-9c11-4421-91b6-101594f5e9c2)





I have selected the tool that can perform this operation and set the necessary options


![6](https://github.com/bdaggg/kevgir/assets/110742864/db46178c-d007-4f5c-ba1a-5a9052c6d55e)





After starting the tool I was able to get the meterpreter shell


![7](https://github.com/bdaggg/kevgir/assets/110742864/35cafdfb-2439-4638-924f-09ecb8b83bdd)





I managed to infiltrate the system and was able to navigate through the files. 


![8](https://github.com/bdaggg/kevgir/assets/110742864/93081ef7-ee4f-467f-8ffb-6a39bf620645)




There may be other ways to infiltrate the system, I infiltrated the system by acting on the first method that came to my mind. by investigating in detail, the system can be entered in other ways.
