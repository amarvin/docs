---
title: "Sync"
linkTitle: "Sync"
description: >
  Learn how to sync a repo with SCM.
---

## Endpoint

```
PATCH  /api/v1/scm/repos/:org/:repo/sync
```

## Parameters

The following parameters are used to configure the endpoint:

| Name   | Description          |
| ------ | -------------------- |
| `org`  | name of organization |
| `repo` | name of repository   |

## Responses

| Status Code | Description                                         |
| ----------- | --------------------------------------------------- |
| `200`       | indicates the request has succeeded                 |
| `401`       | indicates the user does not have proper permissions |

## Sample

{{% alert color="warning" %}}
This section assumes you already know how to authenticate to the API.

To authenticate to the API, please review the [authentication documentation](/docs/reference/api/authentication/).
{{% /alert %}}

#### Request

```sh
curl \
  -X PATCH \
  -H "Authorization: Bearer <token>" \
  "http://127.0.0.1:8080/api/v1/scm/repos/github/octocat/sync"
```

#### Response

```sh
repo "github/octocat" synced
```