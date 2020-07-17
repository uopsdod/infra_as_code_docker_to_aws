### how to run this project

step01: git clone 

step02: cd 

step03: docker-compose build --no-cache

step04: docker-compose up -d 

step05: docker container ls 

step06: echo $(docker-machine ls)

step07: go to browswer and type
http://{ip.ip.ip.ip}:3000/

DONE

#### NEXT: 將dbec2 userdata, appec2 userdata合起cloudformation template

#### NEST: web ec2 part

#### tmp stuff - db ec2 userdata 
sudo yum install -y git
sudo git clone https://github.com/uopsdod/infra_as_code_docker_to_aws.git
cd infra_as_code_docker_to_aws/db_new
sudo yum install -y docker
sudo service docker start
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
sudo docker-compose up -d

#### tmp stuff - app ec2 userdata
sudo yum install -y git
sudo git clone https://github.com/uopsdod/infra_as_code_docker_to_aws.git
cd infra_as_code_docker_to_aws/app_new
sudo yum install -y docker
sudo service docker start
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
sudo docker-compose up -d

