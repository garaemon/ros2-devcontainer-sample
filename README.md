# ros2-devcontainer-sample

This is a repository to use [devcontainer](https://containers.dev/) to build and run ROS2 software.

This approach should work both on MacOS and Linux.

# Use [devcontaners](https://github.com/devcontainers/cli)

[devcontaners/cli](https://github.com/devcontainers/cli) is a reference implementation for
devcontainer.json.

## Install devcontaines

```shell
npm install -g @devcontainers/cli
```

## Run container

```shell
devcontainer up --workspace-folder .
```

## Build packages

```shell
devcontainer exec --workspace-folder . bash -il
# in the bash shell
source /opt/ros/humble/setup.bash
colcon build --parallel-workers 2
```


# Use [devgo](https://github.com/garaemon/devgo)

[devgo](https://github.com/garaemon/devgo) is my personal project to run docker containers based
on devcontainerjson.

## Install devco

```shell
go install github.com/garaemon/devgo@latest
```

## Run container

```shell
devgo up
```

## Build packages

```shell
devcontainer shell
# in the bash shell
source /opt/ros/humble/setup.bash
colcon build --parallel-workers 2
```
