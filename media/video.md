# Video API
***

| Endpoint | Description |
| ---- | --------------- |
| [GET /media/video/:user/list](/media/video.md#get-mediavideouserlist) | Return VOD data |

## `GET /media/video/:user/list`

Returns VOD data for the user. Some parameters overlap, no clue which overrides which.

| Parameter | Required? | Type | Description |
| --- | --- | --- | --- |
| authToken | Yes | string | User's Auth Token |
| filter | No | recent,popular | Video Filter |
| hiddenOnly | No | boolean | Shows only private VODs |
| limit | No | integer | Default: 100 Max: ?; Limits amount of VODs given |
| liveonly | No | boolean | Default: False; Use: ? |
| nocache | No | boolean | Server Side Switch, Gives fresh data |
| publicOnly | No | boolean | Shows only public VODs only |
| search | No | string | Search titles of VODs |
| showHidden | No | boolean | Shows or Hide private VODs |
| yt | No | boolean | Shows only yt VODs |

### Example URL

https://www.hitbox.tv/api/media/video/:user/list

### Example Response 
```json
{
   "request":{
      "this":"\/media\/video\/test-account\/list"
   },
   "media_type":"video",
   "authToken":"1232131",
   "video":[
      {
         "media_user_name":"test-account",
         "media_id":"229802214",
         "media_type_id":"2",
         "media_user_id":"27873323",
         "media_category_id":"2433650",
         "media_file":"f7fad5547948ec921167c0c748cde7edd88c5d9f-53f8dcd26bc06",
         "media_profiles":"[{\"url\":\"\\\/test-account\\\/f7fad55432432ec921167c0c748cde7edd88c5d9f-53f8dcd26bc06\\\/test-account\\\/index.m3u8\",\"height\":\"720\",\"bitrate\":0}]",
         "media_host":null,
         "media_rec_session":null,
         "media_ingest_host":null,
         "media_is_live":"1",
         "media_live_delay":"0",
         "media_featured":null,
         "media_privacy":null,
         "media_hidden":"1",
         "media_notify_users":"1",
         "media_date_added":"2014-08-23 18:36:54",
         "media_date_updated":null,
         "media_live_since":null,
         "media_live_notified":null,
         "media_key":"432432",
         "media_chat_enabled":"1",
         "media_deleted":null,
         "media_playing":"1",
         "media_transcoding":null,
         "media_recording":null,
         "media_dvr":"0",
         "media_countries":null,
         "media_info":null,
         "media_relay":null,
         "media_password":null,
         "media_yt_upload":null,
         "media_yt_upload_status":null,
         "media_processing":null,
         "media_total_views":"8",
         "media_monthly_views":"2",
         "media_weekly_views":"0",
         "media_daily_views":"0",
         "media_featured_weight":null,
         "media_featured_forced":null,
         "media_featured_countries":null,
         "media_name":"f7fad55479432432432432432111de7edd88c5d9f-53f8dcd26bc06",
         "media_display_name":"test-account",
         "media_status":"Testing Microvolts (720p, 60FPS. 1700Bitrate) - Aug 23rd #6",
         "media_title":"Testing Microvolts (720p, 60FPS. 1700Bitrate) - Aug 23rd #6",
         "media_tags":"",
         "media_duration":"295.0000",
         "media_bg_image":null,
         "media_views":"8",
         "media_views_daily":"0",
         "media_views_weekly":"0",
         "media_views_monthly":"2",
         "category_id":"24650",
         "category_name":"MicroVolts",
         "category_name_short":null,
         "category_seo_key":"microvolts",
         "category_viewers":"2",
         "category_media_count":"1",
         "category_channels":null,
         "category_logo_small":null,
         "category_logo_large":"\/static\/img\/games\/2198350-microvolts_logo.jpg",
         "category_updated":"2014-12-13 20:40:22",
         "team_name":"TheBestTeam",
         "media_start_in_sec":"0",
         "media_download_link":"http:\/\/edge.bf.hitbox.tv\/download\/\/test-account\/f7fad3232348ec921167c0c748cde7edd88c5d9f-53f8dcd26bc06\/test-account\/index.m3u8?h=1Wdqn7PSvlE8kWQKC4XICA&e=1418815005",
         "media_duration_format":"00:04:55",
         "media_thumbnail":"\/static\/img\/media\/videos\/f7f\/f7fad5547321312167c0c748cde7edd88c5d9f-53f8dcd26bc06_mid_000.jpg",
         "media_thumbnail_large":"\/static\/img\/media\/videos\/f7f\/f7fad5321328ec921167c0c748cde7edd88c5d9f-53f8dcd26bc06_large_000.jpg",
         "channel":{
            "followers":"7",
            "user_id":"21312",
            "user_name":"test-account",
            "user_status":"1",
            "user_logo":"\/static\/img\/channel\/test-account_53f4e837eb388_large.png",
            "user_cover":"\/static\/img\/channel\/cover_53fbf06572c78.png",
            "user_logo_small":"\/static\/img\/channel\/test-account_53f4e837eb388_small.png",
            "user_partner":null,
            "media_is_live":"0",
            "media_live_since":"2014-12-14 05:18:54",
            "twitter_account":"test-account",
            "twitter_enabled":"0",
            "livestream_count":"1"
         }
      }
   ]
}
```