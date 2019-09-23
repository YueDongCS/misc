# misc
various commands used in systems

## forward a port for remote ipython notebook
ssh -N -f -L localhost:8888:localhost:8889 ydong26@jp-gpu1.cs.mcgill.ca


RUN LAB SERVER GPU
ydong26@jc-9 ~ $ nvidia-smi
nvidia-smi: command not found
ydong26@jc-9 ~ $ ssh agent-server1
ssh: Could not resolve hostname agent-server1: Name or service not known
ydong26@jc-9 ~ $ ssh agent-server-1
The authenticity of host 'agent-server-1 (132.206.52.145)' can't be established.
ECDSA key fingerprint is SHA256:ecAN/Xs6OzpJuvifd3hSlrrU2yKOibPHhuX/PAA8224.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'agent-server-1,132.206.52.145' (ECDSA) to the list of known hosts.
ydong26@agent-server-1's password: 
Welcome to Ubuntu 16.04.2 LTS (GNU/Linux 4.4.0-47-generic x86_64)
There are 9 users logged in.

New to our distributed GNU/Linux system? Type 'less /var/docs/00_welcome.txt'.

[ydong26][agent-server-1][~] nvidia-smi
Wed Mar  8 09:58:23 2017       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 367.44                 Driver Version: 367.44                    |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  GeForce GTX TIT...  Off  | 0000:02:00.0     Off |                  N/A |
| 29%   69C    P2   101W / 250W |    220MiB / 12206MiB |     44%      Default |
+-------------------------------+----------------------+----------------------+
|   1  GeForce GTX TIT...  Off  | 0000:03:00.0     Off |                  N/A |
| 22%   32C    P8    15W / 250W |    867MiB / 12206MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+
|   2  GeForce GTX TIT...  Off  | 0000:82:00.0     Off |                  N/A |
| 32%   73C    P2   138W / 250W |    708MiB / 12206MiB |     50%      Default |
+-------------------------------+----------------------+----------------------+
|   3  GeForce GTX TIT...  Off  | 0000:83:00.0     Off |                  N/A |
| 22%   31C    P8    16W / 250W |      2MiB / 12206MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID  Type  Process name                               Usage      |
|=============================================================================|
|    0     13795    C   python                                         218MiB |
|    1       593    C   /home/2016/sbasu11/miniconda2/bin/python       729MiB |
|    1      7927    C   python                                         133MiB |
|    2      6292    C   python                                         845MiB |
+-----------------------------------------------------------------------------+
[ydong26][agent-server-1][~] THEANO_FLAGS='device=gpu1' python 
