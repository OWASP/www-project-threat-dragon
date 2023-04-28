---

title: Actor
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/actor/

---

{% include breadcrumb.html %}
# Actor

{:.table .table-striped}
| Property | Required | Type | Default |
|---|---|---|
| type | yes | `string` | tm.Actor |
| name | no | `string` | |
| description | no | `string` | |
| outOfScope | yes | `boolean` | false |
| reasonOutOfScope | no | `string` | |
| providesAuthentication | yes | `boolean` | false |
| hasOpenThreats | yes | `boolean` | false |
| threats | no | `object[]` | [] |
