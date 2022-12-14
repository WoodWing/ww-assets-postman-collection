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
2. username - references in the collection as {{username}}
3. password - references in the collection as {{password}}
4. Current X-CRSF-TOKEN - references in the collection as {{Current X-CRSF-TOKEN}}

Here is a short video showing how Collections and Environments work: 



# Flows
Flows are for the creation of a complete set of calls and responses to the API endpoint. Seeing is believing so here is a short video showing the basic creation and usage of a Flow using the Collection and the Environment:



## Release Notes
v0.1 - Initial release of the collection

## Calls contained within the collection

### Login and Logout
1. Login Using 'apilogin'
2. Logout
3. Login using 'login'
4. Logout

### Metadata Reports
1. Metadata report call asking for JSON and using a query to get all assets with status of Production
2. Metadata report call asking for CSV and using a query to get all assets with status of Production
3. Metadata report call asking for JSON and using the assetPath parameter
4. Metadata report using 'login', JSON and a 'assetPath' query

### Operations
1. Create
2. Search
3. Copy
4. Create Relation
5. Checkout
6. Undo Checkout

### Calls not yet included
1. browse
2. createAuthKey
3. createFolder
4. E-mail
5. localization
6. log usage stats
7. move / rename
8. profile
9. promote
10. remove
11. remove relation
12. Rendition Presets
13. revokeAuthKeys
14. updateAuthKey
15. updatebulk
16. update / check-in
17. versioning and history
18. Zip Download
