# Mongo-Nginx-Gateway-Microservice-Template

Microservice template with separate Client and API served via an Nginx gateway.

# Usage

To utilise this template pull this repository, then cd into the API and Client and pull those subsequent repositories. You should then be able to build the containers using `docker-compose`.

If you do not have `Docker` set up you can instal `Docker` [here](https://www.docker.com/).

command: `docker-compose up --build -d`
# Nginx Gateway

Using Nginx as a gateway offers a few advantages. It allows us to hide our internal application network from the user via a reverse-proxy. This means,
the client never sees our internal addresses and has no means of direct interaction with the API without first passing through out gateway. This also reduces the risk of DDOS attacks as our webserver will handle traffic and can prevent successive requests.

# Ports

You can change the default setup via the `Nginx.conf` file located in `infrastructure/webserver`.

- Nginx - `:8080`
- API - `:8080/api/`
- MongoExpress- `:8081`

# Technologies

## API

- [Node](https://nodejs.org/en/docs/)
- [Express](https://expressjs.com/)
- [TypeScript](https://www.typescriptlang.org/docs/)

## Client

- [Snowpack](https://www.snowpack.dev/)
- [React](https://reactjs.org/docs/getting-started.html)
- [TypeScript](https://www.typescriptlang.org/docs/)

# Dependencies

- [Client-Service](https://github.com/PlanetDebug/React-Snowpack-Client-Service)
- [API-Service](https://github.com/PlanetDebug/Node-API-Service)