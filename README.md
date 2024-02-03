# WEB-SETUP-WITH-BASH-SCRIPTING

### USING BASH SCRIPTING TO PUSH A WEBSITE SETUP SCRIPT TO THREE VAGRANT VIRTUAL MACHINES

<hr>

#### STEPS

- Create a Vagrantfile and launch 3 vagrant VM's with the name [mainsvr, web01, web02, web03]
- SSH into the mainsvr vm and set the hostname to "mainsvr"
- SSH into the web01 vm and set the hostname to "web01"
- SSH into the web02 vm and set the hostname to "web02"
- SSH into the web03 vm and set the hostname to "web03"
- Map the IP Addresses and the hostname of all the VM's in the mainsvr vm's etc/hosts file so that the mainsvr can refer to other machines by their IP addresses when it wants to ping them.
  ```
  192.168.10.13 web01
  192.168.10.14 web02
  192.168.10.15 web03
  ```
- Login to the web01, web02 and web03 machine and create a user **devops** and add this user into the visudo file

- Set up key based login method so that the mainsvr vm's can login to other machine using an ssh key. This can be done in the by first generating an ssh key in the mainsvr vm's and copying the key to other vm's.

  ```
  // The below command will run the action
  👇
  ssh-keygen
  ssh-copy-id devops@web01
  ssh-copy-id devops@web02
  ssh-copy-id devops@web03
  ```

- Test this by login into the web01 from the mainsvr vm's by running the command "ssh sevops@web01" and it should be successful.

- Create an empty file and store all the hostname in it.
- Create "website_setup.sh" script that will be used to setup a websites in eash of the 3 VM's.
- Create another script "web_push.sh" that will push the "website_setup.sh" script to the vm's to each remote for execution.

- Run the "web_push.sh" in the mainsvr vm's for execution.

GoodLuck 👍
