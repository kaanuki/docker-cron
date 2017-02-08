# Docker-Cron  
Container to run other containers as cron jobs  

## Building the Container  

    docker build -f Dockerfile -t camilin87/docker-cron .

## Running the script in the container  

    docker run -it --rm --name docker-cron \
        -v /var/run/docker.sock:/var/run/docker.sock \
        -v "$PWD":/usr/src/app -w /usr/src/app \
        camilin87/docker-cron \
        npm start