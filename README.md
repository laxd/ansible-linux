# ansible-linux
A collection of roles and ansible files that help to set up linux machines, including desktop, laptop, headless, VMs etc

Available playbooks:

* main.yml (Effectively the same as running all of the below playbooks)
* vm.yml
* physical.yml

To install dependencies:

    ansible-galaxy install -r requirements.yml

To run:

    ansible-playbook main.yml


