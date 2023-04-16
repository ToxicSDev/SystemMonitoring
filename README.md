# SystemMonitoring

SystemMonitoring is a powerful project that monitors the performance of your system's CPU usage, memory usage, and disk usage in real-time, providing you with valuable insights into your system's resource utilization. The project is designed as a microservices architecture, consisting of two main components - the server for backend data gathering and the client for frontend visualization, allowing for efficient and scalable monitoring.

The client component provides a user-friendly interface that displays the system's resource utilization in a visually appealing pie chart. Each resource has three stages - normal, warning, and alert, each representing the current status of a particular resource usage. The normal stage indicates that the resource usage is within the acceptable range, while the warning stage indicates that the resource usage is approaching the threshold limit. The alert stage indicates that the resource usage has exceeded the threshold limit and requires immediate attention.

The SystemMonitoring project allows users to set customizable threshold limits for each resource usage, based on their system's requirements. When a resource usage exceeds the threshold limit, the client component shows that to the user. The microservices architecture of the project allows for scalability and flexibility, enabling it to be easily integrated into existing systems or deployed as a standalone monitoring solution. The server and client components communicate through sockets, allowing for seamless data exchange and updates.

## Dependencies

- [Docker](https://www.docker.com/) **(Recommended)** - Used for building, shipping, and running the microservices using containers. Docker-compose is used for scalability and container management.

- [NPM](https://www.npmjs.com/) **(Required if Docker isn't used)** - A package manager for the JavaScript programming language.

### NPM Packages

#### Server

- [express](https://www.npmjs.com/package/express) - The web application framework used to create the backend and frontend servers and the routing for them.

- [socket.io](https://www.npmjs.com/package/socket.io) - The library used to establish the communication and data transfer capabilities between the frontend and backend applications.

- [systeminformation](https://www.npmjs.com/package/systeminformation) - The library used for retrieving the system information being tracked, such as CPU, memory, disk usage, and more.

- [node-cron](https://www.npmjs.com/package/node-cron) - The library used to create the cron jobs for the refresh rate of the statistics being tracked. 

#### Client

- [express](https://www.npmjs.com/package/express) - The web application framework used to create the backend and frontend servers and the routing for them.

- [socket.io](https://www.npmjs.com/package/socket.io) - The library used to establish the communication and data transfer capabilities between the frontend and backend applications.

- [serve-favicon](https://www.npmjs.com/package/serve-favicon) - The library used for applying the favicon to the frontend application.

## Installation Guide

To install the application, follow the instructions and run the appropriate file below based on your setup:

| Setup       | Command        |
|-------------|----------------|
| Docker + Linux    | `./docker-start.sh` |
| Docker + Windows  | `docker-start.bat` |
| npm + Linux       | `./npm-start.sh`    |
| npm + Windows     | `npm-start.bat`     |

If you are using Docker, make sure Docker is installed and the daemon is running on your system before running the appropriate start file based on your operating system. The `docker-start.sh` and `docker-start.bat` scripts will build the Docker images and start the containers for you. If you rerun the start file it will first stop any existing containers and then rebuild and rerun the containers.

If you are not using Docker and prefer to use npm, make sure npm is installed on your system and run the appropriate start command based on your operating system. The `npm-start.sh` and `npm-start.bat` scripts will install the necessary npm packages and start the application for you.

Once the application is started, you can access it by navigating to `http://localhost:3030` in your web browser.
