# Container image that runs your code
FROM alpine:3.21

# Copies your code file from your action repository to the filesystem path `/` of the container
COPY entrypoint.sh /entrypoint.sh
COPY wsl-distribution.conf /etc/wsl-distribution.conf
COPY wsl.conf /etc/wsl.conf
COPY terminal-profile.json /usr/lib/wsl/terminal-profile.json
COPY oobe.sh /etc/oobe.sh

# Code file to execute when the docker container starts up (`entrypoint.sh`)
ENTRYPOINT ["/entrypoint.sh", $SCRIPT_TO_EXECUTE]