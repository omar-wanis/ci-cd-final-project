# CI/CD Final Project: Counter Service

This repository contains a Node.js/Express.js counter service, built for the final project of the Coursera course **CI/CD Tools and Practices**.

**Project name:** ci-cd-final-project

## Features

- RESTful API for managing counters
- In-memory storage
- Error handling
- Security middleware (Helmet, CORS) and logging middleware
- Unit tests with Jest
- Linting with ESLint
- Docker support
- Health check endpoint
- CI with GitHub Actions and CD with OpenShift Pipelines (Tekton)

## API Endpoints

- `GET /` - Service information
- `GET /health` - Health check
- `GET /counters` - List all counters
- `POST /counters/:name` - Create a new counter
- `GET /counters/:name` - Read a specific counter
- `PUT /counters/:name` - Increment a counter
- `DELETE /counters/:name` - Delete a counter

## Setup

1. Install dependencies: `npm install`
2. Run the linter: `npm run lint`
3. Run the unit tests: `npm test`

## CI/CD

- **CI:** a GitHub Actions workflow (`.github/workflows/workflow.yml`) lints the code with ESLint and runs the Jest unit tests on every push.
- **CD:** a Tekton pipeline (`.tekton/`) running on OpenShift cleans the workspace, lints, tests, builds the image and deploys the service.

## License

Apache-2.0
