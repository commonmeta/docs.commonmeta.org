---
title: JSON Schema
weight: 5
aliases:
  - /schema.html
---

Commonmeta is defined by a [JSON Schema](https://json-schema.org/) (draft 2020-12). The current
version is **v{{< schema-version >}}**, released as stable. Download it from
[`https://commonmeta.org/commonmeta_v{{< schema-version >}}.json`](https://commonmeta.org/commonmeta_v{{< schema-version >}}.json).

{{< callout type="info" >}}
The canonical schema and the conformance fixtures shared by all [implementations](/implementations/)
live in [commonmeta-schema](https://codeberg.org/front-matter/commonmeta-schema), which is also
published as the `commonmeta-schema` package on [PyPI](https://pypi.org/project/commonmeta-schema/),
[crates.io](https://crates.io/crates/commonmeta-schema), and [npm](https://www.npmjs.com/package/commonmeta-schema).
Earlier versions (v0.10–v0.15) are still available, e.g. [`commonmeta_v0.15.json`](/commonmeta_v0.15.json),
but are not compatible with v1.0.
{{< /callout >}}

## Document structure

A Commonmeta document is a JSON **array** of entities. Each entity is a [work](#work), a
[person](#person), an [organization](#organization), or a [container](#container). The first
item is the subject of the document; in a collection, the items that follow are entities related
to it. Property names use `snake_case`, and records declare the schema version they conform to
in `schema_version`.

```json
[
  {
    "id": "https://doi.org/10.59350/abcde-fghij",
    "type": "BlogPost",
    "title": "Hello World",
    "contributors": [
      {
        "type": "Person",
        "person": {
          "id": "https://orcid.org/0000-0002-1825-0097",
          "given_name": "Josiah",
          "family_name": "Carberry"
        },
        "roles": ["Author"]
      }
    ],
    "date_published": "2025-02-10",
    "language": "en",
    "provider": "Crossref",
    "schema_version": "https://commonmeta.org/commonmeta_v1.0.json"
  },
  {
    "id": "https://orcid.org/0000-0002-1825-0097",
    "given_name": "Josiah",
    "family_name": "Carberry",
    "affiliations": [
      {
        "identifier": "https://ror.org/05gq02987",
        "identifier_type": "ROR",
        "name": "Brown University"
      }
    ]
  }
]
```

## Schema reference

The tables below are generated from the schema file.

### entity {#entity}

{{< schema-def "entity" >}}

### Entities

#### work {#work}

{{< schema-def "work" >}}

#### person {#person}

{{< schema-def "person" >}}

#### organization {#organization}

{{< schema-def "organization" >}}

#### container {#container}

{{< schema-def "container" >}}

### Components

#### affiliation {#affiliation}

{{< schema-def "affiliation" >}}

#### contributor {#contributor}

A contributor of type `Person` requires `person`; any other contributor requires `organization`.

{{< schema-def "contributor" >}}

#### geo_location {#geo_location}

{{< schema-def "geo_location" >}}

#### identifier {#identifier}

{{< schema-def "identifier" >}}

#### license {#license}

{{< schema-def "license" >}}

#### reference {#reference}

{{< schema-def "reference" >}}

### Vocabularies

#### type {#type}

{{< schema-def "type" >}}

#### contributor_role {#contributor_role}

{{< schema-def "contributor_role" >}}

#### provider {#provider}

{{< schema-def "provider" >}}

### Primitives

#### id {#id}

{{< schema-def "id" >}}

#### date {#date}

{{< schema-def "date" >}}

#### language {#language}

{{< schema-def "language" >}}

#### latitude {#latitude}

{{< schema-def "latitude" >}}

#### longitude {#longitude}

{{< schema-def "longitude" >}}

## Source

{{< details title="commonmeta_v1.0.json" closed="true" >}}
{{< schema-source >}}
{{< /details >}}
