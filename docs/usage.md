# Usage

### How to start the ecosystem

1. Execute the following command in library-shelf and library-stats:
    ```
    ./mvnw -Pprod verify jib:dockerBuild
    ```
2. Execute the following command in this repo:
     ```
     docker-compose -f docker/app.yml up -d
     ```
3. If this is first time:
    
    Create rabbitmq user:
    
    ```shell script
    docker exec -it {rabbit_container} bash
    root@b309b0a8a6c6:/# rabbitmqctl add_user admin admin
    Adding user "admin" ...
    root@b309b0a8a6c6:/# rabbitmqctl set_user_tags admin administrator
    Setting tags for user "admin" to [administrator] ...
    root@b309b0a8a6c6:/# rabbitmqctl set_permissions -p / admin ".*" ".*" ".*"
    Setting permissions for user "admin" in vhost "/" ...
    ```

3. Access of the application
    
    There is no UI for the application, it can be used through the Swagger / Open API UI.
    
    1. Login to Jhipster registry: [localhost:8761](http://localhost:8761) (admin/admin)
    2. Navigate to Administration > API
    3. You can send requests by using the "Try it out" functionality of a given endpoint.
