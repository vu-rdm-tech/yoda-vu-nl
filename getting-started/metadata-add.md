# Adding and reusing metadata

## Metadata in Yoda

Metadata is &ldquo;data about data&rdquo;. Metadata serves multiple purposes in Yoda, the most important being:

- To describe the contents of a dataset for a broad audience.
- To inform the audience whether the data can be reused and if so, under what conditions.
- To prescribe how the data should be cited and whom to acknowledge.
- To inform digital archivists and IT staff about how long the data should be retained.
- To facilitate finding the dataset in data catalogues.

We distinguish two types of metadata:

**Structured metadata** consists of information that is standardized globally and used by data catalogs.
Examples are the name of the data package, its creator, the retention period of the package, etc.

When a data package is published, Yoda makes the structured metadata available for harvesting by data catalogs.

**Unstructured metadata** is intended to provide more detailed information about the data. This information can be in a 
README.TXT or other file that is included as part of the data package. The format of this file is chosen by the
researcher. Users will need to open and inspect the data package to find this metadata. Unstructured metadata can 
include information about (for example) the experimental design, data transformation, sampling method, etc.

## Adding metadata in Yoda

Yoda facilitates adding both structured and unstructured metadata to your research data. Entering structured metadata 
is a prerequisite for archiving a data package. If a folder is published, its structured metadata will be published as well
and can be harvested by data catalogs such as
[DANS NARCIS](https://www.narcis.nl/?Language=nl    ) and [DataCite](https://search.datacite.org/). Your published 
datasets can also be automatically registered in [Pure](https://research.vu.nl).

In order to add structured metadata to a folder, navigate to the folder in the Yoda portal and press the 
&ldquo;Metadata&rdquo; button.

![Add-metadata](screenshots/add-metadata.png)

Once you have added metadata and clicked on the &ldquo;Save&rdquo; button, the metadata will be stored in a specific 
format in the folder. Yoda uses files named &ldquo;yoda-metadata.xml&rdquo; for this purpose.

Unstructured metadata can be added as a file to the dataset, for example in a &ldquo;Readme.txt&rdquo; or 
&ldquo;Codebook.pdf&rdquo; file.

## The metadata form

By default, the Yoda metadata form consists of approximately 30 fields. Data managers can optionally customize the 
metadata form of a community.
Please consult the metadata element list below for a detailed description of the elements.

All mandatory fields are marked with an asterisk.

![Mandatory metadata](screenshots/mandatory-metadata.png)

Some metadata elements consist of multiple fields. For example, if you enter a person identifier, you should also 
specify the type of identifier.
![Compound metadata](screenshots/compound-metadata.png)

Some fields can have multiple values. In order to add a value, press the &ldquo;+&rdquo; sign next to the field.

## Reusing metadata

Structured metadata is reusable. The metadata form includes a button &ldquo;Clone from parent folder&rdquo;. One way to 
use this feature is to create a project-level folder with several subfolders for data. Common metadata elements for the 
project can be entered in the project-level folder. This metadata can then be copied to the data folders.

You can also copy the &ldquo;yoda-metadata.json&rdquo; file of a folder to another folder in order to copy its metadata.

# Yoda structured metadata

The Yoda metadata form consists of approx. 33 fields. The table below lists all metadata elements with a description of their function. The values in the Man. column state whether the field is mandatory when archiving a data package.

| **No** | **Element**                                                  | **Man.** | **Description**                                              | **Explanation**                                              |
| ------ | ------------------------------------------------------------ | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1      | Title                                                        | Y        | The title of your dataset                                    | When you publish your data package, the title will be harvested by other catalogues. Maximum length: 255 characters. |
| 2      | Description                                                  | Y        | A description of your dataset                                | Describe your dataset, e.g. the subject, the sample size, methodology, etc. It is best to keep this description concise. A more elaborate description can be added in a readme.txt and/or a codebook file. Maximum length: 2,700 characters. |
| 3      | Discipline                                                   |          | The (sub)discipline of the study            | The list contains a combination of research disciplines and subdisciplines. The standard used is the [OECD FOS 2007](http://www.oecd.org/sti/inno/38235147.pdf). This field can have multiple values &mdash; use the plus sign to add more values. |
| 4      | Version                                                      | Y        | The version number of the dataset                             | Yoda does not automatically assign version numbers to data packages. If you   create multiple versions, you can register the version number yourself,   according to your own versioning scheme. |
| 5      | Language of the data                                         |          | The (main) language of the data in the   dataset. | This element is thought of as a possible aid to assess the usability of a dataset for a specific person. The standard used is ISO 639/1. |
| 6a     | Collection   Process - Start Date                            |          | Indicate when you've started collecting the data for this dataset | Clicking on the field reveals a calendar you can use to pick the date.                                           |
| 6b     | Collection   Process - End Date                              |          | Indicate when you've finished   collecting the data for this dataset | Clicking on the field reveals a calendar you can use to pick the date.                                           |
| 7      | Location(s)   covered                                        |          | Indication of the geographical   entities, like countries, regions and cities, covered by this dataset | English naming convention preferred. It is recommended to use the preferred spelling from the [Getty Thesaurus of Geographic Names](http://www.getty.edu/research/tools/vocabularies/tgn/index.html) whenever possible. One location per line.  This field can have multiple values &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 8a     | Period Covered - Start period                                |          | An indication of the start date of  the period covered by your dataset | Clicking on the field reveals a calendar you can use to pick the date.                                           |
| 8b     | Period   Covered - End Period                                |          | An indication of the end date of   the period covered by your dataset | Clicking on the field reveals a calendar you can use to pick the date.                                           |
| 9      | Tags                                                         |          | Free text field for adding   (searchable) keywords to your dataset | You can choose the keywords freely. It is best to add only one keyword per line. This field can have multiple values &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 10a    | Related Data package                                         |          | The way in which the present data package is related   to another data package. | In this section you can enter a ‘related’ dataset and the nature of   that relation. For instance, you can indicate that another   dataset contains the raw data by selecting *IsSourceOf* in this field and entering the information of the other data package in the fields below. This field can have multiple values &mdash; use the plus sign to add more values. |
| 10b    | Related Data package - Title                                 | If 10a   | Title of the data package related to the present data package. | There is no automatic check whether title and persistent identifier match.  Maximum length: 255 characters.|
| 10d    | Related Data package – Type                                  | If 10e   | The type of the persistent identifier of the related data package   | Example: &ldquo;DOI&rdquo;. Please fill in the plain ID, not a URL |
| 10e    | Related Data package – Identifier                            | If 10d   | The persistent identifier of the related data package.       |  |
| 11     | Retention   Period                                           | Y        | The minimal number of years the   data will be kept in the archive.   The default value is 10 years. | In this field you can only enter integers. The policies for handling expiry of the retention period of a data package are still to be defined. |
| 12     | Retention Information                                        |          | To be used for remarks about the retention period. | Please provide a reason if you deviate from the default value of ten years. If you want to ensure that data is retained longer, then data management might request extra care for choosing sustainable file formats. |
| 13     | Embargo enddate                                              |          | If the dataset has an embargo, on what date does the embargo end? | This functionality is not yet fully implemented. Please contact the data manager if you intend to publish a data package with an embargo. |
| 14     | Data type                                                    |          | Please indicate the type of the data.                  |   |
| 15     | Data Classification                                          | Y        | Please indicate the classification of the data.                  | You can find more information about data classification on this [library libguide](https://libguides.vu.nl/rdm/data-security) |
| 16     | Name of Collection                                           |          | If this data package is part of a larger (conceptual) collection of data packages,   you can enter the collection name here. | The research group should ensure that all other data packages in the collection are archived with the same collection name. Maximum length: 255 characters. |
| 17     | Funder                                                       |          | The name(s) of the organization(s) funding the research.     | Example: &ldquo;NWO&rdquo;. This field can have multiple values &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 18     | Award Number                                                 |          | The grant number issued by the funding organization          |                                                              |
| 19     | Remarks                                                      |          | Remarks from the datamanager          |                                                              |
| 20     | Creator of Data package - Name                               | Y        | The name of the person(s) who created (this version of) the dataset. | This field can have multiple values &mdash; use the plus sign to add more values. Maximum length: 255 characters.|
| 20a    | Creator of Data package – Affiliation                        | Y        | The organizational or   institutional affiliation of the creator | Example: &ldquo;Vrije Universiteit Amsterdam&rdquo;. The affiliation of the creator of a data package could be of importance  when it is unclear who owns the data. In general the organization to which   the creator was affiliated is regarded as the owner. Each creator can have multiple affiliations &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 20b    | Creator of Data package – Persistent Identifier: Type        |          | Please indicate the type of persistent person identifier.    | E.g. AuthorID, ORCID or ResearcherID. Multiple values are possible.   If available, enter at least an ORCID. |
| 20c    | Creator of Data package – Persistent Identifier: Identifier  |          | The Persistent Identifier.                                   | If you are not sure whether someone has a persistent identifier, you can   check with the big three providers: [AuthorID](https://www.scopus.com/freelookup/form/author.uri?zone=&origin=NO%20ORIGIN%20DEFINED), [ORCID](https://orcid.org/orcid-search/search),[ResearcherID](http://www.researcherid.com/ViewProfileSearch.action?returnCode=ROUTER.Success&Init=Yes&SrcApp=CR&SID=E3ZNssthXYuFFfPK2uJ). Each creator can have multiple persistent identifier &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 21     | Contributor to Data Package - Name                           |          | The name of the person(s) who contributed to this dataset.   | Multiple values possible &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 21a    | Contributor to Data Package - Type                           |          | Enter what type of contribution the registered person has had to this   data package. | Examples: *Project lead* or *Project member* This field can have multiple values &mdash; use the plus sign to add more values. |
| 21b    | Contributor to Data Package - Affiliation                    |          | The organizational or institutional   affiliation of the contributor. | E.g. Vrije Universiteit Amsterdam.       Each contributor can have multiple affiliations &mdash; use the plus sign to add multiple values. Maximum length: 255 characters.|
| 21c    | Contributor to Data Package - Persistent Identifier: Type    |          | Please indicate the type of persistent person identifier.    | Each contributor can have multiple persistent identifiers &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 21d    | Contributor to Data Package - Persistent Identifier: Identifier |          | The unique person identifier                                 | Each contributor can have multiple identifiers &mdash; use the plus sign to add more values. Maximum length: 255 characters. |
| 25     | License                                                      | Y        | The license under which you offer the data package for use by third   parties. The preferred value for open data is [CC By 4.0](https://creativecommons.org/licenses/by/4.0/). | Every package needs to be archived with a license &mdash; even when you’re not   planning to publish the data or have it reused in any form.       We offer a number of possible licenses in a drop-down list. If you do not   know which license to choose, contact the data manager.   At the moment of publishing a data package the relevant license text will   be copied into the data package. If you opt for a custom license, you will need to store the custom   license text in a file titled *License.txt*   in the root folder. Please contact the data manager first if you want to   work with custom licenses. |
| 26     | Data Package Access                                          | Y        | Once archived, should your dataset be  accessible to third parties? | *Open Access* means that the dataset is accessible to everyone.  *Restricted Access* means that the dataset can only be obtained on request. *Closed Access* means that the dataset cannot be shared, in principle. |
