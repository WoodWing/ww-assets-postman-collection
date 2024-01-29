# ww-assets-postman-collection

# Description
This is a Postman collection for working with WoodWing Assets. The collection itself contains, at this time, a subset of the available API calls. Those that are included in the collection are noted below. All of the Assets API documentation can be found here: [Woodwing Helpcenter] (https://helpcenter.woodwing.com/hc/en-us/sections/360008455892-APIs-REST). 

In some cases we have added parameters to the calls so that they may be more useful as a starting point. 

# Postman Explanation
When creating this collection we considered three parts of Postman's capabilities:
1. Collections
2. Environments
3. Flows (part of Postman 10)

Please note that to use this collection you will need to create your Environment and, if you wish to use Flows, you'll need to create those as well. Farther down we have included videos to help out with that process.

The relationship between the Collection and the Environments is particularly helpful. Environments allows us to create variables, attach values to the variables and then pass the variable value(s) to subsequent calls. The variables can be used calling each individual call within the collection or you can set up a Flow to use them.

In our environment, named 'WoodWing Assets', we have 4 variables:

1. Assets_Server_URL - referenced in the collection as {{Assets_Server_URL}}
2. username - referenced in the collection as {{username}}
3. password - referenced in the collection as {{password}}
4. Current X-CRSF-TOKEN - referenced in the collection as {{Current X-CRSF-TOKEN}}
5. api_user_name - referenced in the collection as {{api_user_name}}
6. api_password - referenced in the collection as {{api_password}}
7. authToken - referenced in the collection as {{auth_token}}
8. ids - referenced in the collection as {{ids}} => meant to be an array of Assets IDs
9. id - referenced in the collection as {{id}} => Individual ID of an asset
10. folder_id - referenced in the collection as {{folder_id}}
11. external_engine_id - referenced in the collection as {{external_engine_id}}

Here is a short video showing how Collections and Environments work: 

# Flows
Flows are for the creation of a complete set of calls and responses to the API endpoint. Seeing is believing so here is a short video showing the basic creation and usage of a Flow using the Collection and the Environment:

## Release Notes
1. v0.1 - Initial release of the collection
2. v0.2 - Extensive changes to the collection. All 'Assets' calls are now included in the collection. I've added a variety of variables to an environment and use those variables through the collection. 
3. v0.3 - Extensive changes to the collection. Added External Processing and Metrics. Added Environment file and description of variables in the Environment file.

## Calls contained within the collection

### Login and Logout
1. Standard Login and Logout
3. API Login and Logout Logout

### Metadata Reports
1. Metadata report call asking for JSON and using a query to get all assets with status of Production
2. Metadata report call asking for CSV and using a query to get all assets with status of Production
3. Metadata report call asking for JSON and using the assetPath parameter
4. Metadata report using 'login', JSON and a 'assetPath' query

### Operations
#### Search and Browse
1. Browse
2. Search

#### Working with Assets
1. Create
2. Copy
3. Checkout
4. Undo Checkout
5. Move / Rename
6. Remove
7. Update bulk
8. Update / check in
9. Versioning and History
10. Log Usage Stats

#### Relations
1. Create Relation
2. Remove Relation

#### Auth Keys (Sharelinks)
1. Create Auth Key
2. Update Auth Key
3. Revoke Auth Key

#### Folders
1. Create Folder

#### Renditions
1. Rendition Preset - List
2. Rendition Preset - List All
3. Rendition Preset - Save / Update
4. Rendition Preset - Remove

#### Misc
1. Email
2. Localization
3. Profile

### REST API - Management Console
Note that these calls are documented within the Management Console of Assets.
#### Working with Assets
1. Create Asset
2. Create Asset - API Upload
3. Search
4. Signed Image Rendition URL
5. Signed Original URL
6. Signed Preview URL
7. Signed Thumbnail URL
8. Get Specific Asset
9. Download Asset Original
10. Upload Asset (Multi-part form) [POST]
11. Upload Asset (Multi-part form) [PUT]
12. Download Asset Preview
13. Download Asset Thumbnail

#### Create Sharelink
1. Create Sharelink

#### Folder
1. Create Folder (with metadata)
2. Get Folder by Path
3. List folders
4. Folder Search
5. Get Folder by id
6. Update Folder Metadata
7. Delete Folder

### External processing (not in final form)
1. Create External Engine
2. Get All External Engines
3. Get External Engines by ID
4. Update External Engines by ID
5. Delete External Engines by ID
6. Delete All External Engines

### Metrics
1. Get Assets Metrics
