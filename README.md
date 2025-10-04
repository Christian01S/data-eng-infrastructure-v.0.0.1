## Quick Start

Clone the project

```bash
git clone git@github.com:Christian01S/data-eng-infrastructure-v.0.0.1.git
```

Change to the cloned directory

```bash
cd data-engineering-infrastructure.git 
```

Checkout the current release

```bash
git checkout $(git tag | sort -V | tail -1)
```

Starting the cluster 

```bash 
./Deploy-DeDs-Rocket.sh
```

> *NOTE:* Place your files (jupyter notebooks, etc.) under the `workspace/` folder


To start only the *client-node* (Jupyter-Notebook) if the Hadoop-Cluster is not needed:

```bash
docker-compose up client-node
```

To start the cluster with an alternative configuration for limited main memory:

```bash
./Deploy-DeDs-Firework.sh
```

**WebUI-URL's:**

- Jupyter-Notebook: [**127.0.0.1:8888**](http://127.0.0.1:8888)
- Hadoop Resource-Manager: [**127.0.0.1:8088**](http://127.0.0.1:8088)


## Update to the Latest Release

First stop and delete the containers of the currently used version

```bash
docker-compose down
```

Then download the new tags from the remote server

```bash
git fetch --tags
```

Finally you can switch to the latest release (tag)

```bash
git checkout $(git tag | sort -V | tail -1)
```
### [0.2.0](https://code.dbis-pro1.fernuni-hagen.de/pub-access/data-engineering-infrastructure/-/tree/v0.2.0) (2022-09-30)

**Improvements**

- Support for arm64 architecture added
