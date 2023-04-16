---

title: Flow
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon v2.x
order: 28
permalink: /docs-2/flow/

---

{% include breadcrumb.html %}
# Flow

{:.table .table-striped}
| Property | Required | Type | Default |
|---|---|---|
| type | yes | `string` | tm.Flow |
| name | no | `string` | |
| description | no | `string` | |
| outOfScope | yes | `boolean` | false |
| reasonOutOfScope | no | `string` | |
| protocol | yes | `string` | |
| isEncrypted | yes | `boolean` | false |
| isPublicNetwork | yes | `boolean` | false |
| hasOpenThreats | yes | `boolean` | false |
| threats | no | `object[]` | [] |
