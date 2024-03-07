# Linux bash kubectl completion
```sh
# Install bash-completion
sudo apt-get install bash-completion
source /usr/share/bash-completion/bash_completion
# Enable kubectl completion
echo $'source <(kubectl completion bash)\nalias k=kubectl\ncomplete -o default -F __start_kubectl k' >>~/.bashrc
source ~/.bashrc
```
