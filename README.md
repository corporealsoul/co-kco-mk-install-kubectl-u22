### Install kubectl,

`anup@ubuntu-22042-08:~$ curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`

`anup@ubuntu-22042-08:~$ curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"`

`anup@ubuntu-22042-08:~$ echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check`

<br>

`anup@ubuntu-22042-08:~$ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl`

`anup@ubuntu-22042-08:~$ kubectl version --client`

<br>
