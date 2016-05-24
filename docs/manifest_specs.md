Manifest Specifications

# OCDX Data Manifest
## Specification Version: 0.1

# standardsVersion
## Definition and Purpose
Define which manifest standard this manifest is following. This field is machine-generated.

## Cardinality
* required
* not repeatable

## Data format
string: 

Example: v0.1.4

## JSON Example
```json
{
        "standardsVersion": "v0.1.4"
}
```

# id
## Purpose
Uniquely identify the manifest so that we don't confuse it with others and can refer to it easily. This is machine-generated.

## Cardinality
* required
* not repeatable

## Data format
TBD

## JSON Example
```json
{
        "id": " "
}
```

# creator
## Definition and Purpose
Name the person or tool who is creating this manifest so that we know who or how it was created.

## Cardinality
* required
* not repeatable
 
## Data format
string 

Example: Megan Squire

## JSON Example
```json
{
        "creator": " "
}
```

# dateCreated
## Definition and Purpose
Date the manifest was created.

## Cardinality
* required
* not repeatable

## Data format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)
 
* Example: 2016-05-24

## JSON Example
```json
{
        "dateCreated": "2016-05-24"
}
```

# comment
## Definition and Purpose
Any comments on the creation of the manifest. This is where you can tell us more about any "no assertion" answers or the script that generated the manfiest, for instance. You could also tell us about any problems you ran into generating the manifest.

## Cardinality
* not required
* not repeatable

## Data format
string: plain text

## JSON Example
```json
{
        "comment": " "
}
```

# researchObject
## Definition and Purpose
A container for information about the dataset you are describing. We call it a "research object" because you will likely use it to do your research and it may contain a variety of things such as data files, scripts for processing data, and maybe, if you're lucky, documentation.

## Cardinality
just a container - children have cardinality but the container doesn't

## Data format
just a container - children will have specific data formats

## JSON Example
```json
{
        "researchObject": {
        }
}
```

# researchObject: title
## Definition and Purpose
Give the stuff you're sharing a name. This will be used for search purposes, so choose terms appropriately (i.e., be more descriptive than cute).

## Cardinality
* required
* not repeatable

## Data format
string

* Example: Data Sets of Insults, Gender Stereotypes, Double Entendres in FLOSS Communication)
* 
## JSON Example
```json
{
        "researchObject": {
                "title": " "
        }
}
```

# researchObject: dates
## Definition and Purpose
Container for dates where dates are times relevant to the contents, creation, retrieval of the dataset this manifest describes.

## Cardinality
just a container - children have cardinality but the container doesn't

## Data format
just a container - children will have specific data formats

## JSON Example
```json
{
        "researchObject": {
                "dates": { }
        }
}
```
# researchObject: dates: datasetTimeInterval
## Definition and Purpose
The start and end times of the data are useful for people searching for specific time periods, and they help us know what period this data actually covers.

* Example: For a Twitter dataset, the earliest and latest dates represented in the dataset. So, the time the oldest tweet was posted, and the time the newest tweet was posted.

## Cardinality
* not required 
* not repeatable

## Data format
[ISO 8601 Intervals](https://en.wikipedia.org/wiki/ISO_8601)
yyyy-mm-dd/yyyy-mm-dd

* Example: 2016-03-01/2016-05-31

## JSON Example
```json
{
        "researchObject": {
                "dates": { 
                        "datasetTimeInterval": ""
                        }
        }
}
```
# researchObject: dates: dateRetreivedTimeInterval
## Definition and Purpose
Describes when the data collection happened - the earliest and latest times that data were collected. This is important because some data (like Twitter or Wikipedia) change, and so we need to know when the data was collected. This can also signal information like API version implicitly.

## Cardinality
just a container - children have cardinality but the container doesn't

## Data format
just a container - children will have specific data formats

## JSON Example
{
        "researchObject": {
                "dates": { 
                        "dateRetrievedTimeInterval" : " " }
        }
}

# researchObject: dates: dateCreated
## Definition and Purpose
Describes when the research object was created - when did you put all this stuff together?

## Cardinality
* required
* not repeatable

## Data format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)
 
* Example: 2016-05-24

## JSON Example
```json
{
        "researchObject": {
                "dates": { 
                        "dateCreated" : " "}
        }
}
```

# researchObject: provenance
## Definition and Purpose
The purpose of this field is to describe how the data set was created, ownership changes, and any scripts applied to the raw, collected data set between the time of collection and its storage in a repository. References to versions of specific software programs used to modify the originally collected data into the stored form should be noted here if available. Transformations to the originally collected data set should be briefly described. For instance, you should describe how you collected the data (e.g., which API? did you scrape?), what kind of processing you did on the data (e.g., how you cleaned it up, if you parsed it into a DB or something).  Providing a pointer to a full description of the data generation and processing (e.g., methods section of a research paper) is equally valuable.
Based on [Dublin Core](http://dublincore.org/documents/usageguide/elements.shtml).

## Cardinality
* not required
* not repeatable

## Data format

Plain text; URLs to stable locations with full descriptions of data generation and processing.

## JSON Example

```json
{
        "researchObject": {
                "provenance": 
        }
}
```

# researchObject: bibliographicCitations
## Definition and Purpose

Provides context for the data, e.g., a published paper that used the data or describes it.  Can also be a "preferred citation", e.g., in contexts where citations to papers are preferred over citations to datasets (if this is the case, indicate it in the manifest comments).

## Cardinality
* not required
* repeatable

## Data format
String, a fully-formed citation or RIS citation for the paper(s), article(s), etc.

Example: Squire, M. & Gazda, R. (2015). FLOSS as a source for profanity and insults: Collecting the data. In Proceedings of 48th Hawai'i International Conference on System Sciences (HICSS-48). IEEE. Hawaii, USA. 5290-5298

## JSON Example
```json
{
        "researchObject": {
                "bibliographicCitation": "Squire, M. & Gazda, R. (2015). FLOSS as a source for profanity and insults: Collecting the data. In Proceedings of 48th Hawai'i International Conference on System Sciences (HICSS-48). IEEE. Hawaii, USA. 5290-5298."
        }
}
```
# researchObject: distributions
## Definition and Purpose
A container for information about where to actually access the data this manifest describes.

## Cardinality
just a container - children have cardinality but the container doesn't

## Data format
just a container - children will have specific data formats

## JSON Example
```json
{
"researchObject": {
"distributions": [
]
}
}
```

# researchObject: distributions: uri: 
## Definition and Purpose

URI for accessing the data and related artifacts. Ideally persistent. Can also be an API or ODBC connection.

## Cardinality
* required
* repeatable

## Data format
string:URI

## JSON Example
```json
{
"researchObject": {
"distributions": [
{
"uri": "http://flossdata.syr.edu/data/insults/"
}
]
}
}
```

# researchObject: distributions: comment: 
## Definition and Purpose
Any necessary details related to the specific distribution documented in the manifest. If there are necessary details for access, e.g., for APIs, ODBC connections, and repositories, please note them here.

## Cardinality
* not required
* not repeatable

## Data format
string:plain text

## JSON Example
```json
{
"researchObject": {
"distributions": [
{
"comment": "Folder with 7 data files & 1 PDF paper file"
}
]
}
}
```

# researchObject: files: 
## Definition and Purpose
Container to provide a list of the files included in the research object. In some cases, this could be a single file. In other cases, the full corpora associated with a dataset, or an integrated dataset used for research and publication, could include many different files. Files may include data files, related papers, processing scripts, etc. While files are not required, if you _do_ provide file information, some properties within the file description are required (i.e., if you provide file information, you must provide a file's name).

Files is an array of files where each file has the properties
* creator(s) 
* name
* abstract
* size
* uri
* checksum
* permissions
* dates

## Cardinality
just a container - children have cardinality but the container doesn't

## Data format
just a container - children will have specific data formats

## JSON Example
```json

```
# researchObject: files: creator
## Definition and Purpose
Name of the person or persons responsible for creating the files. Alternately, a script or software if more suitable.

## Cardinality
* not required
* repeatable

## Data format

## JSON Example
```json

```
# researchObject: files: name
## Definition and Purpose
File name, e.g., 2012LTinsultsLKML.tsv.txt.

## Cardinality
* not required
* not repeatable

## Data format
string

## JSON Example
```json

```

# researchObject: files: format
## Definition and Purpose
MIME type for the file.

## Cardinality
* not required
* not repeatable

## Data format
string (MIME)

## JSON Example
```json

```


## Dates
# researchObjects: files: dates: datasetTimeInterval
## Definition and Purpose
The start and end times of the data are useful for people searching for specific time periods, and they help us know what period this data actually covers.

* Example: For a Twitter dataset, the earliest and latest dates represented in the dataset. So, the time the oldest tweet was posted, and the time the newest tweet was posted.  This may be one of several files

## Cardinality
* not required 
* not repeatable

## Data format
[ISO 8601 Intervals](https://en.wikipedia.org/wiki/ISO_8601)
yyyy-mm-dd/yyyy-mm-dd

* Example: 2016-03-01/2016-05-31

## JSON Example
```json
{
        "researchObject": {
        "files" {
                "dates": { 
                        "datasetTimeInterval": ""
                        }
					}
        }
}
```
# researchObject: files: dates: dateRetreivedTimeInterval
## Definition and Purpose
Describes when the data collection happened - the earliest and latest times that data were collected. This is important because some data (like Twitter or Wikipedia) change, and so we need to know when the data was collected. This can also signal information like API version implicitly.  

## Cardinality
* singular
* not required 

## Data format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)

* Example: 2016-05-24


## JSON Example
```json
{
        "researchObject": {
"files": {
                "dates": { 
                        "dateRetrievedTimeInterval" : " " }
        }

}
```

# researchObject: dates: dateCreated
## Definition and Purpose
Describes when the research object was created - when did you put all this stuff together?

## Cardinality
* required
* not repeatable

## Data format
[ISO 8601 yyyy-mm-dd](https://en.wikipedia.org/wiki/ISO_8601)
 
* Example: 2016-05-24

## JSON Example
```json
{
        "researchObject": {
                "dates": { 
                        "dateCreated" : " "}
        }
}
```


# researchObject: files: abstract
## Definition and Purpose

## Cardinality

## Data format

## JSON Example
```json

```
# researchObject: files: size
## Definition and Purpose

## Cardinality

## Data format

## JSON Example
```json

```
# researchObject: files: uri
## Definition and Purpose

## Cardinality

## Data format

## JSON Example
```json

```
# researchObject: files: checksum
## Definition and Purpose

## Cardinality

## Data format

## JSON Example
```json

```

# researchObject: files: permission
## Definition and Purpose

## Cardinality

## Data format

## JSON Example
```json

```




Template:
# researchObject: files: uri
## Definition and Purpose
MIME type 

## Cardinality

## Data format

## JSON Example
```json

```

