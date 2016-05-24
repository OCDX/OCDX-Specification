# OCDX Data Manifest
## Specification Version: 0.1

# standardsVersion
## Definition and Purpose
Define which manifest standard this manifest is following. This field is machine-generated.

## Cardinality
* required
* not repeatable

## Data format
e.g., v0.1.4

## JSON Example
```json
{
	"standardsVersion": " "
}
```

# id
## Purpose
Uniquely identify the manifest so that we don't confuse it with others and can refer to it easily. This is machine-generated.

## Cardinality
* required
* not repeatable

## Data format


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
string (e.g., Megan Squire)

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
	"dateCreated": " "
}
```

# comment
## Definition and Purpose
Any comments on the creation of the manifest. This is where you can tell us more about any "no assertion" answers or the script that generated the manfiest, for instance. You could also tell us about any problems you ran into generating the manifest.

## Cardinality
* not required
* not repeatable

## Data format
string

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
		"dates": { }
	}
}

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

# researchObject: provenance
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# researchObject: bibliograpicCitations
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example

# Item
## Definition and Purpose

## Cardinality
* required
* repeatable
* 1:many
## Data format

## JSON Example