# CARTO-Engine-collection
## a Postman collection for CARTO Engine APIs

This is a training-oriented collection and environment for using with Postman. It includes the most typical API interaction use cases. 

### configure the collection 

The collection is pretty much autoconfigured, but in order to use it, there are some adjustments that need to be done:

- [ ] Import collection and environment to Postman
- [ ] Set environment variables:
  - [ ] `USER`: your CARTO username
  - [ ] `KEY` : your CARTO account's API key

	- [ ] **Only for Enterprise API**
	  - [ ] `ORG`: your organization name
	  - [ ] `ORG_OWNER`: your organization's owner username
	  - [ ] `OWNER_KEY`: your organization's owner's API key

That's it. 

### configured tests

There are some actions already configured in the collection. These actions will update certain environment variables according to data received in the response. For example: 

```javascript
var jsonData = JSON.parse(responseBody);

postman.setEnvironmentVariable("LAYERGROUPID", jsonData.layergroupid);
```

It will take `layergroupid` from the Import API call's response and set `LAYERGROUPID` environment variable accordingly.

Similar tests are configured for: 

- Import a file
- Instantiate an anonymous map
- Create a SQL Batch API job
- Create a new Org. user


