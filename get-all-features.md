[service-notorious](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Get all features

# Get all features

Get all features with their importance level.

```
GET /projects/:id/features
```

## Parameters

| Name | Description        |
|------|--------------------|
| `id` | ID of the project. |

## Example

```
GET /projects/1/features
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
    "project_id": 1,
    "workspace_id": 2,
    "name": "trustflow",
    "score": 0.4,
    "position": 4
  }],
  "count": 10,
  "page": 1,
  "total": 14,
  "pageCount": 2
}
```
