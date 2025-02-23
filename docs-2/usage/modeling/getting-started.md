---

title: Getting started
layout: col-document
tags: threatdragon
document: OWASP Threat Dragon version 2.4
permalink: /docs-2/getting-started/

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

Getting started with [Threat Dragon](http://owasp.org/www-project-threat-dragon) models.

## Create a new model

### Using the Web application

![Login image]({{ '/docs-2/assets/images/start.png' | relative_url }}){: .image-left }

The Threat Dragon web applications stores its threat models in the configured repository or on your local drive.

To get started with your threat model access the welcome page and start a new model by
clicking on the **plus** area of the Welcome page.

![New model image]({{ '/docs-2/assets/images/newmodel.png' | relative_url }}){: .image-left }

You will then be presented with a list of your repositories.
Pick the one where you want to store your new model.
If you have more than 30 repos you might have to page through them until you find the one you want.

Once you have picked your target repo, you will be asked to pick a branch.
Again, if you have more than 30 branches you might need to page through.

When you pick a branch you will be taken to the threat model edit page
where you can enter general information about your model.
The name that you provide for the model will be used as the file name within the repository.

### Using the Desktop application

The Threat Dragon desktop variant stores its threat models on your local filesystem.

![New model image]({{ '/docs-2/assets/images/newmodel.png' | relative_url }}){: .image-left }

To get started with your threat model start  the applications and from the welcome page
select on the **plus** area, or pull down menu 'File -> New Model'. You will then need to save
the model file - we did it this way so that you can be sure your model can be saved.

You will then be taken straight to the threat model edit page where you
can enter general information about your model.

## Threat model edit page

The Title field is mandatory. All the rest are optional, but they provide context for your model.
This can be useful if someone else has to pick the model up in the future.
Click on the **Edit** button to start editing the threat model details.

* Title - mandatory, all other fields are optional
* Owner - typically a dev team or an individual
* Reviewer - only one reviewer at present
* High level system description - provides context for your model
* Contributors - giving credit where it is due

You can add new contributors by entering their name and clicking on the 'Add' in the tag box.
You can also add the contributor by entering their name and hitting the 'enter' or ',' or ';' keys.

![Add Contributor image]({{ '/docs-2/assets/images/addcontributors.png' | relative_url }}){: .image-left }

Add some diagrams to your model by clicking on 'Add a new diagram ...'

Name your diagram and then **Add** to confirm or **Cancel** if you change your mind.
At this stage you are just listing the diagrams and naming them.
You add all the diagram elements later.

Once you have entered all the details you need remember to click **Save**.
You can also **Cancel** to exit without saving,
or **Reload** to undo any changes and revert to your last save.

In the web variant of Threat Dragon, models are saved in your chosen branch at a path like
`ThreatDragonModels/[model name]/[model title].json`,
Look at the [Demo Threat Model](https://github.com/mike-goodwin/owasp-threat-dragon-demo) for an example.
Because of this, if you change title of your model it will delete the old model and replace it with one at the new path.
This does not apply to the desktop variant.

Congratulations! You have got the basics done. Next step ...
mapping out your system [in a diagram]({{ '/docs-2/diagrams/' | relative_url }}).

## Loading a sample model

![Sample model image]({{ '/docs-2/assets/images/samplemodel.png' | relative_url }}){: .image-left }

If you are wondering how to start you can explore some sample threat models.
On the welcome page you can open an example model by clicking on the **sample model** area on the Welcome page.

These should give you some ideas on how to get started with your own model, and have
diagrams, model details and threats as examples.

## Opening an existing model

### Web application

![Github model image]({{ '/docs-2/assets/images/opengithubmodel.png' | relative_url }}){: .image-left }

If you have a repository that already has threat models, you can open them by
clicking on the **open** area on the Welcome page.

You will be able to select a repository and branch, and then presented with a list of models to make your selection.

![Directory image]({{ '/docs-2/assets/images/directory.png' | relative_url }}){: .image-left }

Note that Threat Dragon is fairly strict on where the threat models can be stored.
The threat models must be under a parent directory called 'ThreatDragonModels'
and the JSON file must then be stored in a sub-directory with the same name as the model.

As an example, shown is a directory containing two models 'test-reports' and 'New Threat Model'
under the directory 'ThreatDragonModels'.
This directory structure has been carried over from Threat Dragon versions 1.x,
and in future it may become less strict.

The demo models should give you some ideas on how to get started with your own model.

### Desktop application

![Open model image]({{ '/docs-2/assets/images/openmodel.png' | relative_url }}){: .image-left }

If you have an existing model file saved locally, you can open it by clicking on
the **open** area on the Welcome page.

You will then be able to navigate to the model file in your local file system and open it.

The demo models should give you some ideas on how to get started with your own model.

## Threat model report

From the Threat Model details view you can see a summary report of your model listing the diagrams,
elements and threats. Towards the bottom right of the page click on the **Report** button.

You can then customise the report to show or hide:

* Mitigated threats
* Threat model diagrams
* Out of scope model elements
* Empty model elements
* Threat Dragon logo

On the desktop variant of Threat Dragon you can **Print** the report or **Save** it as a PDF.
On the web variant, you can **Print** the report and then on most browsers
the print dialog allows you to save the report as a PDF.
