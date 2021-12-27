# docker-scan-arm64
Docker scan binaries for debian 11 arm64 (raspberry-pi 4). 

Here you will find binaries for docker-scan compiled on a Debian 11 arm64 for raspberry pi 4.

Download the pre-built binary and put it in ~/.docker/cli-plugin/ directory.

If you want to build on your own you can follow the instructions.

## Build on your own
Download the latest source code version from [this link](https://github.com/docker/scan-cli-plugin/releases)
or from the command line:

`wget https://github.com/docker/scan-cli-plugin/archive/refs/tags/v0.16.0.tar.gz -o docker-scan.tar.gz`

Unzip/Untar the archive 

`tar xvzf docker-scan.tar.gz`

`cd scan-cli-plugin-0.16.0`

Pull missing images

`docker pull docker/dockerfile:experimental`

`docker pull golang:1.17.5`

Install make

`sudo apt-get install make`

And build

`make build`

Copy the built binary to docker plugin dir.

`cp bin/* ~/.docker/cli-plugin/`
