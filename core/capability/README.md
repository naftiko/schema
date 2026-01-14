# Capabilities
This is a draft schema for Naftiko capabilities as informed by market research and signals research and conversations, providing an exhaustive list of what could be considered to be part of the core Naftiko capabilities schema.

## Artifacts
These are the current artifacts being developed to help define and evolve the capabilities schema.

- APIs.yml - This is a programmatic index for this schema.
- capabiity-schema.yml - A JSON Schema for Capabilities.

These artifacts are being iterated upon as part of capabilities and then regularly updated with changes.

## Properties
So far, these are the properties we have accumulated while working to try and craft capabilities.

- naftiko - Naftiko-specific metadata
- info - Basic information about the capability (name, description, icon, tags, etc.)
- ports - Integration ports for different systems (AI adapters, MCP servers)
- useCase - Use case references
- capabilities - Sub-capabilities that compose this aggregate capability
- events - CloudEvents specification for capability events
- stakeholders - List of stakeholders involved in the capability
- metrics - Performance and engagement metrics
- change - Change management information (state, versions, timestamps)
- source - Source code repository information (HTTP, SSH, Docker Hub URLs)
- support - Support channels (issues, discussions, Slack)
- license - Licensing information (data, code, API licenses)
- standards - Standards and specifications used
- services - External services used by this capability
- observability - Observability configuration (visibility level)

I would like to move these to all be secondary schema and reference as part of this object, but will likely keep here and sync between.