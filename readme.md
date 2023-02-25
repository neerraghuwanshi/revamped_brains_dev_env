# Setup
1. In the root level of this repo do the following:
- Create an env directory and paste mongodb.env, backend.env and frontend.env files in it.
- Paste frontend and backend repos named frontend and backend only.

## How to Use
1. To create the environment:
    ```docker compose up -d```

1. stop the environment:
    ```docker compose stop```

1. To resume the environment:
    ```docker compose start```

1. To destroy the environment:
    ```docker compose down```

1. To rebuild the images and setup the environment:
    ```docker compose down --rmi```
    ```docker compose up -d --build```

1. To run a command for a specific application:
    ```docker compose exec <service_name> <command>```

1. remove all unused anonymous volumes with the following command:
    ```docker volume rm $(docker volume ls -q -f dangling=true -f name=^.{64}$)```

1. To remove images which are not associated to any containers and without a name:
    ```docker images -f dangling=true | grep '^<none' | awk '{ print $3; }' | xargs docker rmi -f```
