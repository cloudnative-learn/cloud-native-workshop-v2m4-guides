# Bulent's notes

## Installation
Python does not rely on MacOS' openSSL. It comes with its own openSSL bundled and doesn't have access on MacOS' root certificates.
```
cd /Applications/Python\ 3.9/
./Install\ Certificates.command
```

```
ansible-galaxy install siamaksade.openshift_workshopper
```

```
oc login --token=<TOKEN> --server=https://c116-e.us-south.containers.cloud.ibm.com:32274
ansible-playbook ./install-guide.yml
```
Shows errors on first run, but actually does the installation. Second run shows success.

## Notes

namespace=$(oc project -q)
openshift_token=$(oc whoami -t)
openshift_master_url=$(oc whoami --show-server)