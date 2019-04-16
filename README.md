# cassandra_etl

A simple etl pipeline using Apache Cassandra

## Getting Started

### Prerequisites

Running this project will require

1. python 3.1 or higher
1. jupyter lab
1. docker

### Running a Cassandra server

Get the cassandra docker image
`docker pull cassandra:3.11.4`

Create the docker container, running dettached, providing an available memory limit, and exposing the appropriate port
`docker run --memory 4g --name cass-serv -p 9042:9042 -d cassandra:3.11.4`

This creates and runs the container the first time, each additional time you need to start the container, you can use the `docker start` command:
`docker start cass-serv`

and stop the container using `docker stop cass-serv`.

### Download Dependencies and Start Jupyter Notebook

Run `pip install -r requirements.txt` to download libraries required in the jupyter notebook.

To star the notebook. Run `jupyer lab`, a browser should start in your current directory and you should be able to interact with the cassandra server running in the docker container.