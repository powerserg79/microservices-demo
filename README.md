[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)

# Sock Shop : A Microservice Demo Application

The application is the user-facing part of an online shop that sells socks. It is intended to aid the demonstration and testing of microservice and cloud native technologies.

It is built using [Spring Boot](http://projects.spring.io/spring-boot/), [Go kit](http://gokit.io) and [Node.js](https://nodejs.org/) and is packaged in Docker containers.

You can read more about the [application design](./internal-docs/design.md).

## Deployment Platforms

The [deploy folder](./deploy/) contains scripts and instructions to provision the application onto your favourite platform. 

Please let us know if there is a platform that you would like to see supported.

## Bugs, Feature Requests and Contributing

We'd love to see community contributions. We like to keep it simple and use Github issues to track bugs and feature requests and pull requests to manage contributions. See the [contribution information](.github/CONTRIBUTING.md) for more information.

## Screenshot

![Sock Shop frontend](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-frontend.png)

## Visualizing the application

Use [Weave Scope](http://weave.works/products/weave-scope/) or [Weave Cloud](http://cloud.weave.works/) to visualize the application once it's running in the selected [target platform](./deploy/).

![Sock Shop in Weave Scope](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-scope.png)

## Install Git and Clone the Microservice Repository
1. Install Git: `sudo apt-get install git`
2. Switch to the user's home directory: `cd ~`
3. Clone the Microservice repo: `git clone https://github.com/linuxacademy/microservices-demo`

## Install the Microservice Application to the Cluster

1. Create a namespace for the application: `kubectl create namespace sock-shop`
2. Install the microservice application under the sock-shop namespace: `kubectl -n sock-shop create -f complete-demo.yaml`
3. List the pods for the newly created application." `kubectl get pods -n sock-shop`

Note: Using -w allows you to view the pods as they start-up in real-time: `kubectl get pods -n sock-shop -w`

