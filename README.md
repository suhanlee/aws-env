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
