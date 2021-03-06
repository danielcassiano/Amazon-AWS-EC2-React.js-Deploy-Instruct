# Amazon-AWS-EC2-Deploy-Instruct

## Português
Documentação criada para instruir comandos no deploy de aplicações React.js na Amazon AWS EC2 (E. Cloud 2):

1. Comando para conexão à instância
ssh -i "MeuKeyPair.pem" ec2-user@ec2-18-230-199-167.sa-east-1.compute.amazonaws.com

2. Comando para permissões e atualizações da máquina
sudo su
yum update -y

3. Comando para encontrar path raíz da máquina
pwd

4. Comando para criar a pasta build do projeto a ser feito o deploy
npm run build

5. Comando para copiar "/build" do projeto para a máquina virtual
scp -i "MeuKeyPair.pem" -r build/ USUÁRIOEC2:/home/ec2-user (pwd)

6. Comando para instalar Apache (httpd)
yum install httpd

7. Apache start
service httpd start

8. Apache status
service httpd status

9. Abrir o link da instância no navegador
http://ec2-18-229-150-15.sa-east-1.compute.amazonaws.com/

10. Comandos para hospedar a build no Apache (html)
10.1 cd /var/www/html
10.2 mv build/* .
10.3 rm -rf build/
10.4 ls -la

## English
Documentation created to instruct commands in deploying React.js applications on Amazon AWS EC2 (E. Cloud 2):

1. Command to connect to the instance
ssh -i "MyKeyPair.pem" ec2-user@ec2-18-230-199-167.sa-east-1.compute.amazonaws.com

2. Command for machine permissions and updates
sudo su
yum update -y

3. Command to find the machine's root path
pwd

4. Command to create the build folder of the project to be deployed
npm run build

5. Command to copy "/ build" from the project to the virtual machine
scp -i "MyKeyPair.pem" -r build / USEREC2: / home / ec2-user (pwd)

6. Command to install Apache (httpd)
yum install httpd

7. Apache start
service httpd start

8. Apache status
service httpd status

9. Open the instance link in the browser
http://ec2-18-229-150-15.sa-east-1.compute.amazonaws.com/

10. Commands to host the build on Apache (html)
10.1 cd / var / www / html
10.2 mv build / *.
10.3 rm -rf build /
10.4 ls -la
