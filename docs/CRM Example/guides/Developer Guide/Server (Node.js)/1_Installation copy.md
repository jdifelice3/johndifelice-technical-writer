# Installation

Follow the instructions in the Client (React) section, under "Git Repository" and "Node.js & Node Package Manager (npm)" sections.


#### package.json
```json
{
  "name": "zoho-data-explorer-server",
  "version": "1.0.0",
  "type": "module",
  "description": "Backend for ZohoDataExplorer",
  "main": "server.js",
  "scripts": {
    "dev": "nodemon server.js --mode=development",
    "start": "node server.js --mode=production"
  },
  "dependencies": {
    "axios": "^1.8.4",
    "body-parser": "^1.19.0",
    "cors": "^2.8.5",
    "csv-parser": "^3.2.0",
    "csv-stringify": "^6.5.2",
    "express": "^4.17.1",
    "fs": "^0.0.1-security",
    "json2csv": "^5.0.7",
    "mssql": "^11.0.1",
    "swagger-jsdoc": "^6.2.8",
    "swagger-ui-express": "^5.0.1",
    "yamljs": "^0.3.0"
  },
  "devDependencies": {
    "cross-env": "^7.0.3",
    "dotenv": "^16.4.7",
    "nodemon": "^2.0.4"
  },
  "author": "Robert Clarke",
  "license": "MIT"
}
```

Run the server using either one of the two commands, depending if the target environment is development or production.

```bash
nodemon server.js --mode=development
node server.js --mode=production
```
```nodemon``` is an executable that watches for file changes and reruns the server when a change occurs.