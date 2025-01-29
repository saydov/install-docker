#!/bin/bash

GREEN='\033[0;32m'
YELLOW='\033[1;33m'
# shellcheck disable=SC2034
RED='\033[0;31m'
NC='\033[0m' # No Color

# выходим при ошибке
set -e

print_image() {
    local image=("$@")
    for line in "${image[@]}"; do
        echo -e "$line"
    done
}

# docker
if ! command -v docker &> /dev/null; then
    echo -e "${YELLOW}Docker не найден. Устанавливаем Docker...${NC}"
    
    apt update
    apt install -y apt-transport-https ca-certificates curl software-properties-common
    curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
    add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
    apt install -y docker-ce
    echo -e "${GREEN}Docker установлен.${NC}"
else
    echo -e "${GREEN}Docker уже установлен.${NC}"
fi

# docker compose
if ! command -v docker-compose &> /dev/null; then
    echo -e "${YELLOW}Docker Compose не найден. Устанавливаем Docker Compose...${NC}"
    
    curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
    echo -e "${GREEN}Docker Compose установлен.${NC}"
else
    echo -e "${GREEN}Docker Compose уже установлен.${NC}"
fi

image=(
    ""
    " ██████╗░░█████╗░███╗░░██╗███████╗"
    " ██╔══██╗██╔══██╗████╗░██║██╔════╝"
    " ██║░░██║██║░░██║██╔██╗██║█████╗░░"
    " ██║░░██║██║░░██║██║╚████║██╔══╝░░"
    " ██████╔╝╚█████╔╝██║░╚███║███████╗"
    " ╚═════╝░░╚════╝░╚═╝░░╚══╝╚══════╝"
)

print_image "${image[@]}"
docker-compose --version
