# the shibgreen hand
- shibgreen specific docker
- log parser

# build
- sudo docker build --no-cache --build-arg CODE_BRANCH=1.0.0 -t coctohug-shibgreen:latest .
- sudo docker build --build-arg CODE_BRANCH=1.0.0 -t coctohug-shibgreen:latest .

# docker-compose
- coctohug-shibgreen: 
        image: coctohug-shibgreen:latest 
        container_name: coctohug-shibgreen
        hostname: pc1 
        restart: always 
        volumes: 
            - ~/.coctohug-shibgreen:/root/.chia 
            - "/mnt/disk1:/plots1" 
            - "/mnt/disk2:/plots2" 
        environment: 
            - mode=fullnode 
            - controller_address=192.168.1.74 
            - worker_address=192.168.1.74
            - plots_dir=/plots1:/plots2 
        ports: 
            - 12648:12648 
            - 7442:7442 
            - 18974:18974

## Trademark Notice
CHIA NETWORK INC, CHIA™, the CHIA BLOCKCHAIN™, the CHIA PROTOCOL™, CHIALISP™ and the “leaf Logo” (including the leaf logo alone when it refers to or indicates Chia), are trademarks or registered trademarks of Chia Network, Inc., a Delaware corporation. *There is no affliation between this Coctohug project and the main Chia Network project.*Sun Nov 28 21:01:16 CST 2021
Tue Nov 30 09:39:39 CST 2021
Wed Dec 1 10:18:10 CST 2021
Sat Dec 4 15:03:38 CST 2021
Sun Dec 5 13:44:41 CST 2021
