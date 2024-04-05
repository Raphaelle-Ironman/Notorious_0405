[service-notorious](../../../README.md) / [API](../README.md) / [How to use](./README.md) / Pagination

# Pagination

# Pagination

Results of requests with list have a pagination system. The page number can be selected with the
key `page` in json query field `q`. The reponse's body `pagination` property give information about the total number
of pages, the number of elements by pages and the current page.
The number of entries by page can be selected by the key `amount` in json query field `q`.

## Example

```
GET /projects?q={"page":1,"amount":150}
```

```
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
