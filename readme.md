# Setup
1. Create an env directory and paste mongodb.env, backend.env and frontend.env files in it.
2. Paste frontend and backend repos named frontend and backend only.
3. Never rename this folder unless you are proficient with docker.

## How to Use
1. To create the environment:
    ```docker compose up -d```

2. stop the environment:
    ```docker compose stop```

3. To resume the environment:
    ```docker compose start```

4. To destroy the environment:
    ```docker compose down```

5. To rebuild the images and setup the environment:
    ```docker compose down```
    ```docker compose up -d --build```

6. To run a npm command in a specific application:
    ```docker compose run --rm <service_name> <command_without_npm_keyword>```

7. remove all unused anonymous volumes with the following command:
    ```docker volume rm $(docker volume ls -q -f dangling=true -f name=^.{64}$)```
