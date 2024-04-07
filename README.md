# DOT-server
This repository provides an overview of servers in the department of Decisions, Operations and Technology, including 137.189.75.113, 137.189.75.114 and 137.189.75.115. Guidelines on how to use these servers are also introduced.

**IMPORTANT: During the pilot run, we will only open 137.189.75.115 to new users. For ease of management, non-administrator users should not use package management tools such as `pip`, `pip3`, and `conda`. If you are familiar with virtual enviroments, or have additional requirements regarding the versions of Python and R or the installation of libraries, please contact the administrator.**

## Configuration

#### 137.189.75.114 & 137.189.75.115
These two servers are equipped with graphics cards, and users will use them for experiments. Below is the list of components for the two servers. They are identical in configuration.

|Component| Description|
|---------|------------|
|Operating System       |Ubuntu 22.04.4 LTS|
|RAM                    |32GB DDR5-4800 ECC RDIMM [x16]|
|CPU|Intel® Xeon® Gold 5416S 30M Cache, 2.00 GHz (16C32T) [x2]|
|GPU|NVIDIA GeForce RTX 4090 24GB (CUDA 16,384 / Tensor 512) [x8]|
|Storage|Hard Disk Drive [18TB x8] on 137.189.75.113|

#### 137.189.75.113
This server is used for the storage of data. Users will never have to access this server, while their data will be automatically stored in its hard disks.

|Component| Description|
|---------|------------|
|Hard Disk Drive|18TB SAS 12Gb/s 7.2K rpm Seagate Enterprise [x8]|


## Access to the server
We have provided users with a very convenient way of accessing the server simply by using web browsers. They can log in and utilize JupyterHub for experiments related to Python and R. Meanwhile, please make sure that the **internet cable** is available at your workplace or that you can use the **CUHK VPN** service. Otherwise, you will not be able to connect to the server. 

After ensuring that the network environment is correct, please follow the steps below to connect to the server.

1. First, input `137.189.75.115` on your web server, and you will be guided to the following page:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/login.png)

2. Then input the username and password that you have received from the email, and you will be guided to the JupyterLab interface. Below is an example:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/jupyterlab.png)

3. For security reasons, you can reset the password of your jupyter account by opening the terminal located at the bottom of the interface and then executing the following command:
```
passwd
```
Then the terminal will guide you to reset your password. Later you will only be able to log in with the new password.
