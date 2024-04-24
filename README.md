# intel_mlops
Intel MLOps Certification
Course Link - https://learning.intel.com/Developer/pages/133/mlops-professional

Certification Link - https://home.pearsonvue.com/Clients/Intel.aspx


**Intel® Developer Cloud for this Course:**
Visit cloud.intel.com and create a Standard Tier account.
Once your account is created, navigate to the Intel® Developer Cloud homepage.
Refer back to the MLOps Professional Study Guide section called “Getting Started with the MLOps Professional Training Package” and click the link labeled “Access Code for Intel® Developer Cloud” to access your complimentary cloud coupon code. 
To redeem your complimentary cloud coupon, expand the user drop-down on the upper right and select “Cloud Credits.”

4th Generation Intel® Xeon® Scalable Processor VMs
Instance Type: Small VM 8 cores, 16 GB memory, and 20 GB disk
Machine Image: ubuntu-2204-jammy-v20230122

For all labs requiring 4th Generation Intel® Xeon® Scalable Processor VMs, you will be expected to download and install miniconda. To achieve this run the following commands.

>> wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

>> bash https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

>> source ~/.bashrc

****Generate SSH key for cloud account **
**Select your OS:
 Windows
Launch a new PowerShell window on your local system.
Optional: if you haven't generated a key before, create an .ssh directory.
mkdir $env:UserProfile\.ssh

Copy & paste the following to your terminal to generate SSH Keys.
ssh-keygen -t rsa -b 4096 -f $env:UserProfile\.ssh\id_rsa

If you are prompted to overwrite, select No.
Copy & paste the following to your Powershell window to view your SSH key:
cat $env:UserProfile\.ssh\id_rsa.pub

Paste your key's contents in the field below.

**To access your instance with an SSH client:**
Open an SSH client
Locate your public key file (my-key.ssh). The wizard automatically detects the key you used to launch the instance.
Your key must not be publicly visible for SSH to work. Use this command:
chmod 400 my-key.ssh

SSH command to connect to instance
ssh -J guest@146.152.232.8 ubuntu@100.82.223.198

Please note that in most cases the username above will be correct, however please ensure that you read your instance usage instructions to ensure that the instance owner has not changed the default instance username.


--------------------------
Install/Open VS Code
Install extension - Remote - SSH
After installation press Fn+F1 and type remote ssh --> select  Add a new host --> Enter ssh connection from intel compute instance ---> select first option with user folder location---> click on connect in popup --At the right bottom you can see ssh connected--->> click on that
In VS Code click on Remote Explorer, you will see the SSH there click on it.
Click on Open File at centre of your screen ---> you will see /home/ubuntu/

**Configuring VSCode**
On your local machine, open VSCode.

If not installed, click on the extension icon in the sidebar and search for Remote - SSH. Install it.

Press F1 and type in Remote - SSH: Add New SSH Host. Choose it from the dropdown.

Return to the IDC instance and click How to Connect. This will provide the necessary SSH connection command.

Paste the SSH command into VSCode's connection prompt. Choose an SSH config file to update (the first option usually works).

In the appearing pop-up, click Connect.

Select Linux when asked for the remote host platform.

If you have an SSH Key password, enter it twice. If not, simply hit continue twice.

Once you complete these steps, You should now have VSCode operating on the IDC remote host.

**VSCode Remote Folder Access**
In VSCode, go to the file explorer on the left and click Open Folder.

Allow the opening of a folder on the remote host by choosing default options.

You should now have VSCode operating on the Intel Developer Cloud remote host.

Cloning the Course Repository
In the terminal, run: git clone https://github.com/intel/certified-developer

Use the file tree to peruse the repository, modify files, or execute scripts.

A terminal can be opened within VSCode to run scripts.

Some course materials utilize VSCode's port forwarding for prototypes and front-end runs on your local browser.


![image](https://github.com/sumitsaxena-git/intel_mlops/assets/58607740/21b9ad3a-3dc2-4df2-9fe9-06f49ed66053)

