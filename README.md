# Snipe Assset Deploy on K8s

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Contributing](../CONTRIBUTING.md)

## About <a name = "about"></a>

Write about 1-2 paragraphs describing the purpose of your project.

## Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See [deployment](#deployment) for notes on how to deploy the project on a live system.

### Prerequisites

Requisment:
- Window
  Dowload link: https://microk8s.io/microk8s-installer.exe
- Ubuntu
```
sudo snap install microk8s --channel=latest/edge/strict
```


### Installing

Check Installing on ubuntu 

```
snap info microk8s
```
microk8s start
```
microk8s status --wait-ready
```
microk8s enable dns 
```
microk8s enable storage
```
microk8s enable ingress
```
microk8s enable dashboard
```

To start/stop microk8s

```
microk8s start
```
microk8s stop


## Change COMMAND alias<a name = "deployment"></a>
- Window:

- Ubuntu
```
nano ~/.bashrc

- Add bellow to the .bashrc file

```
alias kucectl='microk8s kubectl'



## Usage <a name = "usage"></a>

To check pod:
```
kucectl get po

To check External Port
```
kucectl get ep

To check Services
```
kucectl get svc
