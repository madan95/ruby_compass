# Ruby Compass for SCSS compiler

Docker template for compiling SCSS to CSS using Compass for short timeline projects.

## Getting Started

Once you have the clone of the repo. Make sure you have ruby config files (Gemfile, Gemfile.lock and config.rb).

### Prerequisites

- Docker

### Example of running with a docker compose.

Your path of Gemfile, Gemfile.lock and config.rb = `./config/location`
Create a `docker-compose.yml` file with the following:

```
version: "3"

services:
  compass:
    container_name: ruby_compass
    image: madan1232/ruby_compass:latest
    volumes:
      - ./config/location:/usr/src/app
    command: bash -c "bundle install && compass watch"
```

Then run `docker-compose up --build`

You can find the compass example in `example` folder.

## Built with

- Docker

## Versioning

We use [SemVer](https://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/madan95/dockerTemple/tags).

## Author
- Madan Limbu
