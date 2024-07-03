# CUHK Business School DOT-Server

[[**Create an Account**](https://docs.google.com/forms/d/e/1FAIpQLSeT2iQ311o1I-IW_9hPJ3kP0iEuOM8kqR8Lfs-KphaNBxeGvQ/viewform?usp=sf_link)] [[**Report an Issue**](https://docs.google.com/forms/d/e/1FAIpQLSfEhb-JFyDJY4YJZTm_8JhlqI9xnspSksopMaF1Cem5TAclyw/viewform?usp=sf_link)]

This repository provides an overview of servers in the Department of Decisions, Operations and Technology, CUHK Business School, including two GPU servers (IP addresses: 137.189.75.114 and 137.189.75.115) and one Storage server (IP address: 137.189.75.113). Guidelines on how to use these servers are also introduced.

**IMPORTANT: During the pilot run, we will only open 137.189.75.115 to new users. For now, only the faculty and PhD Students of the Department of Decisions, Operations and Technology are allowed to apply for an account. If you are a CUHK affiliate, please ask your collaborating faculty of the DOT department to apply for an account on your behalf.**

In principle, the base environments of the users are independent from each other, and hence you can install libraries according to your own needs. If you find any problems regarding the management of libraries and packages, please contact the administrator via [this link](https://docs.google.com/forms/d/e/1FAIpQLSfEhb-JFyDJY4YJZTm_8JhlqI9xnspSksopMaF1Cem5TAclyw/viewform?usp=sf_link), where users can report issues/submit your customized requests regarding server functions. We will also update a [document](https://github.com/QiansiqiHu/DOT-server/blob/main/Jupyter_env.pdf) to keep track of installation-related issues and their corresponding solutions.

### Recent Updates:
Now the previously registered users can run Stata programs on JupyterHub. A detailed guidance is provided [here](https://github.com/QiansiqiHu/DOT-server/blob/main/Stata_guide.pdf). Please note that the network license only supports 5 users, so the first five applicants can have access to Stata. For those who have not yet registered but wish to use Stata, please fill out the form through [this link](https://docs.google.com/forms/d/e/1FAIpQLSfEhb-JFyDJY4YJZTm_8JhlqI9xnspSksopMaF1Cem5TAclyw/viewform?usp=sf_link) and state your need for Stata. When the demand reaches a certain number, we will consider upgrading the license. 

## Configuration

#### GPU Servers (137.189.75.114 & 137.189.75.115)
These two servers are equipped with graphics cards (NVIDIA 4090). You may use them for computational experiments. Below is the summary of these two servers. They are identical in configuration.

|Component| Description|
|---------|------------|
|Operating System       |Ubuntu 22.04.4 LTS|
|RAM                    |32GB DDR5-4800 ECC RDIMM [x16]|
|CPU|Intel® Xeon® Gold 5416S 30M Cache, 2.00 GHz (16C32T) [x2]|
|GPU|NVIDIA GeForce RTX 4090 24GB (CUDA 16,384 / Tensor 512) [x8]|
|Storage|Hard Disk Drive [18TB x8] on 137.189.75.113|

#### Storage Server (137.189.75.113)
This server is used for data storage. You will NOT have direct access to this server, but your data will be automatically stored in its hard disks.

|Component| Description|
|---------|------------|
|Hard Disk Drive|18TB SAS 12Gb/s 7.2K rpm Seagate Enterprise [x8]|


## Access to Server

You can apply for the access to the server by filling out this [**registration form**](https://docs.google.com/forms/d/e/1FAIpQLSeT2iQ311o1I-IW_9hPJ3kP0iEuOM8kqR8Lfs-KphaNBxeGvQ/viewform?usp=sf_link).

We have provided users with a convenient way of accessing the server through web browsers. They can log in and utilize JupyterHub for computational experiments in `Python` and `R`. If you need to use some other softwares (e.g., `Stata` or `MATLAB`), please submit your request via [this link](https://docs.google.com/forms/d/e/1FAIpQLSfEhb-JFyDJY4YJZTm_8JhlqI9xnspSksopMaF1Cem5TAclyw/viewform?usp=sf_link). 

**Please make sure that the internet cable (in CYT) is available at your workplace OR that you have connected onto the [CUHK VPN service](https://www.itsc.cuhk.edu.hk/all-it/wifi-and-network/cuhk-vpn/). Otherwise, you will NOT be able to connect to the server for safety reasons.** 

After the network environment is correctly set, please follow the steps below to connect to the server.

1. First, input `137.189.75.115` on your web server, and you will be guided to the following page:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/login.png)

2. Then input the username that you have received from the email sent by the server administrator, and **create a password by yourself**. (Please note that the password you create will be used for every future login, so you need to remember it). Click "Launch Server", then you will be guided to the JupyterLab interface. Below is an example:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/jupyter.png)

**IMPORTANT**: Please ensure that you have access to the folder named `yourusername-dot` (as marked in the screenshot above), and perform all experiments and data storage within it. This folder is mounted to remote hard disks, enabling users to enjoy ample storage space. 

3. `R` has also been installed on the servers. You can access `R` kernels by running the following command in terminal.

```
R                               ## start R programming

IRkernel::installspec()         ## install R kernel
```

Quit R with `q()` and initiate a new launcher, you will find that the R kernel is available:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/R_kernel.png)

4. With everything prepared, now you can start coding with GPU on the servers! 


For more advanced operations using **ssh**, a [tutorial](https://github.com/QiansiqiHu/DOT-server/blob/main/SSH_access.pdf) is provided for your reference. 

With regard to **data transmission**, 
* If you want to upload your own data to the server, you can simply drag files onto Jupyterhub. By **ssh**, you can use the `scp` command or tools like WinSCP to upload files.
* If you want to download data from the server to your local machine, on Jupyterhub you can simply right-click on the file and then select 'Download'. By **ssh**, you should use `scp` or tools like WinSCP.
* If you want to download data from web to the server, you may utilize `wget`, which is commonly used for file downloads in Linux systems.   

# Contact

If you have any additional questions about the DOT-Server of CUHK Business School, please contact us at dotserver@cuhk.edu.hk.

