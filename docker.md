# Docker Cheatsheet

**Docker**: Tool to install software without headache. It creates an isolated environment in our system and allocates some physical resources to run containers.

- **Images**: The basis for creating containers, containing configurations, file system snapshots (files, applications), and startup commands.
  - Example: Running `docker run hello-world` searches the image cache for the `hello-world` image. If not found, it downloads from Docker Hub, stores it in the image cache, creates a container, and displays a message.

- **Command Flow**:
  1. Command goes to Docker client.
  2. Docker client processes the command and sends it to Docker server (daemon running in the background).

- **Linux Dependency**: Docker primarily runs on Linux, using control groups (allocating hardware to each container) and namespaces (separating Docker containers from each other and the host machine for process isolation).

- **Common Commands**:
  - `docker run = docker create(container from image) + docker start(container)`
  - `docker run image-name` → Creates and starts container.
  - `docker create image-name override-command` → Returns container ID.
  - `docker start -a id` → Attaches to Docker container and runs the command.
  - `docker ps` → Shows all running containers.
  - `docker ps --all` → Shows all stopped and running containers.
  - `docker logs id` → Shows output of the command of that container.
  - `docker system prune` → Deletes all containers and their resources.
  - `docker container prune` → Deletes all containers only.
  - `docker run -it image sh` → Opens shell.
  - `docker exec -it id command` → Runs multiple commands in a running container (another terminal).
  - `-it` → Interactive terminal flag.

- **Dockerfile**:
  - A configuration file specifying required software, packages, and container behavior.
  - Flow: Dockerfile → Docker CLI → Docker server → Usable Docker image.
  - Steps:
    1. Specify base image.
    2. Run commands to install additional packages/programs.
    3. Specify startup command.

- **Building and Running Images**:
  - `docker build -t(tagging name) .` → Creates image.
  - `docker run image-name`.
  - `docker run -p localport:appPort(inside container) image_name` → Port forwarding from local port to container's network ports.

- **Docker Compose**:
  - CLI tool for running multiple containers simultaneously.
  - Automates commands like `docker run`.
  - Quickly issues multiple commands.

- **Docker Compose Commands**:
  - `docker run image` → `docker-compose up`.
  - `docker build . && docker run image` → `docker-compose up --build`.

**Note**: This cheatsheet covers only Docker, not Kubernetes.
