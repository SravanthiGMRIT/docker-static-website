\# Docker Static Website



\## Project Description



This project demonstrates how to containerize a simple static website using Docker and Nginx.



The website contains an HTML page and CSS styling. The website is copied into an Nginx Docker image and served through an Nginx web server running inside a Docker container.



\## Technologies Used



\* HTML5

\* CSS3

\* Docker

\* Nginx



\## Project Structure



```text

docker-static-website/

├── Dockerfile

├── index.html

├── style.css

└── README.md

```



\## Dockerfile



```dockerfile

FROM nginx:latest



COPY . /usr/share/nginx/html



EXPOSE 80

```



\## Build the Docker Image



Open PowerShell and go to the project directory:



```powershell

cd C:\\docker-static-website

```



Build the Docker image:



```powershell

docker build -t static-website .

```



\## Run the Docker Container



```powershell

docker run -d -p 8080:80 --name static-web-container static-website

```



\## Check the Running Container



```powershell

docker ps

```



\## Access the Website



Open your browser and visit:



```text

http://localhost:8080

```



\## Port Mapping



```text

8080:80

```



\* `8080` = Port on the host computer

\* `80` = Port inside the Docker container



\## Stop the Container



```powershell

docker stop static-web-container

```



\## Start the Container Again



```powershell

docker start static-web-container

```



\## Remove the Container



```powershell

docker rm static-web-container

```



\## Project Workflow



```text

HTML + CSS

&#x20;   ↓

Dockerfile

&#x20;   ↓

Docker Image

&#x20;   ↓

Docker Container

&#x20;   ↓

Nginx

&#x20;   ↓

http://localhost:8080

```



\## GitHub Repository



GitHub repository:



https://github.com/SravanthiGMRIT/docker-static-website



\## Conclusion



This project demonstrates how a static HTML and CSS website can be packaged into a Docker image and served using Nginx inside a Docker container.



