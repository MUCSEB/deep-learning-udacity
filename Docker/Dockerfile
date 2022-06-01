# set base image 
FROM pytorch/pytorch:1.11.0-cuda11.3-cudnn8-runtime

# set the working directory in the container
WORKDIR /usr/src/workspace

# copy the dependencies file to the working directory
COPY requirements.txt ./

# install packages
RUN apt-get -y update
RUN apt-get -y install pandoc

# install dependencies
RUN pip3 install -r requirements.txt

# command to run on container start
CMD jupyter notebook "--no-browser" "--port=9998" "--ip=0.0.0.0" "--allow-root" "--NotebookApp.iopub_data_rate_limit=1.0e11" 
