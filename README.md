# isc2-IoT-AI-smart-tutorial
The exercise for the ISC2 Tutorial on IoT and AI for Smart Cities
# 1. Installation
i. If you have python3.6 and above (or you can install it) then you do not need to install the VM. 
You can directly install flower.

>  `pip install flwr`

>  `pip install tensorflow`

Clone the flower [Github repository](https://github.com/adap/flower "Github Flower")

ii. Skip this step if above worked. Otherwise if you have good internet connection to be able to download 2.2 GB Virtual Machine. 

Then please [download the virtual machine from here.](https://filesender.renater.fr/?s=download&token=ee500acd-b64e-43c0-99fb-b0a890ccfb15 "VM download link")

It is a Linux virtual machine and we have already installed python3.9, tensorflow and flower for you.
We used a compact virtual machine available from [iLabX](https://ilabxp.com/download-the-vlab/ "iLabX") of Technical University of Munich (TUM).
Then we installed the later software on it.

You will need to use [Virtualbox software](https://www.virtualbox.org/ "VirtualBox") to run it. 
We have configured it to use 4 CPUs and 8GB of RAM. 

Please change the VM settings (on Virtualbox: settings-->system) according to the capabilities of your PC. More is better, 
but it should not exceed your PC's capabilties.

<span style="color:red">*When the VM runs, then please do not select factory install!* <\span> as it will delete python3.6, tensorflow and flower.

After the VM is running on the right you can change keyboard settings by clicking on the keyboard icon (right and below).

# 2. Try Quickstart tensorflow example
i. Open 3 terminals

ii. go to the folder quickstart_tensorflow in all those 3 terminals
>  `cd flower-main/examples/quickstart_tensorflow/`

iii. On one terminal type (on VM we have python3.9, but please use your own version if you are not using the VM)
>  `python3.9 server.py`

iv. On 2 other terminals type 
>  `python3.9 client.py`

Now you will see that 2 clients connect to server and start federated learning.

# 3. Exercise: Playing with Federated learning parameters

Go to the folder advanced_tensorflow in the examples.

i. Change the number of clients to 3

ii. Change the number of rounds to 2

iii. Try to compare the performance of different neural network models such as EfficientNetB0 with its version 2 and MobileNetv2

iv. How can we check the amount of data that is sent to server? To know the network overhead?

