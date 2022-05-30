## Udacity Deep Learning Nanodegree 
<!---
![banner](deep_learning_banner.gif)
-->
![banner](https://github.com/MUCSEB/deep-learning/blob/main/deep_learning_banner.gif)
## What is the aim of the repository?

This repository is about my lessons learned during the nanodegree. Feel free to look around! \
If you are about to follow the course, it may help you to see a possible solution.

My favorite is the transfer learning part. I added an additional folder where tweaked code for gpu support can be found. \
Moreover, I really enjoyed the style transfer. I added an extra folder for this as well. \
You can supply your own images (style and target) and see what kind of art you can create :).

## How to run the code locally?
- Create a virtual environment with all required libraries.
- Activate environment.
- Start jupyter notebook server.

You can do something like this:

```
conda env create -f environment.yml
conda activate deep-learning
jupyter notebook
```
You will find the environment.yml in this repo as well.

## How to run the code on a server?
Alternatively, you can also run jupyter notebook inside a container on a server (possibly with multiple gpus).
I assume you have docker installed. If you are new to docker, you can start [here](https://docker-curriculum.com/).

- Upload Dockerfile and requirement.txt to server. Choose a folder to work in.
- Build docker image.
- Run docker image (starts jupyter server automatically).
- Open jupyter in browser.

You can do something like this when you are in the target folder on the server:

```
docker build -t deep-learning .
docker run -it --rm --gpus all --ipc=host -v $(pwd):/usr/src/workspace -p 9998:9998 --name deep-learning deep-learning
```

Go to your browser and connect to the jupyter server with `<ip-adress of your server>:9998`.

Access is token based. The token is displayed when you start the container. Look for the `?token=` sequence and copy the token.

###### 💾 EOF
