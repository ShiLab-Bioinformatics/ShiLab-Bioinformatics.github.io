__This document provides instructions for using the microbiology software tools and databases installed in the M3 computer cluster.__

1.Create a new M3 account
----------------------
Every user of the mirobiology tools and databases in the M3 computer cluster needs their own M3 account. You can create an M3 account using this website:
  [Create an M3 account](https://hpc.erc.monash.edu.au/karaage/aafbootstrap). 
You need to login using your Monash account.

More details are provided on [the M3 users manual](https://docs.massive.org.au/M3/requesting-an-account.html).

2.Create a new M3 project
----------------------
After creating your M3 user account, you need to create a new project for running analyses. Please use [this Google Form](https://docs.google.com/forms/u/2/d/e/1FAIpQLSefDLmIesBaZ_90efzKQytg-2V5mBbSMfM0uW8MiCrgw3QMJg/viewform) for creating an application for creating the project. The "Apply for Project" link in the HPC ID system (https://hpc.erc.monash.edu.au/karaage/) **cannot** be used for applying for new projects in M3.

You should to indicate in the project description that this project is for using the software tools and databases in the _ws32_ project, which is run by Prof Wei Shi and Yang Liao. If you would like to let Yang Liao to assist you to maintain the data and manage the tasks, you can also indicate that you want to have Yang as a member of this new project.

![image](https://github.com/user-attachments/assets/c8fdaea4-600c-41e2-8b2b-2b00485c67b6)



3.Joining the ws32 project
----------------------
You need to join the ws32 project for using the software tools and databases. But you can only join this project after your new M3 project was successfully created, otherwise your default project will be set to ws32, which does not have any CPU hour allowence. You can join ws32 in the _Join existing projects_ link on [the homepage of the HPC ID system](https://hpc.erc.monash.edu.au/karaage/).

![image](https://github.com/user-attachments/assets/94d9a7dd-f01f-4a72-bc55-7361c417d0a3)

Then you can search for the ws32 project.

![image](https://github.com/user-attachments/assets/436caa09-b6ec-402c-a3e3-f7259053f17e)

On the next page, you can select the ws32 project and submit your application for joining it. This application will be reviewed by Wei and Yang ASAP. 

4.Connect to the M3 cluster
-----------------------
The software tools are provided in the Command-Line Interface (CLI). There are a few ways you can use to access the CLI of the M3 cluster. 

### 4.1.Using the terminal service on the M3 Desktop website
Virtual terminals can be created on the [M3 Desktop website](https://m3-desktop.erc.monash.edu/), so that to access the M3 cluster.

![image](https://github.com/user-attachments/assets/c4a53789-23a0-4ffe-8792-143d93add686)

![image](https://github.com/user-attachments/assets/093137d3-5062-4b16-bec5-3f937fd18e08)


### 4.2.Using the desktop service on the M3 Desktop website
Virtual desktops can be created on the [M3 Desktop website](https://m3-desktop.erc.monash.edu/). The terminal app in the virtual desktop gives access to the M3 cluster.

![image](https://github.com/user-attachments/assets/5bb174ec-b0bf-4886-9862-8f709c9e8d27)

![image](https://github.com/user-attachments/assets/7de90c13-66a3-4830-9bff-aa927897d730)


### 4.3.SSH to the M3 login computer
You can SSH to the M3 login computer from a macOS, Windows or Linux computer. 
```
ssh username@m3-login3.massive.org.au
```
If you use a Windows 10 or Windows 11 computer, the SSH command should have been inbuilt in Windows. This command is inbuilt in macOS and (virtually all) Linux.

5. Use a software tool or a database
   -----------------------------
If you have done all steps above, you will have two _symbolic links_ in your home directory:
```ws32``` and ```ws32_scratch2```. To setup your environment for running software tools, you need to execute a shell script using the ```source``` command:
```
source ~/ws32_scratch2/Shared/welcome.bash
```


