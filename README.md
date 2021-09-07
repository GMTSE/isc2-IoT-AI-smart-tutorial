# Repository for ISC²'s Tutorial "AI for IoT and Smart Cities"

This repository contains the exercise and slides for the ISC² Tutorial entitled "AI for IoT and Smart Cities".

# Slides

[Session1](/Slides/Session1_slides.pdf "Slides for Session1")

[Session2](/Slides/Session2_slides.pdf "Slides for Session2")


# 1. Installation

## Option1 (recommended): Work directly with Python on your machine

### Preliminaries

You need python3.6+ installed.

### Optional

If you want to preserve your Python installation from any modification, you can work in a Virtual Environment:

- Install `venv` package for python. Example for Linux:
> `apt install python3-venv`
- Create a Virtual Environment (here the name is "isc2lab"):
> `python -m venv isc2lab`
- Activate this Virtual Environment:
> `cd isc2lab/ && . ./bin/activate`

Now all your work and package installations will occur inside this Virtual Env.

BEWARE: if you close your terminal, then you have to re-activate the Virtual Env. again (last step above).

### Install flower

>  `pip install flwr`

### Install TensorFlow

>  `pip install tensorflow`

### Optional

Clone or download the flower repository to get all the examples.

See: [Github repository](https://github.com/adap/flower "Github Flower")

## Option2: Work with the provided VirtualBox VM (if you do not have Python 3.6+ on your machine)

NOTE: Beware, this requires to download a 2.2 GB file (the Virtual Machine image). You need a good internet connection. 

[Download the virtual machine from here.](https://filesender.renater.fr/?s=download&token=ee500acd-b64e-43c0-99fb-b0a890ccfb15 "VM download link")

It is a Linux virtual machine and we have already installed python3.9, tensorflow and flower for you.
We used a compact virtual machine available from [iLabX](https://ilabxp.com/download-the-vlab/ "iLabX") of Technical University of Munich (TUM).
Then we installed the latter software on it.

You will need to use [Virtualbox software](https://www.virtualbox.org/ "VirtualBox") to run it. 
We have configured it to use 4 CPUs and 8GB of RAM. 

Please change the VM settings (on Virtualbox: settings-->system) according to the capabilities of your PC. More is better, 
but it should not exceed your PC's capabilties. 

Network settings are set to bridge mode. Sometimes NAT mode is better and you may change it. (on Virtualbox: settings-->network)

**When the VM runs, then please do not select factory reset!** as it will delete python3.9, tensorflow and flower.

After the VM is running on the right you can change keyboard settings by clicking on the keyboard icon (right and below).

# 2. Try Quickstart tensorflow example

i. Open 3 terminals

ii. go to the folder quickstart_tensorflow in all those 3 terminals
>  `cd flower-main/examples/quickstart_tensorflow/`

iii. On one terminal type (on VM we have python3.9, but please use your own version if you are not using the VM)
>  `python3.9 server.py`

iv. On 2 other terminals type 
>  `python3.9 client.py`

Now you will see that 2 clients connect to server and start Federated Learning.

# 3. Exercise: Playing with Federated Learning parameters

Go to the folder `examples/advanced_tensorflow` in the examples.

i. Change the number of clients to 3

ii. Change the number of rounds to 2

iii. How can we check the amount of data that is sent to server (i.e. How to get the network overhead)?

iv. Try to compare the performance/network overhead of different neural network models such as EfficientNetB0 with its version 2 and MobileNetv2
