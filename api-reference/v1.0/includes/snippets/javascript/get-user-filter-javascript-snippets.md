---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let users = await client.api('/users?$count=true&ConsistencyLevel=eventual&$filter=endsWith(mail,\'@contoso.com\')')
	.filter('endsWith(mail,\'@contoso.com\')')
	.get();

```