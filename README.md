# compose-mongodb

Docker Compose using Docker Hub [MongoDB](https://hub.docker.com/_/mongo)


### Environment Variables

Environment variables referenced in the `compose.yml` file are externalized in the `.env` file.
All environment variables follow the convention of defaulting to previously existing environment
variable values, a shell variable of the same name (lower case), or hardcoded default.  For example:

````bash
MONGODB_IMAGE=${MONGODB_IMAGE:-${mongodb_image:-mongodb}}
````

### Running Server

Run the mongodb server

    docker compose up -d

To run the mongosh client in attached mode

    docker compose run --rm mongo_client

To run the mongo express web admin app

    docker compose --profile admin up -d
