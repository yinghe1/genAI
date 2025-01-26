This doc list all the commandline and other tooling needed, assuming fresh Mac
Run which python3 in command, it is already installed, skip the following steps to install homebrew
1. install package manager homebrew https://brew.sh
using mac Terminal run command: 
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
then run these command to add Homebrew to your PATH so brew command will be available
```
echo >> /Users/tiger/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/tiger/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```
run this to verify that where crew is installed 
```
which brew
```
2. use brew to install python3
```
brew install python3
```
Now python3 should be available, now install pip:
```
python3 -m pip install --upgrade pip
```
Add pip to PATH, if you have .zprofile in your homedirectory
```
echo "export PATH=$PATH:/Users/<macUserName>/Library/Python/3.9/bin" >>.zprofile
```
Use pip to install jupyter notebook https://jupyter.org/install After install jupyter command shall be available
```
pip install notebook
```
