# Repository to reproduce this issue: https://github.com/portainer/portainer/issues/13003

1. Fork this repository
2. whoami: Create new stack from repository with gitOps updates enabled
3. nginx: Create new stack from repository with gitOps updates enabled and relative path volumes enabled
4. Check that the file network_internal.conf is present in the nginx container
5. Check that the folder access-lists and inside this folder the network_internal-ips.conf file is present in the nginx container
6. change something to the whoami docker-compose.yml
7. Wait for the gitOps update to be applied
8. Check the file network_internal.conf is still present in the nginx container
9. Check the folder access-lists and inside this folder the network_internal-ips.conf file --> will be missing