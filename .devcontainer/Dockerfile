FROM node:18

# Install basic development tools
RUN apt update && apt install -y less man-db sudo

RUN npm install solc@0.4.17 && npm install mocha ganache web3

# Ensure default `node` user has access to `sudo`
ARG USERNAME=node
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true
