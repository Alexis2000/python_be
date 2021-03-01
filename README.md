### Build the image
`docker build -t python_be:latest .`

### Run the container with name python_fe
`docker run --name python_be -d -p 8080:80 python_be:latest`

### Create a network to enable communication 
`docker network create python_nw`<br>
`docker network connect python_nw python_be`<br>
`docker network connect python_nw python_fe`<br>

### Find both containers IP addresses
`docker network inspect python_nw`

