# Practical Deap Learning for Coders
---
## AWS Setup in Ubuntu 16.04
1. create amawon AWS account
2. requset EC2 limit upgrade
* https://aws.amazon.com/contact-us/ec2-request
* Orgeon(US)
* p2.xlarge
* reason: fast.ai
3. install python2.7 avec Anaconda and pip
* download Anaconda for python 2.7
* sudo apt-get install python-pip
4. install AWS CLI
* pip install awscli
5. create new AWS user
* https://console.aws.amazon.com/iam/home?region=eu-west-1#/users$new?step=details
* [username]
* Check 'Programmatic access'
* next
* Add policies directly -> 'AdministratorAccess'
* next
* download credentials.csv to local PC where User Name, Access key ID, Secret access key, Console longin link are stored
6. configure AWS
* aws configure
* enter Access key ID
* enter Secret Access Key
* Region: us-west-2
* Output format: text
7. download setup scripts
* url: http://files.fast.ai/files/
* wget url/setup_p2:sh
* chmod 775 setup_p2.sh

