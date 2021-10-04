---
title: "directory resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# directory resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[Get directory](../api/directory-get.md)|[directory](../resources/directory.md)|Read the properties and relationships of a [directory](../resources/directory.md) object.|
|[Update directory](../api/directory-update.md)|[directory](../resources/directory.md)|Update the properties of a [directory](../resources/directory.md) object.|
|[List administrativeUnits](../api/directory-list-administrativeunits.md)|[administrativeUnit](../resources/administrativeunit.md) collection|Get the administrativeUnit resources from the administrativeUnits navigation property.|
|[Create administrativeUnit](../api/directory-post-administrativeunits.md)|[administrativeUnit](../resources/administrativeunit.md)|Create a new administrativeUnit object.|
|[List deletedItems](../api/directory-list-deleteditems.md)|[directoryObject](../resources/directoryobject.md) collection|Get the directoryObject resources from the deletedItems navigation property.|
|[Create deletedItems](../api/directory-post-deleteditems.md)|[directoryObject](../resources/directoryobject.md)|Create a new directoryObject object.|
|[List federationConfigurations](../api/directory-list-federationconfigurations.md)|[identityProviderBase](../resources/identityproviderbase.md) collection|Get the identityProviderBase resources from the federationConfigurations navigation property.|
|[Create identityProviderBase](../api/directory-post-federationconfigurations.md)|[identityProviderBase](../resources/identityproviderbase.md)|Create a new identityProviderBase object.|
|[List sharedEmailDomains](../api/directory-list-sharedemaildomains.md)|[sharedEmailDomain](../resources/sharedemaildomain.md) collection|Get the sharedEmailDomain resources from the sharedEmailDomains navigation property.|
|[Create sharedEmailDomain](../api/directory-post-sharedemaildomains.md)|[sharedEmailDomain](../resources/sharedemaildomain.md)|Create a new sharedEmailDomain object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|administrativeUnits|[administrativeUnit](../resources/administrativeunit.md) collection|**TODO: Add Description**|
|attributeSets|[attributeSet](../resources/attributeset.md) collection|**TODO: Add Description**|
|customSecurityAttributeDefinitions|[customSecurityAttributeDefinition](../resources/customsecurityattributedefinition.md) collection|**TODO: Add Description**|
|deletedItems|[directoryObject](../resources/directoryobject.md) collection|**TODO: Add Description**|
|eligibleRoleAssignments|[eligibleRoleAssignment](../resources/eligibleroleassignment.md) collection|**TODO: Add Description**|
|federationConfigurations|[identityProviderBase](../resources/identityproviderbase.md) collection|**TODO: Add Description**|
|groupProxies|[groupProxy](../resources/groupproxy.md) collection|**TODO: Add Description**|
|sharedEmailDomains|[sharedEmailDomain](../resources/sharedemaildomain.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directory",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.directory"
}
```

