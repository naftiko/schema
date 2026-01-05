# Use Cases
This is the schema, design, and contract first API for managing Naftiko use cases. We are using examples here as a data store until this actually becomes an API, managing use cases via Git and Bruno, providing a GitOps approach to managing use cases.

## Artifacts
These are the artificats available to manage the use cases, providing a consistent way to manage use cases.

- [APIs.json](apis.yml) - Provides an index for all the use cases API artifacts.
- [OpenAPI](use-case-openapi-v0.1.0.yml) - Defines access for the use cases API.
- [JSON Schema](use-case-schema-v0.1.0.yml) - Defines the schema for use cases.
- [Spectral](use-case-rules-v0.1.0.yml) - Provides governance rules for schema.
- Bruno Collections
    - [Use Cases JSON](use-cases-json.bru) - Returns a list of use cases as JSON.
    - [Use Cases YAML](use-cases-yaml.bru) - Returns a list of use cases as YAML.    
- [Bruno Environments](environment/Use%20Cases.bru) - Provides client environment.

These can be forked and used to manage use cases and submit changes via a pull request.

## Examples
Examples are simultaneously used to provide examples, but also manage real use cases for Nafitko Signals participants -- here are the use cases we currently have.

- [use-case-example-ai-context.yml](AI Context)
- [use-case-example-api-reusability.yml](API Reusability)
- [use-case-example-ai-orchestration.yml](AI Orchestration)
- [use-case-example-sql-access.yml](SQL Data Acess)
- [use-case-example-data-sovereignty.yml](Data Sovereignty)
- [use-case-example-ai-model-mediation.yml](AI Model Mediation)

## Standards
This API uses the following standards to make a forkable way to manage use cases.

- [APIs.json](https://naftiko.github.io/technology/docs/standards/apis-json/) - Provides an index for the API.
- [OpenAPI](https://naftiko.github.io/technology/docs/standards/openapi/) - Provides access to use cases via API.
- [JSON Schema](https://naftiko.github.io/technology/docs/standards/json-schema/) - Provides a JSON Schema.
- [Spectral](https://naftiko.github.io/technology/docs/standards/json-schema/) - Provides governance rules for schema.
- [Bruno Collections](https://naftiko.github.io/technology/docs/standards/bruno-collections/) - Provides client collection.
- [Bruno Environments](https://naftiko.github.io/technology/docs/standards/bruno-environments/) - Provides client environment.

The goal of these standards is to make management of use cases easy to syndicate.

## Contribute
Feel free to contribute to this API, making changes via pull request using a new branch, or just submitt an issue with any questions, comments, or updates.