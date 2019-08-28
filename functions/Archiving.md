# Archiving your data

When archiving your data, you create a snapshot of a part of the data in your user-group and copy this snapshot to the archive (aka 'Vault') of your user-group, where it will be retained unchanged for the period you indicate. 

After archiving your data, you can publish it, making your data findable and, depending on your settings, accessible.

## Submitting data

You can create an archival package in the Yoda portal. Simply navigate to the folder you want to archive and press the <Actions (Submit)> button. 

![](\\soliscom.uu.nl\users\Liagr001\My Documents\Instituties\Gittest\yoda-uu-nl\functions\Submit-button.JPG)

Before sending your data as a data package to the Vault, ensure that:

1. You have the appropriate rights, either group manager or read/write permissions.

2. You are **in** the folder of which you want archive (incl. it's sub-folders).

3. The folder has a file containing all mandatory Yoda metadata. If this is not the case the system will tell you what metadata is missing and allows you to edit the metadataform (button <Metadata>)
4. The folder is not locked (check the button <(Un)lock> or press the exclamation mark next to the folder name, to identify the location of the lock in the folder tree.)

 When you start the archival process, the system will automatically

- Check whether there is a valid metadata file available in the folder where you started your submission

- lock the folder and its sub-folders
- Notify the data manager that a new data package is waiting for assessment - after his approval, the data will be archived.

## Creating a data-package

The data in your research-group is ‘just’ a bunch of files and folders of which only you and your co-workers in your user-group know what they mean and how they relate.

When you archive data, you need to make it into a ‘comprehensible’ package, so that once you publish your archival package, colleague researchers can understand what the data is about, how it was collected/generated and how and under what conditions it can be (re)used. 

You do this by ensuring a proper folder structure, filling in the Yoda-metadata form, and providing readme.txt and/or codebook files that describe your data in more detail.

## Access to your archived data

Once you've archived a data-package you have access to it as long as you are member of the specific user-group. 

If the user group no longer exists you can request access to the data-package via the data manager, or, if the data-package has been published as _Open Access_, it can be retrieved via Data Catalogues, e.g. that of 

[Dans Narcis]:(https://www.narcis.nl/?Language=nl "Narcis"

or 

[DataCite]: https://search.datacite.org/	"DataCite"

## Maintenance of an archived data package

Once your data has been secured in the Yoda Vault, it will remain there for the time you have indicated in the metadata. During this retention time the data files will be checked regularly for bit-rot. Affected files will be replaced with a back-up.

## Checks before archiving ##

When you start the archival process, the system will automatically check for a valid metadata file.

After that the data manager manually assesses the data-package as well.  If he finds unclarities in the description, he can ask for changes to the folder structure or data-package description before he accepts the package for archival.

The basic idea behind this assessment is that

- the data packages are self-evident for other researchers
- meet basic standards of quality
- comply to sensitive data and privacy rules and regulations.

This assessment consists of a number of checks. Each category will have its own checks. Below you will find the I-Lab’s Data Manager check as an example.

- Folders
    - logical structure
    - logical naming convention

- Codebook
    - the setup of the research
    - the variables of the dataset
    - the units used
    - the instruments
    - sampling method and
    - sample size,
    - experimental set up,
    - etc.

- Large dataset (multiple data objects, e.g. multiple excel sheets)
    - A document describing the relation between the data objects?

-  Raw data
    - If the data package contains raw personal data, the Accessibility should be closed or restricted.
    - If the dataset is based on raw data, which is not available in the set itself, there should be a reference to the location of the raw dataset.
    - If the dataset contains data processed from raw data it should contain a description on how the former has been derived from the latter, e.g. by providing algorithms and/or transformation scripts.

- Valid data
    - Validaty of data in a formal sense; e.g. an excel sheet with calculations should not contain cells with warnings like ‘invalid value’.

