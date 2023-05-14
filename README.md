# Postgres combo

This repository includes a simple docker compose config to setup Postgres + pgAdmin for development use.

- Projects that want to connect to this database should be on bridge network, or staying in a same user-defined network like below:

    ```
    docker network create shared-network
    ```

- and then define the network in compose file:
    ``` 
    networks:
    default:
        name: shared-network
        external: true
    ```