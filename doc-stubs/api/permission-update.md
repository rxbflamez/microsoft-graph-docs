---
title: "Update permission"
description: "Update the properties of a permission object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update permission
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [permission](../resources/permission.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /shares/{sharesId}/permission
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [permission](../resources/permission.md) object.

The following table shows the properties that are required when you update the [permission](../resources/permission.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|expirationDateTime|DateTimeOffset|**TODO: Add Description**|
|grantedTo|[identitySet](../resources/intune-identityset.md)|**TODO: Add Description**|
|grantedToIdentities|[identitySet](../resources/intune-identityset.md) collection|**TODO: Add Description**|
|grantedToV2|[sharePointIdentitySet](../resources/sharepointidentityset.md)|**TODO: Add Description**|
|grantedToIdentitiesV2|[sharePointIdentitySet](../resources/sharepointidentityset.md) collection|**TODO: Add Description**|
|hasPassword|Boolean|**TODO: Add Description**|
|inheritedFrom|[itemReference](../resources/itemreference.md)|**TODO: Add Description**|
|invitation|[sharingInvitation](../resources/sharinginvitation.md)|**TODO: Add Description**|
|link|[sharingLink](../resources/sharinglink.md)|**TODO: Add Description**|
|roles|String collection|**TODO: Add Description**|
|shareId|String|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [permission](../resources/permission.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_permission"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/shares/{sharesId}/permission
Content-Type: application/json
Content-length: 788

{
  "@odata.type": "#microsoft.graph.permission",
  "expirationDateTime": "String (timestamp)",
  "grantedTo": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "grantedToIdentities": [
    {
      "@odata.type": "microsoft.graph.identitySet"
    }
  ],
  "grantedToV2": {
    "@odata.type": "microsoft.graph.sharePointIdentitySet"
  },
  "grantedToIdentitiesV2": [
    {
      "@odata.type": "microsoft.graph.sharePointIdentitySet"
    }
  ],
  "hasPassword": "Boolean",
  "inheritedFrom": {
    "@odata.type": "microsoft.graph.itemReference"
  },
  "invitation": {
    "@odata.type": "microsoft.graph.sharingInvitation"
  },
  "link": {
    "@odata.type": "microsoft.graph.sharingLink"
  },
  "roles": [
    "String"
  ],
  "shareId": "String"
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.permission",
  "id": "892a085e-085e-892a-5e08-2a895e082a89",
  "expirationDateTime": "String (timestamp)",
  "grantedTo": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "grantedToIdentities": [
    {
      "@odata.type": "microsoft.graph.identitySet"
    }
  ],
  "grantedToV2": {
    "@odata.type": "microsoft.graph.sharePointIdentitySet"
  },
  "grantedToIdentitiesV2": [
    {
      "@odata.type": "microsoft.graph.sharePointIdentitySet"
    }
  ],
  "hasPassword": "Boolean",
  "inheritedFrom": {
    "@odata.type": "microsoft.graph.itemReference"
  },
  "invitation": {
    "@odata.type": "microsoft.graph.sharingInvitation"
  },
  "link": {
    "@odata.type": "microsoft.graph.sharingLink"
  },
  "roles": [
    "String"
  ],
  "shareId": "String"
}
```
