# docker
# this is the bash file to install docker automatically by using one command

echo "*********************************** Start docker installation *************************************"
sudo apt update && sudo apt upgrade
# Install dependencies required to enable Docker repository
sudo apt install apt-transport-https ca-certificates curl software-properties-common

# Now Import the GPG key for repository using following curl command:
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

# Add the repository to your system typing following in the terminal
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update

# install docker
sudo apt install docker-ce
# check the docker version
docker -v

# Check the docker service status
sudo systemctl status docker

echo "*********************************** End docker installation ****************************************"

