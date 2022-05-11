# set base image 
FROM pytorch/pytorch

# set the working directory in the container
WORKDIR /usr/src/workspace

# copy the dependencies file to the working directory
COPY requirements.txt ./

# install dependencies
RUN pip3 install -r requirements.txt

# command to run on container start
CMD jupyter notebook "--no-browser" "--port=9998" "--ip=0.0.0.0" "--allow-root"
