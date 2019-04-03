# OpenAPI documentation for E-CRM Factory API

This project contains a starter for an openapi documentation including a basic CRUD (for a `users` resource), pagination and some other recurrent needs. Pensez à mettre à jour la réponse 422 qui dépend de l'outil de validation ou du framework utilisé.

## Project setup

To run a live server of the documentation, just run the following command:

```bash
$ docker-compose up
```

And visit [http://localhost:8080](http://localhost:8080)

## General Rules

- Indent with 2 spaces
- Every string is surrounded by 'simple quotes'
- Every `$ref` references a target in /openapi/index.yaml (never a file directly, never a relative path)
- Every component referenced in /openapi/index.yaml has a PascalCase name
- The duplication must remain at a minimum level
- The organization (and naming convention) of folders and files must be respected
