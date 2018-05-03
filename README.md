# KafkaBrokersWithAnsible
Codes for install/configure Apache Kafka brokers using Ansible playbook

# Files
/hosts/hosts
  - all required kafka servers with IP

/kafka-playbook.yml
  - ansible playbook script with kafka/zookeeper installation and configuration steps
	
/zk/zookeeper.j2
  - zookeeper properties

# Installation
For basic installation what you need to do is to set hosts file (-i option) and provide -l option to further specify that group of servers, given that your hosts file includes more than one group of hosts.

ansible-playbook -i hosts/hosts -l kafka -u [user] kafka-playbook.yml
