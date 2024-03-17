# Automated-Container-deployment-and-Administration
Step 1: Setup Virtual Machines on AWS
- Create two Virtual Machines: one for the Control Node and another for the Managed Node.
- Ensure that both machines are accessible over SSH.

Step 2: Configuration of Control Node
- SSH into the Control Node and install Ansible along with necessary packages.
- Create a myhosts.txt file to specify the IP address of the Managed Node.
- Configure Ansible settings in ansible.cfg.

Step 3: Configuration of Managed Node
- SSH into the Managed Node and install Docker and Apache HTTP Server (httpd).
- Ensure Docker is running and accessible.

Step 4: Establish SSH Connection between Control Node and Managed Node
- Generate SSH keys on the Control Node using ssh-keygen.
- Copy the public key to the Managed Node to enable passwordless SSH access.

Step 5: Create Ansible Playbook
- On the Control Node, create a playbook named docker_deploy.yml.
- Define tasks in the playbook to deploy Docker containers, including the Apache HTTP Server container.

Step 6: Execute Ansible Playbook
- Run the Ansible playbook using the command: ansible-playbook docker_deploy.yml.
- Ensure that the playbook executes successfully without errors.

Step 7: Verification
- Verify the deployment by pinging the server using ping command.
- Access the Apache HTTP Server running in the Docker container by navigating to the public IP address of the Managed Node in a web browser.

Step 8: Cleanup (Optional)
- Optionally, include steps to clean up resources after deployment, such as stopping and removing Docker containers.

By following these steps, we automate the deployment of Docker containers using Ansible and verify the accessibility of the services deployed.
