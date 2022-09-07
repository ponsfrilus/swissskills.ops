# Swiss Skills VM

This project deploys all the necessary software and configurations to an
Ubuntu virtual machine. The final objective is to distribute this VM to all
students that want to train for the Swiss Skills "Trade 17 - Web Technologies"
challenge.

The project uses [Ansible] but you won't need anything but `git` and `curl` to
begin with. The Ansible script uses a "suitcase" that installs everything you
need (read more at [ansible.suitcase]).

The official "competitor-vm-ubuntu" is available here: https://github.com/skills17/competitor-vm-ubuntu.


## TL;DR

In order to use the script, you can either
  a) clone this repository on the VM directly and run `./skillsible --local`, or
  b) edit the [inventory.yml], install `openssh-server` on the VM and run `./skillsible`.


## Prepare the VM

As the plan is to distribute the configured VM to sudents, [VirtualBox] has been
choosen. However it should be pretty easy to use the very same script on real
PCs (i.e. remove the Guest Additions tasks).

To create the VM:
  1. Donwload [Ubuntu] 22.04 LTS
  2. Install [VirtualBox]
  3. Create the new Virtual Machine
  4. Mount the Ubuntu ISO and start on it
  5. Install Ubuntu the minimal way creating the administrator/administrator user
  6. Install `sudo apt install git curl openssh-server`
  7. Setup the port forwarding (3022 → 22) (see [developertharun] documentation)
  8. Choose a) or b) in the TL;DR §


[Ansible]: https://www.ansible.com/
[ansible.suitcase]: https://github.com/epfl-si/ansible.suitcase
[Ubuntu]: https://ubuntu.com/download/desktop/thank-you?version=22.04.1&architecture=amd64
[VirtualBox]: https://www.virtualbox.org/wiki/Downloads
[developertharun]: https://dev.to/developertharun/easy-way-to-ssh-into-virtualbox-machine-any-os-just-x-steps-5d9i
