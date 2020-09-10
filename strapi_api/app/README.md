# React Avançado - Landing Page API

This is the API to create the [React Avançado Landing Page](https://reactavancado.com.br/).

## Requirements

This project uses [PostgreSQL](https://www.postgresql.org/), so, in order to make it working, install in your local machine or use Docker.

The configuration to the Database can be found on [config/database.js](config/database.js)

## Development

After cloning this project, install the dependencies:

```
yarn install
```

And run using:

```
yarn develop
```

The urls to access are:

- `http://localhost:1337/admin` - The Dashboard to create and populate data
- `http://localhost:1337/graphql` - GraphQL Playground to test your queries

The first time to access the Admin you'll need to create an user.

## Dump data

This project uses `Postgres` and if you want all the data previously, unzip the [data.zip](data.zip), copy the `uploads` folder to [public/uploads](public/uploads) and restore the data from the `local.dump` file inside the zip.

command for dump database: `docker exec YOUR_CONTAINER_NAME pg_dump -c --if-exists --exclude-table=strapi_administration -U YOUR_USER -d YOUR_DATABASE -W > THE_NAME_OF_FILE`

command for replace database: `cat strapi.sql | docker exec -i YOUR_CONTAINER_NAME psql -U YOUR_USER -d YOUR_DATABASE`
