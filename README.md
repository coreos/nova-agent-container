# Nova Agent Container

Minimal container to have nova-agent running in a container

## Running

### systemd-nspawn

```
systemd-nspawn -D /srv/nova-agent/ /bin/sh -c      \
    "HOME=/root mount -t xenfs none /proc/xen;     \
    /usr/share/nova-agent/0.0.1.37/sbin/nova-agent \
    -o - -n -l info /usr/share/nova-agent/nova-agent.py"
```
