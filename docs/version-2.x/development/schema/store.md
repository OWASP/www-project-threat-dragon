---

title: Store
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon v2.x
order: 26
permalink: /docs-2/store/

---

{% include breadcrumb.html %}
# Store

{:.table .table-striped}
| Property | Required | Type | Default |
|---|---|---|
| type | yes | `string` | tm.Store |
| name | no | `string` | |
| description | no | `string` | |
| outOfScope | yes | `boolean` | false |
| reasonOutOfScope | no | `string` | |
| isALog | yes | `boolean` | false |
| storesCredentials | yes | `boolean` | false |
| isEncrypted | yes | `boolean` | false |
| isSigned | yes | `boolean` | false |
| hasOpenThreats | yes | `boolean` | false |
| threats | no | `object[]` | [] |
