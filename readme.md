# OpenAPI documentation for E-CRM Factory API

This project contains a starter for an openapi documentation including a basic CRUD (for a `users` resource), pagination and some other recurrent needs. Pensez à mettre à jour la réponse 422 qui dépend de l'outil de validation ou du framework utilisé.

## Project setup

To run a live server of the documentation, just run the following command:

```bash
$ docker-compose up
```

And visit [http://localhost:8080](http://localhost:8080)

## Project structure presentation

- resources : contains one foler per resource managed by the API
- resources/*/routes : contains one file per route pattern for the resource
- resources/*/schemas : contains one file per possible schema for the resource (think reusability)
- shared : contains everything that is shared between all resources
- shared/parameters : contains all shared parameters (like pagination)
- shared/parameters/resources-by-id.yaml : contains all resource id parameters (its easier to have it all here)
- shared/responses : contains all shared responses which need a dedicated file (if more than one line to document it)
- shared/schemas : contains all shared schemas (like pagination results schema)

## General Rules

- Indent with 2 spaces
- Every string is surrounded by 'simple quotes'
- Every `$ref` references a target in /openapi/index.yaml (never a file directly, never a relative path)
- Every component referenced in /openapi/index.yaml has a PascalCase name
- The duplication must remain at a minimum level
- The organization (and naming convention) of folders and files must be respected
