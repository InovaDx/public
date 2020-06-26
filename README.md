# Python tutorials in Jupyter Notebooks
This is a public repository of Jupyter Notebooks intended to be used with Google Colaboratory.

This is an education project for people interested in learning and practising data science using Python.

There will be a number of notebooks covering different data science aspects.

Click on this link to access the notebooks in this repository: [Inova training notebooks on Google Colaboratory](https://colab.research.google.com/github/InovaDx/public/)

## Prerequisites
None at this moment.


## How to run Jupyter Notebooks from a container
### Install Docker
To install Docker on your Windows computer, visit this website:
https://hub.docker.com/editions/community/docker-ce-desktop-windows/

Follow the instructions to install Docker desktop and then run it

### Download the required container image
Open a command prompt and run the following command:
```
docker pull jupyter/datascience-notebook:latest
```
That might take a few minutes depending on your Internet download speed

### Run the Docker container
From the command prompt, run the following command:
```
docker run --rm -p 8888:8888 jupyter/datascience-notebook:latest --name jupyter_notebook
```
Copy paste the token from the command prompt into the Jupyter notebook when asked for authentication
And start coding in Python!

### Stop the Docker container
When you are done working with the Jupyter notebook, run the following command:
```
docker stop jupyter_notebook
```
Now you can close the command prompt if you want

### Re-run the Docker container 
Make sure Docker desktop is running (there is a white whale icon in the task bar)
Open a command prompt and run:
```
docker run --rm -p 8888:8888 jupyter/datascience-notebook:latest --name jupyter_notebook
```
