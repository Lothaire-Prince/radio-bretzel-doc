# Radio Bretzel API
### Teams
`/teams`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return teams list

`/<team_name>`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return team infos
UPDATE | / | {"team":"team_name"} | Update team infos
DELETE | / | None | Delete team

`/<team_name>/tracks`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return teams tracks list (pool)
POST/PUT | / | ? | Upload
GET | /<track_id> | None | Return track infos
DELETE | /<track_id> | None | Delete track
UPDATE | /<track_id> | {"infos":[]} | Update track infos


### Users
`/users`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return users list

`/users/<user_id>`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return user infos
UPDATE | / | {"user":"user_name"} | Update user infos
DELETE | / | None | Delete users

`/users/<user_id>/channels`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return user channels list

`/users/<user_id>/active_chats`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return user active chats list

### Channels
`/<team_name>/channels`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return channels list
POST/PUT | / | {"channel":"channel_name"} | Create new channel

`/<team_name>/channels/<channel_name>/`

HTTP verb | URI | Parameters | Description
----------|-----|------------|------------
GET | / | None | Return channel
UPDATE | / | {"channel":"channel_name"} | Update channel infos
DELETE | / | None | Delete channel
POST/PUT | /feed | {"filters":[]} | Feed playlist with matching team tracks
GET | /next | None | Return next track path
GET | /users | None | Return channel users
POST/PUT | /users | {"id":"user_id"}  | Add user to channel
DELETE | /users/<user_id> | None | Delete user from channel
GET | /tracks | None | Return channel playlist tracks
POST/PUT | /tracks | {"id":"tracks_id"}  | Add track to playlist
DELETE | /tracks/<track_id> | None | Delete track from playlist
GET | /historic | None | Return channel historic
POST/PUT | /historic | {"id":"tracks_id"} | Add track to historic
GET | /tags | None | Get channel tags list
POST/PUT | /tags | {"tag":"string"} | Get channel tags list
DELETE | /tags/<tag_id> | None | Delete one tag from channel tags list
