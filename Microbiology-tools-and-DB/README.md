# Guide to Using Microbiology Software and Databases on the M3 Cluster

1.About this document
----------------------
This document provides instructions for using the microbiology software tools and databases installed on the M3 computer cluster. You need to create an M3 account, apply for your own M3 project, then you can connect to the M3 cluster and run your analyses using software tools and databases on it. The steps are detailed in sections below.

2.Create a new M3 account
----------------------
Every user of the microbiology tools and databases on the M3 computer cluster needs their own M3 account. You can create an M3 account using this website:
  [Create an M3 account](https://hpc.erc.monash.edu.au/karaage/aafbootstrap). 
You need to login using your Monash account before you can create an M3 account on this webpage.

You will be required to select a username in the M3 computer and create a password for it. You need to keep this info for connecting to M3 by ```SSH```.

More details are provided on [the M3 users manual](https://docs.massive.org.au/M3/requesting-an-account.html).

3.Create a new M3 project
----------------------
After creating your M3 user account, you need to create a new project for running analyses. Please use [this Google Form](https://docs.google.com/forms/u/2/d/e/1FAIpQLSefDLmIesBaZ_90efzKQytg-2V5mBbSMfM0uW8MiCrgw3QMJg/viewform) for creating an application for creating the project. The "Apply for Project" link in the HPC ID system (https://hpc.erc.monash.edu.au/karaage/) **cannot** be used for applying for new projects in M3.

You need to indicate in the project description that this project is for using the software tools and databases in the ```ws32``` project, which is run by Prof Wei Shi and Yang Liao. If you would like to let Yang to assist for maintaining the data and managing the tasks, you can also indicate that you want to have Yang as a member of this new project. You can also specify the disk space that you need for storing your data. The space by default is 500GB for the primary data and 500GB for temporary files that are created while running your analysis.
![Create a new M3 project](https://github.com/user-attachments/assets/c8fdaea4-600c-41e2-8b2b-2b00485c67b6)

Once your application is submitted, the eResearch team will review your application and give feedback. This is usually done in a few days.

4.Joining the ws32 project
----------------------
You need to join the ```ws32``` project for using the software tools and databases. But you can only join this project __after__ your new M3 project is successfully created, otherwise your default project will be set to ```ws32```, which does not provide any CPU hour allowance. You can join ```ws32``` in the _Join existing projects_ link on [the homepage of the HPC ID system](https://hpc.erc.monash.edu.au/karaage/).
![image](https://github.com/user-attachments/assets/94d9a7dd-f01f-4a72-bc55-7361c417d0a3)

Then you can search for the ```ws32``` project.

![image](https://github.com/user-attachments/assets/436caa09-b6ec-402c-a3e3-f7259053f17e)

On the next page, you can select the ```ws32``` project and submit your application for joining it. This application will be reviewed by Wei and Yang ASAP. 

5.Connect to the M3 cluster
-----------------------
The software tools are provided in the Command-Line Interface (CLI). There are a few ways you can use to access the CLI of the M3 cluster. 

### 5.1.Using the terminal service on the M3 Desktop website
Virtual terminals can be created on the [M3 Desktop website](https://m3-desktop.erc.monash.edu/), so that to access the M3 cluster. You need to first click "Launch" as in the figure below. After a terminal is created, you can then click "connect".
![image](https://github.com/user-attachments/assets/9b7eab45-de1a-406e-8a57-fea84e952703)

### 5.2.Using the desktop service on the M3 Desktop website
Virtual desktops can be created on the [M3 Desktop website](https://m3-desktop.erc.monash.edu/). The terminal app in the virtual desktop gives access to the M3 cluster. You need to first click "Launch" as in the figure below. After a virtual desktop is created, you can then click "connect" to start a CLI. 
![image](https://github.com/user-attachments/assets/5bb174ec-b0bf-4886-9862-8f709c9e8d27)

After connected to the virtual desktop, you can then run the terminal app to start a CLI.
![image](https://github.com/user-attachments/assets/7de90c13-66a3-4830-9bff-aa927897d730)

### 5.3.SSH to the M3 login computer
You can SSH to the M3 login computer from a macOS, Windows or Linux computer to start a CLI. You need to use the username and password that were created in Section 2.
```
ssh username@m3-login3.massive.org.au
```
If you use a Windows 10 or Windows 11 computer, the ```SSH``` command should have been inbuilt in Windows. This command is also inbuilt in macOS and virtually all Linux distributions.

6.Use a software tool or a database
-----------------------------
If you have done all steps above, you will have two _symbolic links_ in your home directory:
```ws32``` and ```ws32_scratch2```. To setup your environment for running software tools, you need to execute a shell script using the ```source``` command:
```
source ~/ws32_scratch2/Shared/welcome.bash
```

For using the installed tools, you can find examples in ```~/ws32_scratch2/Shared/Examples```:

```
cd ~/ws32_scratch2/Shared/Examples
ls -l
```

You can also find the databases in ```~/ws32_scratch2/Shared/Database```:

```
cd ~/ws32_scratch2/Shared/Database
ls -l
```


7.Use the computational resources in M3
-----------------------------
Many analyses are hungry to computational resources. That is to say, they need large amounts of memory, many CPUs and/or GPUs. You need to send jobs to the SLURM task management system to utilise the large amounts of resources in M3 for running these analyses. The manual can be found in [M3 SLURM users manual](https://docs.massive.org.au/M3/slurm/slurm-overview.html).

8.Seek for help
-----------------------------
If you have had some questions or need help, please feel free to send an Email to [Yang Liao](mailto:yang.liao@monash.edu).
