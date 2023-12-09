# Docker configuration files :whale2:

This is a list of docker files that have been configured to use different types of programming languages and run projects without the need to install environments or files locally.

## What the hell are you going to find here? :confused:

You will find development environments configured in Docker or Docker images, not at an expert level but you can work without installing Node js, Python and other environments to run programming languages.

## How the hell do I run these files? :rage:

Don't worry Sailor, I'm going to explain to you how to do it using two simple commands:

1. **First command** :eggplant:
    - Go to the project folder, open a terminal, and then run the following command:
    ```docker build -t your_image_name .```
2. **Second command** :alien:
    - Then run the following command:
    ```docker run -d -p 8080:8080 your_image_name```

## Warning :weary:

Dude remember that you can modify the **Port** both in the command in the terminal and in the Docker configuration file. :sweat_drops: