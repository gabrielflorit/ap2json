# ap2json
[![Build Status](https://travis-ci.org/gabrielflorit/ap2json.svg?branch=master)](https://travis-ci.org/gabrielflorit/ap2json)

Split one AP API request into many JSON files. Currently only works on presidential primaries.

	Usage: ap2json [options]

	Options:
		-f, --file       File containing API election results. Must have a <races> field.  [string] [required]
		-d, --directory  Directory where ap2json will place the output JSON files.  [string] [required]
		-c, --clear      Whether to clear output directory before writing output files.  [boolean] [default: true]

		Examples:
			ap2json -f results.json -d output -c false

## Real-world example

```sh
# First download results from AP:
curl 'https://api.ap.org/v2/elections/2016-02-01?test=true&level=ru&apikey=<APTOKEN>&format=json' > ia.json
# Then:
```
![output](https://cloud.githubusercontent.com/assets/370976/12668272/e0ff613e-c622-11e5-964d-ac6fc4bef2b8.png)

## Install

`npm install -g ap2json`
