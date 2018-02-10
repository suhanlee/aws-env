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
