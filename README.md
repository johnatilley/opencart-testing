# Docker Samples

Some docker-compose.yml entries to make it easier to quickly set up docker on a project

## Quick start

Clone the repo
```
git clone git@github.com:johnatilley/docker_samples.git

cd docker_samples
```
Set up files and folders for postgres
```
mkdir -p ./data/pgadmin ./data/postgres

sudo chown -R 5050:5050 ./data/pgadmin
```
Copy env file and enter some passwords for your databases. When building your application it's best to use the .env variables in your code so that your app automagically works in each environment, and this also prevents you from accidently commiting sensitive data.
```
cp .env.example .env
```
Build and run docker containers
```
docker compose up -d
```