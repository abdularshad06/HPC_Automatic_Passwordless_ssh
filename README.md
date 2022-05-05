# HPC_Automatic_Passwordless_ssh
passwordless ssh on all compute nodes


- /etc/skel/.bash_profile

# ssh-keygen for newly created user for HPC

if [ ! -f ~/.ssh/authorized_keys ]
then
  ssh-keygen -t rsa -q -f "$HOME/.ssh/id_rsa" -N ""
  cp -r ~/.ssh/id_rsa.pub ~/.ssh/authorized_keys

fi
