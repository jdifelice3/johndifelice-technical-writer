# Third Party Packages

## Body-Parser

Node.js body parsing middleware.

It parses incoming request bodies in middleware before your handlers, available under the req.body property.

Note As req.body's shape is based on user-controlled input, all properties and values in this object are untrusted and should be validated before trusting. For example, req.body.foo.toString() may fail in multiple ways, for example the foo property may not be there or may not be a string, and toString may not be a function and instead a string or other user input.