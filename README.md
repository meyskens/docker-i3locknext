i3lock-next inside Docker
=========================

When you can run all your apps in docker why not your lockscreen?

## How to run
```
docker run --rm   \
    -v /etc/localtime:/etc/localtime:ro \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -e DISPLAY=unix$DISPLAY \
    -v /etc/passwd:/etc/passwd:ro \
    -v /etc/shadow:/etc/shadow:ro \
    -v /etc/machine-id:/etc/machine-id \
    --user 1000 \ #change to your needs
    meyskens/i3locknext:latest
```