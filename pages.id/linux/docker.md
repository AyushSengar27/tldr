file_content = """
# Docker Configuration and Cheatsheet

## Table of Contents:
1. [Installing Docker](#installing-docker)
2. [Basic Docker Commands](#basic-docker-commands)
3. [Creating and Managing Containers](#creating-and-managing-containers)
4. [Working with Images](#working-with-images)
5. [Volumes and Networks](#volumes-and-networks)
6. [Dockerfile Basics](#dockerfile-basics)
7. [Docker Compose](#docker-compose)
8. [Common Docker Troubleshooting Commands](#common-docker-troubleshooting-commands)
9. [Docker Cheatsheet](#docker-cheatsheet)

---

## Installing Docker

1. **Ubuntu**:
    ```bash
    sudo apt-get update
    sudo apt-get install \\
        ca-certificates \\
        curl \\
        gnupg \\
        lsb-release

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --batch --yes --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    echo \\
      "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \\
      $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

    sudo apt-get update
    sudo apt-get install docker-ce docker-ce-cli containerd.io
    ```

2. **MacOS**:
   - Install via [Docker Desktop](https://www.docker.com/products/docker-desktop) for Mac.

3. **Windows**:
   - Install via [Docker Desktop](https://www.docker.com/products/docker-desktop) for Windows.

Verify installation:
```bash
docker --version
