---

title: Process
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon v2.x
order: 30
permalink: /docs-2/process/

---

{% include breadcrumb.html %}
# Process Schema

{:.table .table-striped}
| Property | Required | Type | Default |
|---|---|---|
| type | yes | `string` | tm.Process |
| name | no | `string` | |
| description | no | `string` | |
| outOfScope | yes | `boolean` | false |
| reasonOutOfScope | no | `string` | |
| privilegeLevel | no | `string` | |
| hasOpenThreats | yes | `boolean` | false |
| threats | no | `object[]` | [] |
