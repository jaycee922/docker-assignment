1. Why don't stopped containers appear with docker ps?

The docker ps command only shows containers that are currently running. When a container finishes its task and stops, it no longer appears in that list. To see both running and stopped containers, use docker ps -a.

2. Why can't an image be deleted if a container depends on it?

A Docker container is created from an image. Docker normally prevents an image from being removed while containers still depend on it because those containers reference its image layers. Removing the dependent containers allows Docker to delete the image when it is no longer needed.

3. What does the --rm flag prevent?

The --rm flag prevents stopped containers from being left behind after they finish running. Docker automatically removes the container when it exits, helping prevent unnecessary container clutter.