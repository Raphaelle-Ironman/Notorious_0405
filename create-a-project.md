[service-notorious](../../../README.md) / [API](../README.md) / [Projects](./README.md) / Create a project

# Create a project

Create a project and launch an analyse.

```
POST /projects
```

## Body

* `user`: Details of the user the request is being done for. See [User management](../how-to-use/user-management.md),
* `data`:
  * `workspace_id`: ID of the workspace the project is created for,
  * `title`: Title of the project,
  * `query`: Query of the serp to analyze,
  * `language`: Language of the serp to analyze,
  * `page`: Page to improve,
  * `email`: Email to send a notification when the project is finished.

## Example

```
POST /projects
```

```json
{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "data": {
    "id": 1,
    "workspace_id": 5,
    "title": "A title",
    "query": "cat",
    "language": "fr",
    "page": "https://www.cat.com",
    "email": "bobi@mail.fr"
  }
}
```

Response

```
201 Created
```

```json
{
  "id": 1,
  "workspace_id": 5,
  "title": "A title",
  "query": "cat",
  "language": "fr",
  "page": "https://www.cat.com",
  "created_at": "2022-11-30 10:10:10",
  "email": "bobi@mail.fr"
}
```
