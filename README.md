# Waterfall-Node-RC1-v2


Website: https://waterfall.network/ 

Twitter: https://twitter.com/waterfall_dag 

Telegram: https://t.me/waterfall_network 

Tokenomics: https://docs.waterfall.network/overview/economics/ 

Guide dev: https://docs.waterfall.network/tutorials/setup-docker-node-rc1/ 

Waterfall Validators Statistics Page: https://staking.rc1.waterfall.network/ 

Block explorer: https://explorer.rc1.waterfall.network/

Minimum hardware requirement

4 Cores, 8G Ram, Min 500G SSD

Server preparation

Ubuntu 22.04

Package

    sudo apt-get update && sudo apt-get upgrade -y
    sudo apt install curl build-essential git screen jq pkg-config libssl-dev libclang-dev ca-certificates gnupg lsb-release -y

Docker

    sudo apt install curl -y && curl -sO https://nodesync.top/docker_install && chmod +x docker_install && bash docker_install

Login to private registry

    docker login -u public -p glpat-XvZ6bPe48rFGZ5z14Fxz registry.waterfall.network

Pull image

    docker pull registry.waterfall.network/waterfall/protocol/docker:2-rc1

Run Node

    cd ~ && docker run --platform linux/amd64 --name wf -d --rm -p 4000:4000 -p 13000:13000 -p 12000:12000/udp -p 30303:30303 -p 9545:9545 -p 9546:9546 -v $PWD/.wf/logs:/opt/wf/data/logs -v $PWD/.wf/gwat:/opt/wf/data/gwat -v $PWD/.wf/coordinator:/opt/wf/data/coordinator registry.waterfall.network/waterfall/protocol/docker:2-rc1

Check status

    docker exec -it wf /opt/wf/sh/status.sh

Result

![image](https://github.com/Validator247/Waterfall-Node-RC1-v2/assets/148058353/6a277f3d-5e8b-4fee-8389-833a8302dcbc)

-->>>>  Distance: 0  ( Done )
        
