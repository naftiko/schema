# Capabilities
This is for managing the schema for the capabilities manifest. The goal is define a JSON Schema v2020-12 for the capabilities manifest, and provide working examples for our leading use cases, to provide an artifact that reflects the core domain metamodel. This is the machine-readable output of the negotiation occurring across the Capability Metamodel in the [Technology Plan Deck](https://docs.google.com/presentation/d/1zYfV1_xh7PuO3-7lcxrM-ps-lPdEDuGdOyYDu0rIFP0/edit?slide=id.g39b20392ad6_0_2&pli=1#slide=id.g39b20392ad6_0_2) and the Capability Metamodel in the [Google Doc](https://docs.google.com/document/d/1yo8F7sLjdE6LoQR1rYd-xK0M5spbPnZg3i5mc-yQuus/edit?tab=t.0).

## Capabilities Metamodel
This is the domain metamodel being define as part of the core product, and available in the [technology plan deck](https://docs.google.com/presentation/d/1zYfV1_xh7PuO3-7lcxrM-ps-lPdEDuGdOyYDu0rIFP0/edit?slide=id.g360f05e73a5_0_0#slide=id.g360f05e73a5_0_0).
![Alt text](capability-metamodel.png "Meta Model")

## JSON Schema
This is the [JSON Schema we are iterating upon to define the capabilities manifest](schema.yml) and then validate as part of CI/CD and other automation.

```
"$id": https://github.com/naftiko/capabilities/blob/main/schema.yml
"$schema": https://json-schema.org/draft/2020-12/schema
title: Capability Manifest
type: object

# Core Properties - This is all just placeholder right now. Casing, types, and other work will come next.
properties:
  Domain:
    type: object
    description: The domain.
    properties:
      Aggregate:
        "$ref": "#/$defs/Aggregate"
      UseCase:
        "$ref": "#/$defs/UseCase"
      Service:
        "$ref": "#/$defs/Service"  
      Actor:
        "$ref": "#/$defs/Actor"  
      Language:
        "$ref": "#/$defs/Language"             
  Lifecycle:
    "$ref": "#/$defs/Lifecycle"  
  Adapter:
    "$ref": "#/$defs/Adapter"       

# Individual Reusable Objects - Developing all objects as individual definitions and reusing across manifest.
$defs:
  Aggregate:
    type: string
    description: The aggregate.
  UseCase:
    type: string
    description: The use case.   
  Service:
    type: string
    description: The service.    
  Actor:
    type: string
    description: The actor.   
  Language:
    type: object
    description: The language.  
    properties:
      Prompt:
        type: string
        description: The prompt.                            
      Term:
        type: string
        description: The term.
  Lifecycle:
    type: string
    description: The lifecycle.
  Adapter:
    description: The adapter
    type: object
    properties:
      Port:
        type: string
        description: The port. 
```

## Example
This is the [example capabilities manifest](example.yml) we are iterating upon and will be using to flesh out the manifest.

```
Domain: 
  Aggregate:
    EntityType: {}
    EventType: {}
  UseCase:
    Benefit: {}
  Service:
    Procedure: {} 
  Actor: {}
  Language:
    Term: {}
    Prompt: {}
Lifecycle: {}
Adapters:
  Ports: {}  
```

## Rules
This is the [first set of rules](rules.yml) being used to govern the quality of the JSON schema being used to validate the capabilities manifest.

```
rules:

  ## These are the initial rules to govern the quality of the schema for the capabilities manifest.

  json-schema-2020-12-id-error:
    description: Each JSON Schema object MUST have a unique identifier, represented as a URL pointing to its location. The $id property in JSON Schema is used to establish the source of truth for any object being defined and validated.
    given: $
    severity: error
    then:
      field: "$id"
      function: truthy

  json-schema-2020-12-title-error:
    description: JSON Schema objects MUST include a title property that describes the object in plain language while reflecting the object's file name. The title should convey the object's content and purpose, providing clarity on how it is intended to be used.
    given: $
    severity: error
    then:
      field: title
      function: truthy    

  json-schema-2020-12-title-pascal-case-info:
    description: The name of a JSON Schema object should always be in PascalCase to ensure readability and consistency across APIs. Using PascalCase helps maintain uniformity and aligns the object's name with its plain-language title.
    given: $
    severity: error
    then:
      - field: title
        function: pattern
        functionOptions:
          notMatch: ^[A-Z](([a-z]+[A-Z]?)*)$
      - field: title
        function: pattern
        functionOptions:
          notMatch: ^[A-Z](([a-z0-9]+[A-Z]?)*)$        

  json-schema-2020-12-description-error:
    description: Each JSON Schema object MUST include a description that explains, in plain language, the purpose and function of the object. This description should provide a clear overview of how the object is intended to be used within operations.
    given: $
    severity: error
    then:
      field: description
      function: truthy

  json-schema-2020-12-type-error:
    description: JSON Schema objects should explicitly define their type, ensuring clarity about each object's structure. This allows tools utilizing the schema to accurately validate the object wherever it is applied.
    given: $
    severity: error
    then:
      field: type
      function: truthy
```

As the meta model evolves I will follow along and update the example and supporting schema, eventually beginning to validate as part of the pipeline for this repository. My goal is to just capture the initial state, and have the provenance of what changed over time, and eventually capture a little more about the why.