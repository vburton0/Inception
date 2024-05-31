# Inception


# Docker
    # Commande

    - docker build <folder_location> -t nginx .
        - build image with name nginx
    - docker image ls
        - Show the images
    - docker run -it <image_name>
        - Run an image and open his terminal (with -it)
    - docker ps
        - Show the running containers

    # .yml command

    - docker-compose -f  <path_docker_compose>  -d —build
        - Build the .yml file
    - docker-compose -f  <path_docker_compose>  stop
        - Stop 
    - docker-compose -f  <path_docker_compose>  down -v
        - Delete

    # Launch command
        - docker-compose build --no-cache
        - docker compose up  


    

# Sources
- https://tuto.grademe.fr/inception/
