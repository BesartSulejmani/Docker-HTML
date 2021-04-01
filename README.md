# Docker container and html page
                            ## 
              ## ## ##       ==          
           ## ## ## ##      ===          
       /""""""""""""""""\___/ ===        
      |_ _ _ _ _ _ _ _ _ _ _ /
       \______ o          __/            
         \    \        __/             
          \____\______/                
 
          |          |
       __ |  __   __ | _  __   _
      /  \| /  \ /   |/  / _\ | 
      \__/| \__/ \__ |\_ \__  |

## Prepare Your Environment
---

### VS Code

| Name                                    | Installation Method    | Source                                             |
| ----------------------------------------| -----------------------| ---------------------------------------------------|
| VS Code                                 | Download & Install     | [Download here](https://code.visualstudio.com/)    |
| Docker                                  | VS Code extension      | Install in VS Code                                 |

### Docker desktop

| Name                                    | Installation Method    | Source                                                             |
| ----------------------------------------| -----------------------| -------------------------------------------------------------------|
| Docker desktop                          | Download & Install     | [Download here](https://www.docker.com/products/docker-desktop)    |


## nginx alpine

Container image based on nginx alpine (latest).

## Index.html

Contains "index.html" which you can alter to your liking. This file will be stored inside the image and the container will be built using that image.

## Build image

'docker build -t my-page:v1.0 .'

Make sure you run the command in the directory where the \'Dockerfile' is stored.

## Running the container

'docker run –d –p 8080:80 my-page:v1.0'

This will run the container in detached mode (-d) and publishes the containers ports to the host (-p),external port of 8080 and an internal container port of 80. The image to use is my-page with a tag of v1.0.

*NOTE: I have issues sometimes copying and pasting the code in my terminal and it won't run the container for me that way, so type it in manually if you have the same issue* 

### Web browser

Browse to http://localhost:8080 and you should see the webpage containing a message and ASCII-art :-) 

## Cleanup

'docker ps -a'

Shows all running containers with a CONTAINER ID. Copy the ID that is attached to the IMAGE: my-page:v1.0.

'docker stop [CONTAINER ID]'

Stops the container.

'docker rm [CONTAINER ID]'

Removes the container.