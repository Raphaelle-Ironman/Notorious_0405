[service-blitzlink](../../../README.md) / [API](../README.md) / [Projects](./README.md) / 
Export backlinks

# Export backlinks by project

Export all backlinks in csv.

```
GET /projects/:idProject/export-backlinks
```

## Parameters

| Name         | Description        |
|--------------|--------------------|
| `id_project` | ID of the project. |
| `id_url`     | ID of the url.     |

## Queries

`ids[]` : id of the backlinks to export. Must be repeat to have multiple backlinks
  

## Example

```
GET /projects/3/export-backlinks?ids[]=3&ids[]=5
```

```json
{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response

```
200 OK
```

```csv
domain,position,tf_domain,cf_domain,ext_backlinks,domain_rating,refdom_domain,traffic_domain,principal_topic,secondary_topic,tertiary_topic,health,page_value,page_trust,domain_backlinks,bas,fame
bobi.com,null,17,46,98417,56,null,654437,Business,Computers/Software/Operating Systems,null,null,null,null,null,null,0
jardin.com,null,20,24,14430,53,null,1043937,Shopping/Recreation,Computers/Multimedia,null,66,61,13,521,35,0
jardineur.com,20,15,38,185787,65,15032,null,Business,Shopping/Home and Garden,Science/Biology,0,53,11,2230,34,0
```