🔰Ansible PlayBook does the following operations in the managed nodes: 🔹 Configure Docker 🔹 Start and enable Docker services 🔹 Pull the httpd server image from the Docker Hub 🔹 Run the docker container and expose it to the public 🔹 Copy the HTML code in the/var/www/html directory and start the web server🌐

Follow this step:-💡♾️
👉step1: Launch 2 instance in Amazon-linux2 image one for managed and 2nd for slave
step2: Install Ansible: ansible-2.9.23-1.amzn2.noarch version
step3: install collection: ansible-galaxy collection install community-docker 
Step 4: Make ansible.cfg file for configuration in the ansible folder
Step5: Make an Inventory and paste the slave IP name inside [dev]
Step 6: check the slave node from command #ansible dev -m ping  check  it running fine or not. (if get error go to slave node and type a command vim /etc/ssh/sshd_config and then give the #publicpasswordaccess yes that's it. and restart the sshd after slave node go to managed node and copy the slave node ip iD through command ssh-coyp-id @ec2-user and the slave node Ip)
Step7: create a file name Docker.yml and paste the entire code a
step8:Run the code ansible-playbook Docker.yml
step9: If you want to check the webserver is running fine or not
step10: copy slave ip and type on server 192.03.33.44:8080/index.html then you can see the results...
