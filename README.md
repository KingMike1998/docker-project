# docker-project
For my project, I ran Ansible on an Ubuntu based VM using Oracle VM VirtualBox.

Requirments:
  1. Operating System (Windows, Linux, MacOS)
  2. Ansible installed on the system
  
Contents of my project:
  1. Dockerfile - contains the configuration of the container to be created
  2. docker-compose.yml -- contains the configuration for docker-compose to be able to build the container and run it at the same time
  3. .env file -- cotnains the port mapping used in the docker-compose file
  4. ansible-playbook -- contains the instructions for the ansible playbook to run succesfully
  5. inventory.yml -- contains information about the system where we are running the playbook and also has customisation on the port on which the application in the container is running.
  
  
Here are the instructions on how to run my project:
  1. Clone my repository to your local machine to locally run the project:
    git clone https://github.com/mike-soroceanu/docker-project.git
  2. Navigate into the app directory of my project
    cd ~/docker-project/app
  3. Run the ansible-playbook from the terminal
    ansible-playbook docker-playbook.yml -i inventory.yml
  4. Check on the guest machine if the container is up and running
    docker ps
    
For a quick demo you can take a look at the 2 videos hosted in this repo in the following order:
  1. MasterAnsibleNodeRuningPlaybook
  2. GuestNodewithContainerandApp

