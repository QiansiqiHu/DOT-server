# CUHK Business School DOT-Server
This repository provides an overview of servers in the Department of Decisions, Operations and Technology, CUHK Business School, including 137.189.75.113, 137.189.75.114 and 137.189.75.115. Guidelines on how to use these servers are also introduced.

**IMPORTANT: During the pilot run, we will only open 137.189.75.115 to new users. In principle, base environments of users are independent from each other, and hence users can install libraries according to their own needs. If you find any problems regarding the management of libraries and packages, please contact the administrator.**

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

Users can apply for access to the server by filling out the [registration form](https://docs.google.com/forms/d/e/1FAIpQLSeT2iQ311o1I-IW_9hPJ3kP0iEuOM8kqR8Lfs-KphaNBxeGvQ/viewform?usp=sf_link).

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

4. `R` has also been installed on server. You can access R kernels by running the following command in terminal.

```
R                               ## start R programming

IRkernel::installspec()         ## install R kernel
```

Quit R with `q()` and initiate a new launcher, you will find that the R kernel is available:

![image](https://github.com/QiansiqiHu/DOT-server/blob/main/img/R_kernel.png)

5. With everything prepared, now you can start coding with GPU on the server! More details regarding the Python environment can be find here. For more advanced operations using **ssh**, a [tutorial](https://github.com/QiansiqiHu/DOT-server/blob/main/ssh_instructions.pdf) is provided for your reference. If you want to upload your data to the server, you can use the `scp` command or tools like WinSCP.
