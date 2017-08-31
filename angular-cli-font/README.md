## Instructions

```
    docker run -ti --rm -v /c/Users/YOUR_USER/Proyectos/folder/:/usr/src/app -p 4200:4200 -p 49153:49153 -p 9876:9876  frontened_client-angular bash

    # Create a new Project
    ng new Project_name --directory .

    ng serve --host 0.0.0.0 --poll=2000
    ng test --poll 2000
```