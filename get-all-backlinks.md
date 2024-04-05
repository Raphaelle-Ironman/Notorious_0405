[service-notorious](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get all backlinks

# Get all backlinks

Get all backlinks and metrics of the project.

```
GET /projects/:id/backlinks
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Example

```
GET /projects/3/backlinks
```

```json
{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "admin"
  }
}
```

Response

```
200 OK
```

```json
{
  "data": [{
    "id": 1,
    "project_id": 3,
    "workspace_id": 5,
    "domain": "https://www.cat.com",
    "position": 1,
    "metrics": {
      "tf": 15,
      "cf": 10,
      "ext_backlinks": 11,
      "domain_rating": 30,
      "refdom_page": 1000,
      "refdom_domain": 1000,
      "traffic_domain": 1000,
      "pricipal_topic": "Arts/Movies",
      "secondary_topic": "Business/Business Services",
      "tertiary_topic": "Regional/Europe",
      "health": 90,
      "page_value": 50,
      "page_trust": 50,
      "semantic_value": 50,
      "domain_backlinks": 50,
      "bas": 50
    },
    "fame": 234
  }],
  "error": false,
  "count": 10,
  "page": 1,
  "total": 134,
  "pageCount": 14
}
```
