[toc]

# OCDX Data Manifest Specifications
__Version: 0.1__

This document describes the properties you should include in a manifest for inclusion in the OCDX manifest directory. For each property, we describe its definition and purpose, cardinality, and format. We currently provide one [complete example](sampleCompletedManifest.json).

## standardsVersion
### Definition and Purpose
Define which manifest standard this manifest is following. This field is machine-generated.

### Cardinality
* required
* not repeatable

### Data Format
string 

* Example: v0.1.4

## id
### Definition and Purpose
Uniquely identify the manifest so that we don't confuse it with others and can refer to it easily. This is machine-generated.

### Cardinality
* required
* not repeatable

### Data Format
TBD

## creator
### Definition and Purpose
Name the person or tool who is creating this manifest so that we know who or how it was created.

### Cardinality
* required
* not repeatable
 
### Data Format
string 

* Example: Megan Squire

## dateCreated
### Definition and Purpose
Date the manifest was created.

### Cardinality
* required
* not repeatable

### Data Format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)
 
* Example: 2016-05-24

## comment
### Definition and Purpose
Any comments on the creation of the manifest. This is where you can tell us more about any "no assertion" answers or the script that generated the manifest, for instance. You could also tell us about any problems you ran into generating the manifest.

### Cardinality
* not required
* not repeatable

### Data Format
string

## researchObject
### Definition and Purpose
A container for information about the dataset you are describing. We call it a "research object" because you will likely use it to do your research and it may contain a variety of things such as data files, scripts for processing data, and maybe, if you're lucky, documentation.

### Cardinality
* required
* not repeatable

### Data Format
just a container - children will have specific data formats

## researchObject: creators
### Definition and Purpose
A container for information about the creator(s) of the research object - who put all this data together?

### Cardinality
* not required
* repeatable (meaning you can provide more than one contact)

### Data Format
just a container - children will have specific data formats

## researchObject: creators: name
### Definition and Purpose
Name of the person or persons responsible for creating the files. Must include at least one human being or beings in order to provide a point of contact for support if needed.

### Cardinality
* required
* not repeatable

### Data Format
string, First Name Last Name

## researchObject: creators: email
### Definition and Purpose
Provides a point of contact in case assistance is needed. May be an individual email address or mailing list. 

### Cardinality
* required
* not repeatable

### Data Format
string, email


## researchObject: abstract
### Definition and Purpose
A complete summary of the dataset which should include institutional affiliations, motivations for data collection, and magnitude of the data (how many people, events, rows, etc.).

### Cardinality
* required
* not repeatable

### Data Format
string

* Example: The Teahouse corpus is aset of questions asked at the Wikipedia Teahouse, a peer support forum for new Wikipedia editors. This corpus contains data from its first two years of operation.

## researchObject: title
### Definition and Purpose
Give the stuff you're sharing a name. This will be used for search purposes, so choose terms appropriately (i.e., be more descriptive than cute).

### Cardinality
* required
* not repeatable

### Data Format
string

* Example: Data Sets of Insults, Gender Stereotypes, Double Entendres in FLOSS Communication)

## researchObject: dates
### Definition and Purpose
Container for dates where dates are times relevant to the contents, creation, retrieval of the dataset this manifest describes.

### Cardinality
* not required
* not repeatable

### Data Format
just a container - children will have specific data formats

## researchObject: dates: datasetTimeInterval
### Definition and Purpose
The start and end times of the data are useful for people searching for specific time periods, and they help us know what period this data actually covers.

* Example: For a Twitter dataset, the earliest and latest dates represented in the dataset. So, the time the oldest tweet was posted, and the time the newest tweet was posted.

### Cardinality
* not required 
* not repeatable

### Data Format
[ISO 8601 Intervals](https://en.wikipedia.org/wiki/ISO_8601)
yyyy-mm-dd/yyyy-mm-dd

* Example: 2016-03-01/2016-05-31

## researchObject: dates: dateRetrievedTimeInterval
### Definition and Purpose
Describes when the data collection happened - the earliest and latest times that data were collected. This is important because some data (like Twitter or Wikipedia) change, and so we need to know when the data was collected. This can also signal information like API version implicitly.

### Cardinality
* not required
* not repeatable

### Data Format
ISO 8601, YYYY-MM-DD

## researchObject: dates: dateCreated
### Definition and Purpose
Describes when the research object was created - when did you put all this stuff together?

### Cardinality
* required
* not repeatable

### Data Format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)
 
* Example: 2016-05-24

## researchObject: provenance
### Definition and Purpose
The purpose of this field is to describe how the data set was created, ownership changes, and any scripts applied to the raw, collected data set between the time of collection and its storage in a repository. References to versions of specific software programs used to modify the originally collected data into the stored form should be noted here if available. Transformations to the originally collected data set should be briefly described. For instance, you should describe how you collected the data (e.g., which API? did you scrape?), what kind of processing you did on the data (e.g., how you cleaned it up, if you parsed it into a DB or something).  Providing a pointer to a full description of the data generation and processing (e.g., methods section of a research paper) is equally valuable.

Based on [Dublin Core](http://dublincore.org/documents/usageguide/elements.shtml).

### Cardinality
* not required
* not repeatable

### Data Format

string, URLs to stable locations with full descriptions of data generation and processing.

## researchObject: bibliographicCitations
### Definition and Purpose

Provides context for the data, e.g., a published paper that used the data or describes it.  Can also be a "preferred citation", e.g., in contexts where citations to papers are preferred over citations to datasets (if this is the case, indicate it in the manifest comments). Not a citation for the _data_ but for a paper or the product about or using the data.

### Cardinality
* not required
* repeatable

### Data Format
string, a fully-formed citation or RIS citation for the paper(s), article(s), etc.

* Example: Squire, M. & Gazda, R. (2015). FLOSS as a source for profanity and insults: Collecting the data. In Proceedings of 48th Hawai'i International Conference on System Sciences (HICSS-48). IEEE. Hawaii, USA. 5290-5298.



## researchObject: distributions
### Definition and Purpose
A container for information about where to actually access the data this manifest describes.

### Cardinality
* not required
* repeatable

### Data Format
just a container - children will have specific data formats

## researchObject: distributions: uri 
### Definition and Purpose

URI for accessing the data and related artifacts. Ideally persistent. Can also be an API or ODBC connection.

### Cardinality
* required
* repeatable

### Data Format
string, URI

## researchObject: distributions: comment 
### Definition and Purpose
Any necessary details related to the specific distribution documented in the manifest. If there are necessary details for access, e.g., for APIs, ODBC connections, and repositories, please note them here.

### Cardinality
* not required
* not repeatable

### Data Format
string

## researchObject: files 
### Definition and Purpose
Container to provide a list of the files included in the research object. In some cases, this could be a single file. In other cases, the full corpora associated with a dataset, or an integrated dataset used for research and publication, could include many different files. Files may include data files, related papers, processing scripts, etc. While files are not required, if you _do_ provide file information, some properties within the file description are required (i.e., if you provide file information, you must provide a file's name).

Files is an array of files where each file has the properties
* name
* abstract
* size
* uri
* checksum
* permissions
* dates

### Cardinality
* not required
* repeatable (meaning you can describe multiple files)

### Data Format
just a container - children will have specific data formats

## researchObject: files: name
### Definition and Purpose
File name, e.g., 2012LTinsultsLKML.tsv.txt.

### Cardinality
* not required
* not repeatable

### Data Format
string, a full file name include extension

## researchObject: files: format
### Definition and Purpose
[MIME type](https://en.wikipedia.org/wiki/Media_type) for the file.

### Cardinality
* not required
* not repeatable

### Data Format
string, ([MIME type or file extension](https://en.wikipedia.org/wiki/Media_type))

* Example: application/json

## researchObjects: files: dates: fileTimeInterval
### Definition and Purpose
The start and end times of the data within the file are useful for people searching for specific time periods, and they help us know what period the data in the file actually covers.

* Example: For a file of insults posted by Linus Torvalds, the earliest and latest dates on which he sent those insults as recorded in the file.

### Cardinality
* not required 
* not repeatable

### Data Format
[ISO 8601 Intervals](https://en.wikipedia.org/wiki/ISO_8601)
yyyy-mm-dd/yyyy-mm-dd

* Example: 2016-03-01/2016-05-31

## researchObject: files: dates: dateRetrievedTimeInterval
### Definition and Purpose
Describes when the data collection for the data in this file happened - the earliest and latest times that data in this file were collected. This is important because some data (like Twitter or Wikipedia) change, and so we need to know when the data was collected for the content of the file. This can also signal information like API version implicitly.  

### Cardinality
* singular
* not required
* not repeatable 

### Data Format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)

* Example: 2016-05-24

## researchObject: files: dates: dateCreated
### Definition and Purpose
Describes when the file was created - when did you put all this stuff together?

### Cardinality
* not required
* not repeatable

### Data Format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)
 
* Example: 2016-05-24


## researchObject: files: abstract
### Definition and Purpose
Description of the contents of the file. When datasets are composed of multiple files, it is useful to indicate which files contain which data.

### Cardinality
* not required
* not repeatable

### Data Format
string

## researchObject: files: size
### Definition and Purpose
Disk size of file, provides context to determine what tools to use on the file.

### Cardinality
* not required
* not repeatable

### Data Format
Based on International System of Quantities: number and size, e.g., 10MG, 2.4GB, 500PB.

## researchObject: files: uri
### Definition and Purpose
If the individual file has a specific and distinct URI, indicate it here.

### Cardinality
* not required
* not repeatable

### Data Format
string:URI


## researchObject: files: checksum
### Definition and Purpose
A [checksum](https://en.wikipedia.org/wiki/Checksum) for the file. The purpose is to verify authenticity of the file.

### Cardinality
* not required
* not repeatable

### Data Format
string

## researchObject: files: permission
### Definition and Purpose
Description of any file-specific limits on use or access.

### Cardinality
* not required
* not repeatable

### Data Format
string
