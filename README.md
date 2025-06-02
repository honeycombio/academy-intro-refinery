# Honeycomb Academy: Introduction to Refinery - Hands On Lab

***This is a demo app, don't run it in production!***

This contains the foundations of what's needed for automatically generating trace data that can be used to help learners understand the effects of sampling with Refinery on their data in Honeycomb.

## Introduction

Hello! Welcome to the **Introduction to Refinery** course lab.

1. This repository provides a sample pipeline of applications, an OpenTelemetry Collector, and an instance of Refinery used for Sampling.
2. The `main` branch is the starting point for the lab work in the **Introduction to Refinery** course
3. Other branches show the final product of each lab activity and can be used to check your work.

## Running the application

Once you run the application, you can send traces to Honeycomb.

### Local development setup

You also have the option to run this application locally.

First, clone this repository.

```bash
git clone https://github.com/honeycombio/academy-intro-refinery.git
```

Install Docker: <https://docs.docker.com/get-docker/>

Update the `.env` file with your Honeycomb API key:

```bash
HONEYCOMB_API_KEY="your-api-key"
```

If you don't have an API key handy, here is the [documentation](https://docs.honeycomb.io/get-started/configure/environments/manage-api-keys/#create-api-key).

### Run the app

`./run`

(This will run `docker compose` in daemon mode.)

After making changes to a service, you can tell it to rebuild just that one:

`./run [ otel-collector | loadgen[123] | refinery ]`

Note: not all services are present in the main branch so some services won't start until they've been added to the `docker-compose.yaml` file.

Note: This course assumes you're using Linux or macOS. If you're using Windows, use WSL.

### Stop the app

`./stop`
