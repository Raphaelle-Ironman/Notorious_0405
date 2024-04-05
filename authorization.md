[service-notorious](../../../README.md) / [API](../README.md) / [How to use](./README.md) / Authorization

# Authorization

Each request must be authenticated with the `API_KEY` environment variable as a bearer access token.

> [!IMPORTANT]
> The token must be base64 encoded.

## Example

```
GET /projects
authorization: Token WW91IGFyZSB0b28gY3VyaW91cw==
```

```json
{
  "user": {
    "id": 1,
    "workspaces": [],
    "role": "admin"
  }
}
```
