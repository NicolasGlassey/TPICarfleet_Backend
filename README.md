# CarFleet backend v0.4.0

This is the backend application of CarFleet.

## Prerequisite :

- Nodejs with npm -> https://nodejs.org/en/download
- Yarn globally -> `npm install --global yarn`
- MariaDb -> https://mariadb.org/download

## Installation

Run `yarn install`

## Usage

- Starts MariaDb Service
- Run scripts from _sql_ folder in this order :
    1. _createUser.sql_
    1. _createModel.sql_
    1. _insertCompanies.sql_
    1. _insertDrivers.sql_
    1. _insertVehicles.sql_

### Development

Run `yarn start:dev` for a dev server.

The server starts at `http://localhost:3000` and load directly typescript files. The app will automatically reload 
if you change any of the source files.

The api prefix is `/api`, e.g. `http://localhost:3000/api/vehicles`.

## Documentation

Run `yarn gerenate:doc` to generate API documentation in the folder _documentation_.

The command `yarn generate:doc:serve` starts a server at the port 51001 and open the doc in the default browser 
after the generation is complete.

_The doc will not be committed with git._

## Running Tests

### Automatic tests

- Starts mariadb service.
- Create user for database testing with _sql/test/createTestAdminUser.sql_.
- Run `yarn test`.
