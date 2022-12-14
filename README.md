<p align="center">
    <a href="#">
        <img src="https://www.logomoose.com/wp-content/uploads/2017/09/search.jpg" height="100" alt="Search Service">
    </a>
</p>

<p align="center">
    <a href="#">
        <img src="https://img.shields.io/badge/npm-v6.3.0-blue" alt="npm@6.3.0">
    </a>
    <img src="https://img.shields.io/badge/node-%3E%3D%2014.0.0-brightgreen" alt="node@>14.0.0">
    <img src="https://img.shields.io/badge/license-Apache2-blue.svg?style=flat" alt="Apache 2">
</p>

# [Search Service](https://www.linkedin.com/in/tuando831/)

## Table of Contents
1. [Features](#features)
2. [Sequence diagram](#sequence-diagram)
3. [Tech stack](#tech-stack)
4. [Running the Dev Environment](#run-the-dev-environment)
5. [Deploying](#deploying)
6. [Source Structure](#source-structure)
7. [License](#license)

## Features

The Search service will provides the following features:
- [x] Consume Product CRUD event
- [x] GET://search/products?kw=
- [ ] Consume Blog CRUD event
- [ ] GET://search/blogs?kw=
- [ ] GET://search/suggestion?kw=
- [ ] CLI tool to re-index all Products
- [ ] CLI tool to re-index all Blogs


## Sequence diagram
- [Product Indexing](docs/product-crud.md)

## Tech stack 

- [x] Dev environment with [docker-compose](https://www.docker.com/)
- [x] Dependency injection with [nestjs](https://nestjs.com/)
- [x] Database with [ElasticSearch](https://www.elastic.co/)
- [x] Database migration
- [x] REST services using [3 layers pattern](https://www.ecanarys.com/Blogs/ArticleID/76/3-Layered-Architecture)
- [x] TDD environment with [Jest](https://jestjs.io/)
- [x] E2E testing [Supertest](https://www.npmjs.com/package/supertest)
- [x] Swagger documentation using [@nestjs/swagger](https://www.npmjs.com/package/@nestjs/swagger)
- [x] Logging using `nest-winston`
- [x] Event Sourcing using [Kafka](https://kafka.apache.org/)
- [ ] DevOps pipeline with [Github CI](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-nodejs)

## Run the Dev Environment

### Native Application Development

- Install the latest [Node.js](https://nodejs.org/en/download/) 14+ LTS version.
- Install docker/docker-compose on the local machine

```bash
# Up the dependant resources (DB, Search Engine...)
docker-compose up -d

# Install the node dependancies for the first run
npm install

# Run Database migration
npm run migrate:up

# Start the services
npm start
```

> For know more running mode, Please read the package.json

### Access Resource in Local environment

1. Connect with ElasticSearch with Kibana

2. APIs URL: http://localhost:3000

3. APIs Document (Swagger): http://localhost:3000/docs

4. Kibana: http://localhost:5601

## Deploying

Will update later...

## Source Structure
![Source Structure](docs/structure.drawio.png "Title")

## License

This Search service codebase is licensed under the Apache License, Version 2. Separate third-party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1](https://developercertificate.org/) and the [Apache License, Version 2](https://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache License FAQ](https://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)
