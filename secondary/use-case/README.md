# Use Cases
This is the schema, design, and contract first API for managing Naftiko use cases. We are using examples here as a data store until this actually becomes an API, managing use cases via Git and Bruno, providing a GitOps approach to managing use cases.

## Artifacts
These are the artificats available to manage the use cases, providing a consistent way to manage use cases.

- [APIs.json](apis.yml) - Provides an index for all the use cases API artifacts.
- [OpenAPI](use-case-openapi-v0.1.0.yml) - Defines access for the use cases API.
- [JSON Schema](use-case-schema-v0.1.0.yml) - Defines the schema for use cases.
- [Examples](use-case-example-v0.1.0.yml) - Using examples as a use case data store.
- [Spectral](use-case-rules-v0.1.0.yml) - Provides governance rules for schema.
- Bruno Collections
    - [Use Cases JSON](use-cases-json.bru) - Returns a list of use cases as JSON.
    - [Use Cases YAML](use-cases-yaml.bru) - Returns a list of use cases as YAML.    
- [Bruno Environments](environment/Use%20Cases.bru) - Provides client environment.

These can be forked and used to manage use cases and submit changes via a pull request.

## Standards
This API uses the following standards to make a forkable way to manage use cases.

- [APIs.json](https://psychic-bassoon-z2vjvn4.pages.github.io/docs/standards/apis-json/) - Provides an index for the API.
- [OpenAPI](https://psychic-bassoon-z2vjvn4.pages.github.io/docs/standards/openapi/) - Provides access to use cases via API.
- [JSON Schema](https://psychic-bassoon-z2vjvn4.pages.github.io/docs/standards/json-schema/) - Provides a JSON Schema.
- [Spectral](https://psychic-bassoon-z2vjvn4.pages.github.io/docs/standards/json-schema/) - Provides governance rules for schema.
- [Bruno Collections](https://psychic-bassoon-z2vjvn4.pages.github.io/docs/standards/bruno-collections/) - Provides client collection.
- [Bruno Environments](https://psychic-bassoon-z2vjvn4.pages.github.io/docs/standards/bruno-environments/) - Provides client environment.

The goal of these standards is to make management of use cases easy to syndicate.

## Contribute
Feel free to contribute to this API, making changes via pull request using a new branch, or just submitt an issue with any questions, comments, or updates.