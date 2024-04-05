[service-notorious](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get serp's pages

# Get serp's pages

Get serp's pages with metrics from query in projects.

```
GET /projects/:id/serp-pages
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Example

```
GET /projects/4/serp-pages
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

```json
{
  "data": [{
    "id": 10,
    "project_id": 4,
    "workspace_id": 5,
    "page": "https://www.cat.com",
    "position": 2,
    "metrics" : {
      "tf_page": 15,
      "tf_domain": 20,
      "cf_page": 15,
      "cf_domain": 10,
      "ips_page": 10,
      "ips_domain": 11,
      "domain_rating": 30,
      "refdom_page": 1000,
      "refdom_domain": 1000,
      "traffic_domain": 1000,
      "pricipal_topic": "Arts/Movies",
      "secondary_topic": "Business/Business Services",
      "tertiary_topic": "Regional/Europe",
      "pricipal_topic_domain": "Arts/Movies",
      "secondary_topic_domain": "Business/Business Services",
      "tertiary_topic_domain": "Regional/Europe",
      "health": 90,
      "page_value": 50,
      "page_trust": 50,
      "semantic_value": 50,
      "domain_backlinks": 50,
      "bas": 50
    }
  }],
  "error": false,
  "count": 10,
  "page": 1,
  "total": 101,
  "pageCount": 11
}
```
