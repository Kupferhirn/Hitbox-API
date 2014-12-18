# Facebook API
***

| Endpoint | Description |
| ---- | --------------- |
| [GET /facebook/pages](/facebook/index.md#get-facebookpages) | Return facebook pages associated with the linked facebook account |
| [POST /facebook/pages](/facebook/index.md#post-facebookpages) | Modify `selected` value on facebook pages |
| [POST /facebook/post](/facebook/index.md#post-facebookpost) | Send message to `selected` facebook pages |

## `GET /facebook/pages`

Returns associated facebook pages. `id` is the Facebook Page ID 

| Parameter | Required? | Type | Description |
| --- | --- | --- | --- |
| authToken | Yes | string | User's Auth Token |
| user_name | Yes | string | User's username |

### Example URL

https://www.hitbox.tv/api/facebook/pages

### Example Response 

```json
{
   "pages":[
      {
         "id":"111111111",
         "name":"Not Selected Facebook Page",
         "access_token":"facebook_oauth_token",
         "selected":"0"
      },
      {
         "id":"22222222",
         "name":"Selected Facebook Page",
         "access_token":"facebook_oauth_token",
         "selected":"1"
      }
   ]
}
```

## `POST /facebook/pages`

Modify which page(s) are used for posting to. Yes, You only need to post `id` and `selected`.

| Parameter | Required? | Type | Description |
| --- | --- | --- | --- |
| authToken | Yes | string | User's Auth Token |
| user_name | Yes | string | User's username |

### Example POST Payload

```json
{
   "pages":[
      {
         "id":"3333333",
         "selected":1
      },
      {
         "id":"2222222",
         "selected":0
      },
      {
         "id":"11111111",
         "selected":0
      }
   ]
}
```

### Example Response

```json
success
```

## `POST /facebook/post`

Sends a message to the `selected` facebook pages from [/facebook/pages](/facebook/index.md#post-facebookpages)

| POST Data | Required? | Type | Description |
| --- | --- | --- | --- |
| authToken | Yes | string | User's Auth Token |
| user_name | Yes | string | User's username |
| message | Yes | string | Messsage |

### Example Response

Even if it's successful
```json
post_failed
```