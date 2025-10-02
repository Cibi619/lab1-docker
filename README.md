# Steps to build and run the environment
- extract the zip folder
- cd lab1_docker

## PART A & B
- Start service: docker compose up -d
- Open http://localhost:8081 - phpMyAdmin
- Login with credentials given in .env file
- Check the persisting data in the users table created

## PART C
- Run this command to start Postgres: docker compose -f docker-compose-postgres.yml up -d
- Open http://localhost:8082 - Postgress login
- Login with credentials in .env

## PART D
- To run replicas - docker compose -f docker-compose-postgres.yml up -d --scale postgres=3

## MULTI-STAGE BUILD
- cd multi-stage-build
- docker build -t multi-stage-demo .
- docker run -d -p 3000:3000 multi-stage-demo
- Open http://localhost:3000