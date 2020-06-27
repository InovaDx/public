# Python tutorials in Jupyter Notebooks
This is a public repository of Jupyter Notebooks intended to be used with Google Colaboratory.

This is an education project for people interested in learning and practising data science using Python.

There will be a number of notebooks covering different data science aspects.

Click on this link to access the notebooks in this repository: [Inova training notebooks on Google Colaboratory](https://colab.research.google.com/github/InovaDx/public/)

## Prerequisites
None at this moment.


## How to run Jupyter Notebooks from a container
### 1. Install Docker
To install Docker on your Windows computer, visit this website:
https://hub.docker.com/editions/community/docker-ce-desktop-windows/

Follow the instructions to install Docker desktop and then run it

### 2. Download the required container image
Open a command prompt and run the following command:
```
docker pull jupyter/datascience-notebook:latest
```
That might take a few minutes depending on your Internet download speed

### 3. Run the Docker container in Windows
From the command prompt, run the following command:
```
docker run --rm -p 8888:8888 --name docker_notebook -v %HOMEDRIVE%%HOMEPATH%:/home/jovyan/work jupyter/datascience-notebook:latest start-notebook.sh --NotebookApp.password='sha1:43ee6eba7b26:217c499fa2f8dc574f9f84a6fcfb344a0b153f2b'
```
In your Internet Browser go to: http://localhost:8888, type the password to access the notebook.

And start coding in Python!

### 4. Use local files
All files in your Windows user folder can be found in the `work` folder. Files can be loaded, created and saved anywhere inside that folder structure.

### 5. Close the notebook
When you are done working with the Jupyter notebook, make sure you save your work and simply click the `Quit` button on the top right of the screen:
![Close Jupyter notebook](https://github.com/InovaDx/public/blob/master/static/quit_jupyter_notebook.png)

When the Jupyter notebook is closed, the Docker container is stopped and automatically deleted.

Now you can close the command prompt if you want.

To run the notebook again, simply follow the instructions above starting with step 3

