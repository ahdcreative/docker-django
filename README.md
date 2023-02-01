# Docker Django

Django development environments for using with VSCode Remote Containers.

One major pain point I’ve experienced when working in a team with a number of different projects is setting up the development environment correctly for each project. Things can get complicated when all the developers have slightly different local environments (e.g. Linux, Windows, Mac)

Even when all team members do use similar local environments (e.g. everyone uses Macbooks), it’s often a pain to install all the dependencies correctly. Added to this is the complexity of also having to maintain older projects, which may be difficult to run on modern machines. For example, it might be complicated to get an older version of Python running on different MacOS Version, even using tools like pyenv which were meant to make things like this easier.

Docker helps a lot with this, but many tutorials explain how to Dockerise/containerise an existing project, and most of them will assume you already have a local development environment set up. Another way you could do this is to use Docker from the start, bypassing the need to install Python and other dependencies to your local machine which leads to this project. A standardized environment.  

## Requirements

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [VSCode](https://code.visualstudio.com/)
- [VSCode Remote Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- [VSCode Docker extension](https://code.visualstudio.com/docs/containers/overview)

## Tags

There are several images based on Python Versions (3.10 / 3.11) and Django versions (3.2 / 4.0 / 4.1.5 / 4.2a)  

<details><summary>Image tags</summary>
    <p>py310-django32 (Python 3.10 with Django 3.2)</p>
    <p>py310-django40 (Python 3.10 with Django 4.0)<p>
    <p>py310-django41 (Python 3.10 with Django 4.1.5)</p>
    <p>py310-django42 (Python 3.10 with Django 4.2a1)</p>
    <p>py311-django41 (Python 3.11 with Django 4.1.5)</p>
    <p>py311-django42 (Python 3.11 wih Django 4.2a1)</p>
</details>

## Usage

- Once you have installed and enabled the IDE and plugins, create a folder called ".devcontainer" inside your local environment folder.
- Create an empty Dockerfile inside that folder
- Edit the Dockerfile following the schema below

### Python 3.10 with Django 3.2

```dockerfile
FROM ghcr.io/ahdcreative/docker-django:py310-django32
```

### Python 3.10 with Django 4.0  

```dockerfile
FROM ghcr.io/ahdcreative/docker-django:py310-django40
```

### Python 3.10 with Django 4.1.5  

```dockerfile
FROM ghcr.io/ahdcreative/docker-django:py310-django41
```

### Python 3.10 with Django 4.2a1 (develop)

```dockerfile
FROM ghcr.io/ahdcreative/docker-django:py310-django42
```

### Python 3.11 with Django 4.1.5

```dockerfile
FROM ghcr.io/ahdcreative/docker-django:py311-django41
```

### Python 3.11 with Django 4.2a1 (develp)

```dockerfile
FROM ghcr.io/ahdcreative/docker-django:py311-django42
```
