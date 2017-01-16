[![npm version](https://badge.fury.io/js/mime-names.svg)](https://badge.fury.io/js/mime-names)

# mime-names

This is a database of mime names keyed by mime types. It was created to use alongside
https://github.com/jshttp/mime-db and as such mirrors the structure of the project.

It does **not** try to be all encompassing and instead includes the most popular file formats,
your code should gracefully handle a mime type not existing in this database.


## Installation

```bash
npm install mime-names
```

## Usage

```js
var db = require('mime-names');

var data = db['application/javascript'];
console.log(data.name);
```

## Contributing

Happily accepting PR's which add new types and names, particularly those listed in `mime-db`


## Data Structure

The JSON file is a map lookup for lowercased mime types.
Each mime type has the following properties:

- `.name` - a human readable description of the file type
- `.extensions[]` - known extensions associated with this mime type.
