### Install kubectl binary with curl on Linux ,

**Download the latest release with the command ,**

`[anup@rhel-92-04 ~]$ curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`


**Validate the binary (optional) ,**

`[anup@rhel-92-04 ~]$ curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"`


**Validate the kubectl binary against the checksum file ,**

`[anup@rhel-92-04 ~]$ echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check`

<br>

**Install kubectl**

`[anup@rhel-92-04 ~]$ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl`

<br>

`[anup@rhel-92-04 ~]$ kubectl version --client`

`[anup@rhel-92-04 ~]$ kubectl version --client --output=yaml`
