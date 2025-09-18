# Environment Variables

Environment variables are in the ```.env``` file. Here are the contents of the file as of this writing.
```js
NODE_ENV=development

# ZOHO CREDENTIALS
ZOHO_API_DOMAIN=https://www.zohoapis.com
ZOHO_CLIENT_ID=***********************************
ZOHO_CLIENT_SECRET=******************************************

# ZOHO API REFRESH TOKENS
ZOHO_CAMPAIGN_CONTACTS_ALL_REFRESH_TOKEN=1000.1c6eb7842bd6ec76191ac303e1a80d78.a0341ed0f270955d0e048d642a590b6f    
ZOHO_CAMPAIGN_CONTACTS_UPDATE_REFRESH_TOKEN=1000.75d93603bc98f17da0ba1fd840ecc970.0aae803d410a8aa8f4f08b64b09bd32d
ZOHO_RECRUIT_CLIENT_ALL_REFRESH_TOKEN=1000.e32dec05284b83cab62cb42f26db4397.4f857c8a0bb566b88968eae8421b7177
ZOHO_RECRUIT_MODULES_ALL_REFRESH_TOKEN=1000.1508ce9d03711cc325e5bf8865798d42.6428e64417fc86a49e8a2640131721b7
ZOHO_RECRUIT_SETTINGS_ALL_REFRESH_TOKEN=1000.a91ec564394dabdf2eee9e0bcec35d31.cf52220eb57462c1b251773463970058
ZOHO_RECRUIT_SEARCH_READ_REFRESH_TOKEN=1000.765ed28b7d174beb71614ee941669553.2c04c6cbdd730bb1355b46f84826f9e6

# ZOHO API ENDPOINTS
ZOHO_API_ACCESS_TOKEN_URL=https://accounts.zoho.com/oauth/v2/token
ZOHO_API_ASSOCIATE_CONTACT_TAG_URL=https://campaigns.zoho.com/api/v1.1/tag/associate
ZOHO_API_BASE_URL=https://www.zohoapis.com/crm/v2
ZOHO_API_GET_CLIENTS_URL=https://recruit.zoho.com/recruit/v2/Clients
ZOHO_API_GET_CONTACTS=https://recruit.zoho.com/recruit/v2/Contacts
ZOHO_API_TOKEN_REDIRCT_URL=http://localhost:8080/oauth/callback
ZOHO_API_GET_CONTACTS_SEARCH_URL=https://recruit.zoho.com/recruit/v2/Contacts/search

# SQL SERVER CONFIG
DB_CONFIG={"server": "localhost","port": 1433,"user": "NewAdminLogin","password": "StrongPassword123!","database": "Zoho","options": {"encrypt": false,"trustServerCertificate": true}}
DB_CLIENT_CSV_FILENAME=clients.csv
DB_CONTACT_CSV_FILENAME=contacts.csv

# SERVER CONFIG
DB_SERVER_PORT=5000
DB_WEB_SERVICE_URL=http://localhost:5000
WEB_SERVER_HOST=localhost
WEB_SERVER_PORT=5173
WEB_SERVER_URL=http://localhost:5173
```

Variables defined in this file are accessible with the ```process.env``` object in the ```dotenv``` package.

NOTE: the ```.env``` file should never be checked into git or any other source control because it contains client ids and client secrets.