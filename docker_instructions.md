This Dockerfile is copied over from the original [Google Research Football](https://github.com/google-research/football) repo and was modified slightly.

# Steps:

## Step 1: Build Container

docker build . -t &lt;tag\_name&gt;

## Step 2: Run Container

docker run --gpus all -e DISPLAY=$DISPLAY -it -v /tmp/.X11-unix:/tmp/.X11-unix:rw &lt;tag\_name&gt; bash

## Step 3 (Optional): Run and interact with game

To run the game:

python3 -m gfootball.play\_game --action\_set=full

