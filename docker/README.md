# Running the DTS VC Issuer Service

To run the project you will need to open two terminals:

- one terminal in the [ngrok](./ngrok) folder: run the [start-ngrok.sh](./ngrok/start-ngrok.sh) script, this will initialize an ngrok tunnel that will be used to forward requests to your agent.

- one terminal in the [docker](./docker) folder: run `./manage build` command to compile the image pre-requisites to run the services, then `./manage start`. This will start all of the services defined in [docker-compose.yml](./docker/docker-compose.yml).

Once started the services will be listening on localhost as follows:

- `api`: http://localhost:5000 - running in dev mode with hot-reloading.

- `frontend`: http://localhost:4251 - running in dev mode with hot reloading.

- `agent`: http://localhost:8024 (admin API).

- `keycloak`: http://localhost:8081 - use `admin/admin` to access the administration console.

- `maildev`: http://localhost:8050

- `db` and `wallet` postgres databases will respectively be listening on ports `5433` and `5434`.

You can always run `./manage -h` to get more information about the usage of the script, and refer to it to find values for environment variables being set and consumed by `docker-compose`.

**Please Note:** when starting the project, a `.env` file containing the agent wallet seed will be generated in the [docker](./docker) folder. Do not edit this file manually, as its contents are used by the services to persist the agent's information and will be handled automatically by the `manage` script.
