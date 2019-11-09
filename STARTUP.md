## Run in userdata on every boot

cd /home/ec2-user/concourse-docker
extu=$(curl -s http://169.254.169.254/latest/meta-data/public-hostname)
echo EXTURL=${extu}:8080 > .env
sudo docker-compose up -d
