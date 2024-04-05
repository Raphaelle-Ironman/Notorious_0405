[service-notorious](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get a project

# Get a project

Get a project by id.

```
GET /projects/:id
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Example

```
GET /projects/3
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
  "id": 3,
  "workspace_id": 5,
  "title": "A title",
  "query": "cat",
  "language": "fr",
  "customer_page": "https://www.cat.com",
  "date_created": "2022-11-30 10:10:10",
  "email": "bobi@mail.fr",
  "is_done": true,
  "is_finish": true,
  "is_all_recup": true,
  "f1_accuracy": 0,
  "error": false,
  "error_state": null
  "fametop10": 417.7,
  "estimatedtop10": 4594.7,
  "fametop3": 440.91,
  "estimatedtop3": 4850.01,
  "budgettop3": {
    "min": 6000,
    "max": 10000,
    "difficulty": "MEDIUM"
  },
  "budgettop10": {
    "min": "-Infinity",
    "max": 1000,
    "difficulty": "EASY"
  },
  "dashboard": {
    "top10": {
      "tf_page": 12,
      "tf_domain": 27.5,
      "domain-rating": 74.5,
      "refdom_page": 5,
      "refdom_domain": 12006.5,
      "traffic_domain": 748322,
      "brand_volume": 1700,
      "cf_page": 22,
      "cf_domain": 54
    },
    "top3": {
      "tf_page": 12,
      "tf_domain": 42,
      "domain-rating": 80,
      "refdom_page": 8,
      "refdom_domain": 190709,
      "traffic_domain": 2487539,
      "brand_volume": 4700,
      "cf_page": 16,
      "cf_domain": 57
    },
    "client": {
      "position": 38,
      "tf_page": 0,
      "tf_domain": 41,
      "domain_rating": 47,
      "refdom_page": 2,
      "refdom_domain": 1028,
      "traffic_domain": 19794,
      "brand_volume": 14800,
      "cf_page": 19,
      "cf_domain": 31
    }
  }
}
```
