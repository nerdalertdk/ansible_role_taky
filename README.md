# Taky Server Ansible role (Work in Progress)
--- 

### Requirements
  Only tested running ansible from OSX to Debian 12, but should work on Ubuntu also /shrug
  - Docker installed
  - Knowledge of ansible

### Setup

```yaml
# Create hosts.yaml file with the following info
---
all:
  hosts:
    taky.server.io:

# Main server host, usally only one 
taky_host:
  hosts:
    taky.server.io:

# Add as many instances of taky you need
taky_servers:
  hosts:
    blue.taky.server.io:
      ansible_host: taky.server.io
    red.taky.server.io:
      ansible_host: taky.server.io
    # Special Role given in pref files
    yellow.taky.server.io:
      ansible_host: taky.server.io
```

### Thanks
  - [tkuester](https://github.com/tkuester/taky) for creating Taky
  - [skadakar](https://github.com/skadakar) For inspiration
  - [Airsoftnorge](https://github.com/airsoftnorge) For inspiration


#### INFO 
  - https://mytecknet.com/creating-tak-data-packages-for-enrollment/
