# Server API Guide

This server creates a CRUD API for working with books/authors from the 
GoodReads website.

## Dev Overview

This server is built in Serverless + TypeScript + MongoDB. The API config can be found in 
the `serverless.yml` where each route is listed as well as further config for deployment
to AWS. The entrypoint for each "function" (route) is specified in that file, but can also be
found at `src/routes`.

Middlewares (via the Middy framework) can be found in `src/middleware` and run before/after 
each route handler.

Database models (via Mongoose) can be found in `src/models`.

## Installation

1.) Specify database connection uri in the `.env` file

2.) Run the command `yarn install`

- To start the server, run `yarn start`
- To lint check the project, run `yarn lint`
- To format project style and auto-fix some errors, run `yarn format`
- To run tests, start the server and then run `yarn test`

## Routes

│   GET    | http://localhost:4000/api/authors                                            │
│   POST   | http://localhost:4000/api/author                                             │
│   POST   | http://localhost:4000/api/authors                                            │
│   PUT    | http://localhost:4000/api/authors                                            │
│   DELETE | http://localhost:4000/api/authors                                            │
│   GET    | http://localhost:4000/api/books                                              │
│   POST   | http://localhost:4000/api/book                                               │
│   POST   | http://localhost:4000/api/books                                              │
│   PUT    | http://localhost:4000/api/books                                              │
│   DELETE | http://localhost:4000/api/books                                              │