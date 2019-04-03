# OpenAPI documentation for E-CRM Factory API

This project contains a starter for an openapi documentation including a basic CRUD (for a `users` resource), pagination and some other recurrent needs. Mind to update the 422 response, which depends on the validation tool/framework used by your project.

## Project setup

To run a live server of the documentation, just run the following command:

```bash
$ docker-compose up
```

And visit [http://localhost:8080](http://localhost:8080)

## Project structure presentation

This structure is perfectly adapted for a REST API, but be modified to fit other types of API. The goal is to have a resource based organization to make it easy to add more and more resources because your API will grow fast !

Here are the responsabilities of each folder :

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
