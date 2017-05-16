# Software requirements

- socat

# How to:
Add entry to ~/.ssh/config:
```
host github.com
  proxyCommand socat - PROXY:ENTER_PROXY_ADDRESS_HERE:%h:%p,proxyport=ENTER_PROXY_PORT_HERE
```
