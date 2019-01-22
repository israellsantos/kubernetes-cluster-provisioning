# Kubernetes Cluster Provisioning - Ansible


## Playbooks

Ansible Playbooks para criação de um cluster Kubernetes

hosts.ini = nomes dos hosts e seus papéis (master ou nodes)

Ordem de execução:

    ansible-playbook -i hosts.ini -v initial.yaml
    ansible-playbook -i hosts.ini -v dependencies.yaml
    ansible-playbook -i hosts.ini -v master.yaml
    ansible-playbook -i hosts.ini -v nodes.yaml

## Laboratorio Vagrant

Inclui Vagrantfile para configuração de um ambiente de laboratório

master = kube-master.lab
nodes  = kube-node1.lab, kube-node2.lab

Configuração das VMs:

- 2 CPUs
- 2GB de RAM

Para subir o ambiente basta executar:

    vagrant up
