# Emergency IT kit (E-IT Kit) Virtual Machine

Virtual Machine with IT software and documentation for emergency situations.

It uses [Vagrant](https://www.vagrantup.com/) and [Ansible](https://www.ansible.com/)
to define a configuration for the virtual machine that can easily be executed using
a single command (given that you have the required dependencies installed):

```
vagrant up
```

This will fail after a while because some user files do not exist. You will
then need to do the following to continue:

- Open VirtualBox
- Right-click on the (now running) virtual machine
- Select "Show"
- Log in to Xubuntu with vagrant and vagrant.
- Then go back to the shell where you were running `vagrant up`, and now run `vagrant provision`.

After this step is finished, the virtual machine should be ready to use.

## Required dependencies

To build the virtual machine in this recipe, you need the following software installed:

- VirtualBox
- Vagrant
- Ansible

On Ubuntu 18.04 you can install them with:

```bash
sudo apt -y install virtualbox virtualbox-guest-utils vagrant ansible
```

## Usage

The login to the vm is vagrant:vagrant

## Troubleshooting

If you run Windows 10 on your host machine, and get a message such as "VT-X
missing" when trying to start the virtual machine, you can try the following:

- Start PowerShell as administrator (Search for it in the start menu, and right
  click and choose "Run as Administrator" or "Kör som administratör")
- In PowerShell, run the command: `bcdedit /set hypervisorlaunchtype off`
- Restart the computer

If this still does not help, you can also try:

- Open the control panel (Search for "control panel" in the start menu)
- Choose "Programs and features"
- Choose "Add or remove features in Windows"
- Disable "Hyper-V"

## Acknowledgements

The development of this project is sponsored by:

- [Savantic AB](https://savantic.eu/)
- [RIL Partner AB](https://rilpartner.com/)
