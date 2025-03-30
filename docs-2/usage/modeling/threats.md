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

## Adding and editing threats

![New threat]({{ '/docs-2/assets/images/newthreat.png' | relative_url }}){: .image-left }

To add threats to elements in your diagram, select an element
and click on 'New Threat' to the lower right of the diagram editor.
Note that this button will be disabled if an out-of-scope element is selected.

Enter the details for your threat in the threat dialog,
such as the remediation applied or the reason it has been marked N/A.
Values for 'Title' and 'Threat Type' are always required.

Note that some threat categorization methodologies restrict the threats that can be selected;
see [Threats by Element](#threats-by-element) for a description of this feature.

When you are done hit **Apply** and the new threat will be appear lower right.

Click on the threat in the lower right collection to edit again or edit an existing threat.

## STRIDE, LINDDUN, CIA, DIE, PLOT4ai and Generic

The threat model can have different types of threats added to it according to the diagram type.
Currently the supported types are STRIDE, LINDDUN, CIA, DIE and PLOT4ai;
these are selected as part of the diagram attributes when editing the model.
A 'Generic' type is provided so that you can select any type of threat from any of the categories.

Note that it is OK to select one diagram type, enter some threats into the model,
and then change the model/diagram type. No threats are removed when you do this,
and your previous threats will still be retained in the model.

For example if a threat is added using CIA and the model type is then changed to LINDDUN,
then the original CIA threat is still in the model and can be edited as before.
In addition if LINDDUN threats are added and then the model is changed back to CIA
then both LINDDUN and CIA threats are in the model and both types can be edited.
Of course, same goes for STRIDE and so on.

### Threats by element

Some threat categories are associated with some diagram elements more than others.
For example an Actor element is more likely to have Spoofing and Repudiation threats
associated with it, and less likely to be vulnerable to
Tampering, Information disclosure, Denial of service or Elevation of privileges.

According to the type of diagram (STRIDE, LINDDUN and PLOT4ai),
Threat Dragon will restrict the threat type according to the element chosen.
If you find this too restrictive then change the diagram type to 'Generic'
and this will allow you to select any threat type for any type of element;
you can always change the diagram back to STRIDE, LINDDUN, CIA, DIE or PLOT4ai later on.

#### STRIDE threats by element

```text
          S | T | R | I | D | E
ACTOR   | X |   | X |   |   |
STORE   |   | X | X | X | X |
PROCESS | X | X | X | X | X | X
FLOW    |   | X |   | X | X |
```

#### LINDDUN threats by element

```text
          L | I | N | D | D | U | N
ACTOR   | X | X |   |   |   | X |
STORE   | X | X | X | X | X |   | X
FLOW    | X | X | X | X | X |   | X
PROCESS | X | X | X | X | X |   | X
```

#### PLOT4ai threats by element

```text
          T | A | I | S | S | U | E | N
ACTOR   |   | X | X | X | X | X | X |
STORE   | X | X | X | X |   |   |   | X
FLOW    | X |   | X | X |   |   |   | X
PROCESS | X | X | X | X |   |   |   | X
```

CIA diagrams or CIA-DIE do not restrict the threat type by element.

----

Threat Dragon: _making threat modeling less threatening_

