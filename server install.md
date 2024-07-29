sudo dnf install git -y
sudo dnf install docker -y
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s | tr '[:upper:]' '[:lower:]')-$(uname -m) -o /usr/bin/docker-compose && sudo chmod 755 /usr/bin/docker-compose
sudo service docker start
sudo usermod -a -G docker ec2-user
git clone https://github.com/nahueltori/mediawiki.git
cd mediawiki
docker-compose up --build