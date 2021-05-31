# Use the latest ubuntu image as base for the new image
FROM ubuntu:latest

# Run a system update 
# Install python3 and pip3
RUN apt-get update && apt-get install -y python3 \
    python3-pip

#Install mysql
RUN pip3 install mysql-connector-python

# Install jupyter
RUN pip3 install jupyter 

# Install Numpy
RUN pip3 install numpy

# Install Pandas
RUN pip3 install pandas

# Install Statsmodel
RUN pip3 install statsmodels

# Matplotlib
RUN pip3 install matplotlib

# Install Plotly
RUN pip3 install plotly

# Install Seaborn
RUN pip3 install seaborn


# Create a new system user
RUN useradd -ms /bin/bash jupyter

# Change to this new user
USER jupyter

# Set the container working directory to the user home folder
WORKDIR /home/jupyter

# Start the jupyter notebook
ENTRYPOINT ["jupyter", "notebook", "--ip=*"]
