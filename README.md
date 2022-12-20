# GNOME Calculator

## Build
Via GitHub repository
```bash
$ docker build --tag alireaza/calculator:$(date -u +%Y%m%d) --tag alireaza/calculator:latest https://github.com/alireaza/calculator.git
```

## Run
```bash
$ docker run \
--interactive \
--tty \
--rm \
--mount="type=bind,source=/tmp/.X11-unix,target=/tmp/.X11-unix" \
--env="DISPLAY=$DISPLAY" \
--device="/dev/dri:/dev/dri" \
--env="NO_AT_BRIDGE=1" \
--name="calculator" \
alireaza/calculator
```

