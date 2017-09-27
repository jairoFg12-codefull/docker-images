## Instructions

``` 
    # First you should build the image
    docker-compose build

    # If you want up the image manually
    docker run -ti --rm -v /c/Users/YOUR_USER/Proyectos/folder/:/usr/src/app -p 4200:4200 -p 49153:49153 -p 9876:9876 -p 49152:49152 frontened_client-angular bash

    # If you want up the image automatically, remember the Dockerfile and the docker-compose must is in the root folder of your project

    docker-compose up -d  ## You can wait few seconds, your app is run in http://localhost:4200

    # now you can attach to container, and execute more commands
    docker-compose exec client-angular bash


    # Create a new Project
    ng new Project_name --directory .

    ng serve --host 0.0.0.0 --poll=2000
    ng test --poll 2000
```