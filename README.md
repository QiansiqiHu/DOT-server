# CUHK Business School DOT-Server

[[**To Create an Account**](https://docs.google.com/forms/d/e/1FAIpQLSeT2iQ311o1I-IW_9hPJ3kP0iEuOM8kqR8Lfs-KphaNBxeGvQ/viewform?usp=sf_link)] [[**To Report an Issue**](https://docs.google.com/forms/d/e/1FAIpQLSfEhb-JFyDJY4YJZTm_8JhlqI9xnspSksopMaF1Cem5TAclyw/viewform?usp=sf_link)]

This repository provides an overview of servers in the Department of Decisions, Operations and Technology, CUHK Business School, including two GPU servers (IP addresses: 137.189.75.114 and 137.189.75.115) and one Storage server (ID address: 137.189.75.113). Guidelines on how to use these servers are also introduced.

**IMPORTANT: During the pilot run, we will only open 137.189.75.115 to new users. In principle, the base environments of the users are independent from each other, and hence you can install libraries according to your own needs. If you find any problems regarding the management of libraries and packages, please contact the administrator via [this link](https://docs.google.com/forms/d/e/1FAIpQLSfEhb-JFyDJY4YJZTm_8JhlqI9xnspSksopMaF1Cem5TAclyw/viewform?usp=sf_link), where users can report issues/submit your customized requests regarding server functions.**

## Configuration

#### GPU Servers (137.189.75.114 & 137.189.75.115)
These two servers are equipped with graphics cards (NVidia 4049). You may use them for computational experiments. Below is the summary of these two servers. They are identical in configuration.

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

We have provided users with a convenient way of accessing the server through web browsers. They can log in and utilize JupyterHub for computational experiments in Python and R. If you need to use some other softwares (e.g., Stata or MatLab), please submit your request via [this link](https://docs.google.com/forms/d/e/1FAIpQLSfEhb-JFyDJY4YJZTm_8JhlqI9xnspSksopMaF1Cem5TAclyw/viewform?usp=sf_link). 

**Please make sure that the internet cable (in CYT) is available at your workplace OR that you have connected onto the [CUHK VPN service](https://www.itsc.cuhk.edu.hk/all-it/wifi-and-network/cuhk-vpn/). Otherwise, you will NOT be able to connect to the server for safety reasons.** 

After the network environment is correctly set, please follow the steps below to connect to the server.

1. First, input `137.189.75.115` on your web server, and you will be guided to the following page:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/login.png)

2. Then input the username and password that you have received from the email sent by the server administrator, and you will be guided to the JupyterLab interface. Below is an example:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/jupyterlab.png)

3. For security reasons, you can reset the password of your jupyter account by opening the terminal located at the bottom of the interface and then executing the following command:
```
passwd
```
Then the terminal will guide you to reset your password. Later you will only be able to log in with the new password.

4. `R` has also been installed on server. You can access R kernels by running the following command in terminal.

```
R                               ## start R programming

IRkernel::installspec()         ## install R kernel
```

Quit R with `q()` and initiate a new launcher, you will find that the R kernel is available:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/R_kernel.png)

5. With everything prepared, now you can start coding with GPU on the server! More details regarding the Python environment can be find here. For more advanced operations using **ssh**, a [tutorial](https://github.com/QiansiqiHu/DOT-server/blob/main/SSH_instructions.pdf) is provided for your reference. If you want to upload your data to the server, you can use the `scp` command or tools like WinSCP.
