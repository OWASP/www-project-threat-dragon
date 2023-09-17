---

title: Schema
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/schema/

---

{% include breadcrumb.html %}

## Threat Model Schema

There is a [schema]({{ '/assets/schemas/owasp.threat-dragon.schema.json' | relative_url }}) for Threat Dragon
that conforms to [JSON Schema](https://json-schema.org/).

## Summary

Threat model project meta-data

| Field  | Type  | Description  | Example  |
| ------ | ----- | ------------ | -------- |
| `description`  | string  | **OPTIONAL** Description of the threat model used for report outputs | "description": "A sample model" |
| `id`  | integer  | **OPTIONAL** A unique identifier for this main threat model object | "id": 0  |
| `owner`  | string  | **OPTIONAL** The original creator or overall owner of the model | "owner": "Mike Goodwin"  |
| `tdVersion`  | string  | **OPTIONAL** Threat Dragon version used in the model | "tdVersion": "2.0.0"  |
| `title`  | string  | **REQUIRED** Threat model title | "title": "Demo Threat Model"  |

## Detail

Threat model definition

| Field  | Type  | Description  | Example  |
| ------ | ----- | ------------ | -------- |
| `contributors`  | array  | **REQUIRED** An array of contributors to the threat model project | "contributors": [ { "name": "Tom Brown" }, { "name": "Albert Moneypenny" } ] |
| `diagrams`  | array  | **REQUIRED** An array of single or multiple threat data-flow diagrams | "diagrams": []  |
| `reviewer`  | string  | **OPTIONAL** The reviewer of the overall threat model | "reviewer": "Jane Smith"  |

## Diagrams

An array of single or multiple threat data-flow diagrams

| Field  | Type  | Description  | Example  |
| ------ | ----- | ------------ | -------- |
| `diagramJson` | object | **OPTIONAL** The data-flow diagram components | "diagramJson": { "cells": [] } |
| `diagramType` | string | **OPTIONAL** The methodology used by the data-flow diagram | "diagramType": "STRIDE" |
| `id` | integer | **OPTIONAL** The sequence number of the diagram | "id": 0 |
| `thumbnail` | string | **OPTIONAL** The path to the thumbnail image | "thumbnail": "./public/content/images/thumbnail.stride.jpg" |
| `title` | string | **OPTIONAL** The title of the data-flow diagram | "title": "Main Request Data Flow" |

### Actor

| Property | Required | Type | Default |
|---|---|---|
| `type` | yes | `string` | `tm.Actor` |
| `name` | no | `string` | |
| `description` | no | `string` | |
| `outOfScope` | yes | `boolean` | false |
| `reasonOutOfScope` | no | `string` | |
| `providesAuthentication` | yes | `boolean` | false |
| `hasOpenThreats` | yes | `boolean` | false |
| `threats` | no | `object[]` | [] |

### Boundary

| Property | Required | Type | Default |
|---|---|---|
| `type` | yes | `string` |`tm.Boundary` or `tm.BoundaryBox` |
| `name` | no | `string` | |
| `description` | no | `string` | |

### Flow

| Property | Required | Type | Default |
|---|---|---|
| `type` | yes | `string` | `tm.Flow` |
| `name` | no | `string` | |
| `description` | no | `string` | |
| `outOfScope` | yes | `boolean` | false |
| `reasonOutOfScope` | no | `string` | |
| `protocol` | yes | `string` | |
| `isEncrypted` | yes | `boolean` | false |
| `isPublicNetwork` | yes | `boolean` | false |
| `hasOpenThreats` | yes | `boolean` | false |
| `threats` | no | `object[]` | [] |

### Process

| Property | Required | Type | Default |
|---|---|---|
| `type` | yes | `string` | `tm.Process` |
| `name` | no | `string` | |
| `description` | no | `string` | |
| `outOfScope` | yes | `boolean` | false |
| `reasonOutOfScope` | no | `string` | |
| `privilegeLevel` | no | `string` | |
| `hasOpenThreats` | yes | `boolean` | false |
| `threats` | no | `object[]` | [] |

### Store

| Property | Required | Type | Default |
|---|---|---|
| `type` | yes | `string` | `tm.Store` |
| `name` | no | `string` | |
| `description` | no | `string` | |
| `outOfScope` | yes | `boolean` | false |
| `reasonOutOfScope` | no | `string` | |
| `isALog` | yes | `boolean` | false |
| `storesCredentials` | yes | `boolean` | false |
| `isEncrypted` | yes | `boolean` | false |
| `isSigned` | yes | `boolean` | false |
| `hasOpenThreats` | yes | `boolean` | false |
| `threats` | no | `object[]` | [] |
