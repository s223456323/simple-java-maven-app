# simple-java-maven-app

This repository is for the
[Build a Java app with Maven](https://jenkins.io/doc/tutorials/build-a-java-app-with-maven/)
tutorial in the [Jenkins User Documentation](https://jenkins.io/doc/).

The repository contains a simple Java application which outputs the string
"Hello world!" and is accompanied by a couple of unit tests to check that the
main application works as expected. The results of these tests are saved to a
JUnit XML report.

The `jenkins` directory contains an example of the `Jenkinsfile` (i.e. Pipeline)
you'll be creating yourself during the tutorial and the `jenkins/scripts` subdirectory
contains a shell script with commands that are executed when Jenkins processes
the "Deliver" stage of your Pipeline.

---------------------------------------------------------------------------------

Open a Terminal in Ubuntu. Update the Ubuntu package manager before proceeding using the command: sudo apt update
Install the prerequisite packages for Docker by entering the command: sudo apt install ca-certificates curl gnupg lsb-release
Add Docker’s official GPG key using the command: curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
Setup the Docker repository below to the latest stable release by entering the below command in the terminal. Type this on the one line in the terminal: echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
With the Docker repository correctly configured with apt, prepare for installation with: sudo apt update
Install Docker using the command: sudo apt-get install docker-ce docker-ce-cli containerd.io
Verify installation was complete by running a simple Docker container called “Hello World”: sudo docker run hello-world
Installing DVWA using Docker
With Docker installed, we can install the Damn Vulnerable Web Application (via a Docker container) quite easily, as it will take care of all the dependencies required (e.g. mySQL).

Open a terminal within your Ubuntu instance.
Install DVWA with the following command: sudo docker run --restart always -p 80:80 vulnerables/web-dvwa
DVWA should now be installed and running. To access it, open up Firefox and browse to your localhost address. In other words, in the URL toolbar (where you type in URLs), type in localhost and press the ENTER key.
Login to DVWA with username admin and password password
Once logged in, select the ‘Create/Reset Database’ link.
Return Ubuntu back to an Internal network (so that Ubuntu and Kali and communicate with each other; refer to the ‘Connect Ubuntu and Kali’ screencast for a reminder if needed).
Ensure that they are connected by pinging each other.
