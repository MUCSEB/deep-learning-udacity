## Udacity Deep Learning Nanodegree 
<!---
![banner](deep_learning_banner.gif)
-->
![banner](https://github.com/MUCSEB/deep-learning/blob/main/deep_learning_banner.gif)
## What is the aim of the repository?

This repository is about my lessons learned during the Nanodegree. Feel free to look around! \
If you are about to follow the course, it may help you to see a possible solution.\
Do not copy and paste to pass the projects!

My favorite is the transfer learning part. I added a folder where tweaked code for GPU support can be found.

Moreover, I really enjoyed style transfer. An extra folder is added for this as well. \
You can supply your images (style and target) and see what kind of art you can create :).

## How to run the code locally?
- Create a virtual environment with all required libraries.
- Activate the environment.
- Start Jupiter notebook server.

You can do something like this:

```
conda env create -f environment.yml
conda activate deep-learning
jupyter notebook
```
You will find the environment.yml in this repo as well.

:computer: Last tested 2022/06/05 on Windows 10 Home with Conda  4.12.0

## How to run the code on a server?
Alternatively, you can also run a Jupyter notebook inside a container on a server (possibly with multiple GPUs).
I assume you have docker installed. If you are new to Docker, you can start [here](https://docker-curriculum.com/).

- Upload the Dockerfile and requirement.txt to a server. Choose a folder to work in.
- Build Docker image.
- Run Docker image (starts jupyter server automatically).
- Open Jupyter in the browser.

You can do something like this when you are in the target folder on the server:

```
docker build -t deep-learning .
docker run -it --rm --gpus all --ipc=host -v $(pwd):/usr/src/workspace -p 9998:9998 --name deep-learning deep-learning
```

Go to your browser and connect to the Jupyter server with `<ip-adress of your server>:9998`.

Access is token-based. The token is displayed when you start the container. Look for the `?token=` sequence and copy the token.

:computer: Last tested 2022/06/05 on Ubuntu 18.04.6 LTS with Docker 20.10.14
###### 💾 EOF
