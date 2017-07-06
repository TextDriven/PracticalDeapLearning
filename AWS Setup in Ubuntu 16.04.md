# [Practical Deap Learning for Coders](http://course.fast.ai/)
---
## AWS Setup in Ubuntu 16.04
1. create amawon AWS account
2. [requset EC2 limit upgrade](https://aws.amazon.com/contact-us/ec2-request)
configuration of my instance
 * _Oregon(US)_
 * _p2.xlarge_
 * reason: _fast.ai_
3. install python2.7 avec Anaconda and pip
 * download Anaconda for python 2.7
 * `sudo apt-get install python-pip`
4. install AWS CLI
 * `pip install awscli`
5. [create new AWS user](https://console.aws.amazon.com/iam/home?region=eu-west-1#/users$new?step=details)
 * [User name]
 * Check '_Programmatic access_'
 * Add policies directly -> '_AdministratorAccess_'
 * download **credentials.csv** to local PC where [User Name], [Access key ID], [Secret access key], [Console longin link] are stored
6. configure AWS
 * `aws configure`
 * enter [Access key ID]
 * enter [Secret Access Key]
 * Region: _us-west-2_
 * Output format: _text_
7. download setup scripts
 * [url](http://files.fast.ai/files/)
 * `wget [url]/setup_p2:sh`
 * `chmod 775 setup_p2.sh`
8. run setup of p2 instance
 * `bash setup_p2.sh`
 * copy screen output information into a file for later use
  * _securityGroupID_
  * _subnetId_
  * _instanceId_
  * _instanceUrl_
  * _Connect_
9.  connect to AWS server
 * `ssh -i /home/[localUser]/.ssh/aws-key.pem ubuntu@[_instanceUrl_]`
 * enter 'Yes' to go into AWS VM
10. check GPU setup
 * `nvidia-smi`
11. run jupyter-notebook
 * `jupyter-notebook`
 * in web browser, type http://[_instanceUrl_]:8888
 * pass word is 'dl_course'
12. check theano, keras package setup 
 * create a new notebook in '**nbs**' folder with Python [_conda root_]
 * `import theano`
 * `import keras`
13. use shortcuts
 * download alias file > wget [url]/aws-alias:sh
 * `source aws-alias.sh`
 * to stop instance -> `aws-stop`
 * to start instance -> `aws-start`
 * to connect instance -> `aws-ssh`
 * to get instance url -> `aws-ip`
 * to get instance info -> `aws-get-p2`
 14. stop instance and release associated Elastic IP
 
