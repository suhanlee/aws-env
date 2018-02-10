# aws-env
aws environment documentation

# EB
## Install eb-cli
### (requirement) Install python - Installing pyenv
```
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
$ echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
$ source ~/.bash_profile
```
install python specific version using pyenv
```
$ pyenv install 3.6.1
$ pyenv local 3.6.1
```
install awseb cli using pip
```
$ pip install awsebcli --upgrade --user
```
configurating aws account
```
$ aws configure
AWS Access Key ID [****************AQOQ]: 
AWS Secret Access Key [****************vqZK]: 
Default region name [ap-northeast-2]: 
Default output format [None]: json
```
initialize eb setup including region, language, keypair
```
$ cd [project-directory]
$ eb init [project-name]
```
create eb env
```
$ eb create [env-name]
Creating application version archive "app-818b-180210_152441".
Uploading [project-name]/app-818b-180210_152441.zip to S3. This may take a while.
Upload Complete.
Environment details for: [env-name]
  Application name: [app-name]
  Region: ap-northeast-2
  Deployed Version: app-818b-180210_152441
  Environment ID: e-cmxp6zfej9
  Platform: arn:aws:elasticbeanstalk:ap-northeast-2::platform/Puma with Ruby 2.4 running on 64bit Amazon Linux/2.6.5
  Tier: WebServer-Standard-1.0
  CNAME: UNKNOWN
  Updated: 2018-02-10 06:24:45.782000+00:00
Printing Status:
INFO: createEnvironment is starting.
INFO: Using elasticbeanstalk-ap-northeast-2-782164292379 as Amazon S3 storage bucket for environment data.
INFO: Created security group named: 
INFO: Created security group named: 
INFO: Created load balancer named: 
INFO: Created Auto Scaling launch configuration named: 
INFO: Created Auto Scaling group named: 
INFO: Waiting for EC2 instances to launch. This may take a few minutes.
INFO: Created Auto Scaling group policy named:
INFO: Created Auto Scaling group policy named:
INFO: Created CloudWatch alarm named: 
INFO: Created CloudWatch alarm named: 
INFO: Successfully launched environment: [env-name]
```

## rails
create secret key and add env variable to eb (SECRET_KEY_BASE) on AWS EB Console
```
$ rake secret
34216fa4947d75eeb2fa706c939cbea59e7624fe864e6e73c19231a8ef50407a84c5661a794719c07379c44809e05946621178b5d713b170b63fa8d781e791fc
```
