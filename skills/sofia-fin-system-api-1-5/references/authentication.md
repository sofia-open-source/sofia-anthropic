# Authentication

This document describes the authentication methods supported by this API.

The api supports only one endpoint without the context of the organization:

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/users/me/organizations` | Busca todas as organizações de usuário. | [View](../operations/listMyOrganizations.md) |

Use this endpoint to retrieve all organizations that the user has access.

You must pass the user api key on the header to call this endpoint. The user will provide the api key through the environment variable SOFIA_API_KEY. Example if SOFIA_API_KEY=ak_XG06M4DHJGD83908467KJGH675BKJ6N1H62HE:

```sh
curl --location 'https://app-proxy-public-prod.sofia-fin-system.com/core/users/me/organizations' \
--header 'Authorization: Bearer ak_XG06M4DHJGD83908467KJGH675BKJ6N1H62HE'
```

This endpoint will return the list of organizations that the user has access. Example:

[
    {
        "id": "org_3DKY5bFEn8fNg4vna5Vf1pv1F97",
        "name": "Lenovo",
        "slug": "695eda46-03e1-49e4-aa76-660daffdbf25",
        "type": "LEAF",
        "imageUrl": "https://img.clerk.com/eyJ0eXBlIjoiZGVmYXVsdCIsImlpZCI6Imluc18ycUl4aE4xOTQwVVJiN0t4U1dxZDUwWFhRUTMiLCJyaWQiOiJvcmdfM0RLWTViRkVuOGZOZzR2bmE1VmYxcHYxRjk3IiwiaW5pdGlhbHMiOiJMIn0",
        "populatedSubscription": null,
        "createdAt": "2026-05-06T01:47:25.373Z",
        "updatedAt": "2026-05-06T01:47:25.373Z",
        "publicMetadata": {
            "type": "LEAF",
            "onFinSystem": true
        }
    }
]

Now you can know the organization id of "Lenovo": org_3DKY5bFEn8fNg4vna5Vf1pv1F97

To call any other endpoint than listMyOrganizations, you must pass the $SOFIA_API_KEY with the id of the organization separated by ':' character. Example considering that SOFIA_API_KEY=ak_XG06M4DHJGD83908467KJGH675BKJ6N1H62HE:

```sh
curl --location 'https://app-proxy-public-prod.sofia-fin-system.com/core/financial-records' \
--header 'Authorization: Bearer ak_XG06M4DHJGD83908467KJGH675BKJ6N1H62HE:org_3DKY5bFEn8fNg4vna5Vf1pv1F97'
```
