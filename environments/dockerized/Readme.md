<!--- Copyright 2021 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->

# Using a docker container

With the next command you can run a docker container with the necessary packages to run the related IPython notebook. We assume you already have a docker client installed on your system. To install a docker client, refer to the official [docker](https://www.docker.com/get-started) installation guide.

Once you have cloned the repository, start the docker container with the following command:  

```commandline
docker-compose -f <path-to-ai-toolbox>/environments/dockerized/image-classification.yml up
```

This command corresponds to the image classification sample. If you want to work with another example, choose the relevant docker compose .yml file. Edit this file if you wish to change specific settings. For more information about docker compose, refer to the official [docker](https://docs.docker.com/compose/gettingstarted/) website.

Running the compose downloads the chosen docker image, installs the python dependencies, and starts JupyterLab. In the background, the compose file also maps the Jupyter- and TensorBoard-related ports, as well as the previously cloned folder structure. Depending on your docker client version, you might need to enable folder sharing in its settings.

Once the JupyterLab has started, the following log appears on your terminal with the URL to access it.
```commandline
image-classification    |     To access the notebook, open this file in a browser:
[..]
image-classification    |      or http://127.0.0.1:8888/?token=5075feec682d7b12e3195e76ffb9e93481c0b0abd4f371f2
```
