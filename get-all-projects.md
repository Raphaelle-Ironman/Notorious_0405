[service-notorious](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get all projects

# Get all projects

Returns all projects.

```
GET /projects
```

## Query fields

| Name           | Description                                          |
|:---------------|:-----------------------------------------------------|
| `workspace-id` | Returns only the projects related to this workspace. |

## Example

```
GET /projects?workspace-id=5
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
    "id": 1,
    "created_by_id": 4,
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
    }
  }, {
    "id": 2,
    "workspace_id": 5,
    "title": "A new Title",
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
    }
  }],
  "count": 126,
  "page": 1,
  "total": 126,
  "pageCount": 1
}
```
