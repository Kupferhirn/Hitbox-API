<<<<<<< HEAD:media/status/index.md
# Media Status API
=======
#Media Status API 
>>>>>>> origin/org:media/status.md
***

| Endpoint | Description |
| ---- | --------------- |
| [GET /media/status/:channel](/media/status.md#get-mediastatuschannel) | Returns simple information about the stream. |

## `GET /media/status/:channel`

Returns live status and viewers. (Viewer count is delayed)

### Example URL

https://www.hitbox.tv/api/media/status/test-account

### Example Response 

```json
{
  "media_is_live":"1",
  "media_views":"1111"
}
```