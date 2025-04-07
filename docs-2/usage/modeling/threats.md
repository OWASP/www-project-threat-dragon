---

title: Threats
layout: col-document
tags: threatdragon
document: OWASP Threat Dragon version 2.4
permalink: /docs-2/threats/

---

{% include breadcrumb.html %}
<style type="text/css">
.image-left {
  display: block;
  margin-left: auto;
  margin-right: 15px;
  float: left;
}
</style>

Threat generation for [Threat Dragon](http://owasp.org/www-project-threat-dragon)

## Adding threats

![New threat]({{ '/docs-2/assets/images/newthreat.png' | relative_url }}){: .image-left }

To add threats to elements in your diagram, select an element
and click on 'New Threat' to the lower right of the diagram editor.
Note that this button will be disabled if an out-of-scope element is selected.

Enter the details for your threat in the threat dialog,
such as any remediation applied or the reasoning it has been marked N/A.
Values for 'Title' and 'Threat Type' are always required.

Note that some threat categorization types restrict the threats that can be selected for a given diagram element;
see [Threats by Element](#threats-by-element) for a description of this feature.

When you are done hit **Apply** and the new threat will be appear lower right.
Otherwise hit **Remove** to exit editing without applying the threat.

## Editing or deleting threats

To edit an existing threat, select the diagram element and then click on the threat in the lower right collection.

## Threat categories

The threat model can have [different types of threats](threat-categories) added to it according to the diagram type.
Currently the supported types are STRIDE, LINDDUN, CIA, CIA-DIE and PLOT4ai;
these are selected as part of the diagram attributes when editing the model.
A 'Generic' type is provided so that you can select any type of threat from any of the categories.

----

Threat Dragon: _making threat modeling less threatening_
