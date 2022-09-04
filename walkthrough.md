# walkthrough

1. Create a new development VM and setup SSH
   1. Using [VirtualBox](https://www.virtualbox.org/) and a [bridged adapter](https://www.virtualbox.org/manual/ch06.html#network_bridged)
   2. Runnning [Ubuntu Server 20.04 LTS](https://releases.ubuntu.com/20.04/)
2. Install [Ansible](https://docs.ansible.com/ansible/latest/getting_started/index.html) on the host machine
3. Setup SSH keys for the development VM. (`ssh-keygen`, `ssh-copy-id`, place key in `ssh/key.prv`)
4. Add the new VM to the Ansible inventory in `inventory.yaml` (IP address, ansible_user)
5. Verify that the new VM is reachable by running `ansible virtualmachines -m ping -i inventory.yaml`
