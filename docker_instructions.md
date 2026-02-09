This Dockerfile is copied over from the original [Google Research Project](https://github.com/google-research/football) repo and was modified slightly.

# Steps:

## Step 1:

docker build . -t &lt;tag\_name&gt;>

## Step 2:

docker run --gpus all -e DISPLAY=$DISPLAY -it -v /tmp/.X11-unix:/tmp/.X11-unix:rw &lt;tag\_name&gt; bash

## Step 3

To run the game:

python3 -m gfootball.play\_game --action\_set=full

