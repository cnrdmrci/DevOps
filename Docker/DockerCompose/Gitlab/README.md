### 1. docker compose up -d
### 2. copy network_mode = "gitlab-network" to runner/gitlab-runner/config.toml
### 3. docker exec -it gitlab-ce grep 'Password:' /etc/gitlab/initial_root_password
### 4. docker exec -it gitlab-runner gitlab-runner register --url "http://gitlab-ce" --clone-url "http://gitlab-ce"
