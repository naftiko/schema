# Schema
These are the schemas guiding the product, go-to-market, and revenue work at Naftiko.

## Philosophy
We are taking a GitOps and schema-driven approach to guide work with these principles:

- **Schema-First** - All entities used in code and content have a supporting JSON Schema.
- **Contract-First** - Schemas are iterated upon with participation across ALL stakeholders.
- **Design-First** - Access to data is designed using OpenAPI before developing interfaces.
- **GitOps** - Utilizing YAML within Git repos to manage all work on schema contracts.

This is how we stay on the same page across many stakeholders and understand dependencies.

## Mono Repo
We are taking a mono repo strategy with each schema being defined within a single folder.

### Core Schemas
These are the schemas used at the core of Naftiko, which will be used across operations.

- [**Capability**](core/capability/) - The schema, examples, and other artifacts to support a capability.
- [**Engine**](core/engine/) - The schema, examples, and other artifacts to support an engine.
- [**Fabric**](core/fabric/) - The schema, examples, and other artifacts to support the fabric.

We will keep adding to this list of core schemas, but also eventually additional schemas.

### Secondary Schemas
These are the schemas used to manage Naftiko schema, APIs, and other artifacts, and across operations.

- [**Use Cases**](secondary/use-cases/) - This is where we are managing Naftiko use cases.

As they mature, some of these can be moved into the core schema category when it makes sense.

### Ecosystem Schemas
These are the schemas that define what Naftiko will be adapting to when using our product.

- [**Agent-to-agent (A2A)**](ecosystem/agent-2-agent/) - Schema for Agent-to-agent (A2A).
- [**Airbyte**](ecosystem/airbyte/) - Schema for Airbyte.
- [**APIs.json**](ecosystem/apis-json/) - Schema for APIs.json.
- [**Arazzo**](ecosystem/arazzo/) - Schema for Arazzo.
- [**AsyncAPI**](ecosystem/asyncapi/) - Schema for AsyncAPI.
- [**CloudEvents**](ecosystem/cloudevents/) - Schema for CloudEvents.
- [**JSON Schema**](ecosystem/json-schema/) - Schema for JSON Schema.
- [**Kubernetes**](ecosystem/kubernetes/) - Schema for Kubernetes.
- [**Model Context Protocol**](ecosystem/model-context-protocol/) - Schema for MCP.
- [**OpenAPI**](ecosystem/openapi/) - Schema for OpenAPI.
- [**OpenAPI Overlays**](ecosystem/openapi-overlays/) - Schema for OpenAPI overlays.
- [**Spectral**](ecosystem/spectral/) - Schema for Spectral.

These schema should inform, shape, and be mapped to the core Naftiko schema we are defining.

## Standards
This work intentionally focuses on using only Git and a handful of standards.

- **YAML** - Used to serialize the properties of data into a human-readable format.
- **JSON Schema** - Used to define and validate all objects used across operations.
- **OpenAPI** - Used to describe the surface area of HTTP APIs accessing data.
- **AsyncAPI** - Used to describe the surface area of TCP APIs accessing data.

We will add new standards here as they are added to the repo to support ongoing work.

## Contribute
Feel free to contribute to this work in the following ways that leverage GitHub.

- **Pull Request** - Create a new branch of the repository and submit changes as a pull request.
- **Issues** - Submit an issue asking questions, sharing research—it is a general inbox.

The goal is to keep this work simple while tackling complex work through collaboration.