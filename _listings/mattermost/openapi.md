---
swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost API Reference
  description: -api-v4-is-stable-with-the-mattermost-server-4-0-release--api-v3-was-deprecated-on-january-16th-2018-and-scheduled-for-removal-in-mattermost-v5-0--details-heretagapiv3deprecation--looking-for-the-api-v3-reference-it-has-moved-herehttpsapi-mattermost-comv3-
  termsOfService: https://about.mattermost.com/default-terms/
  version: 4.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /teams/{team_id}/members:
    get:
      summary: Get team members
      description: |-
        Get a page team members list based on query string parameters - team id, page and per page.
        ##### Permissions
        Must be authenticated and have the `view_team` permission.
      operationId: get-a-page-team-members-list-based-on-query-string-parameters--team-id-page-and-per-page-permissions
      x-api-path-slug: teamsteam-idmembers-get
      parameters:
      - in: query
        name: page
        description: The page to select
      - in: query
        name: per_page
        description: The number of users per page
      - in: path
        name: team_id
        description: Team GUID
      responses:
        200:
          description: OK
      tags:
      - Team
      - Members
  /users/{user_id}/teams/members:
    get:
      summary: Get team members for a user
      description: |-
        Get a list of team members for a user. Useful for getting the ids of teams the user is on and the roles they have in those teams.
        ##### Permissions
        Must be logged in as the user or have the `edit_other_users` permission.
      operationId: get-a-list-of-team-members-for-a-user-useful-for-getting-the-ids-of-teams-the-user-is-on-and-the-rol
      x-api-path-slug: usersuser-idteamsmembers-get
      parameters:
      - in: path
        name: user_id
        description: User GUID
      responses:
        200:
          description: OK
      tags:
      - Team
      - Membersa
      - User
  /teams/{team_id}/members/ids:
    post:
      summary: Get team members by ids
      description: |-
        Get a list of team members based on a provided array of user ids.
        ##### Permissions
        Must have `view_team` permission for the team.
      operationId: get-a-list-of-team-members-based-on-a-provided-array-of-user-ids-permissionsmust-have-view-team-perm
      x-api-path-slug: teamsteam-idmembersids-post
      parameters:
      - in: body
        name: body
        description: List of user ids
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: team_id
        description: Team GUID
      responses:
        200:
          description: OK
      tags:
      - Team
      - Members
      - By
      - Ids
  /channels/{channel_id}/members:
    get:
      summary: Get channel members
      description: |-
        Get a page of members for a channel.
        ##### Permissions
        `read_channel` permission for the channel.
      operationId: get-a-page-of-members-for-a-channel-permissionsread-channel-permission-for-the-channel
      x-api-path-slug: channelschannel-idmembers-get
      parameters:
      - in: path
        name: channel_id
        description: Channel GUID
      - in: query
        name: page
        description: The page to select
      - in: query
        name: per_page
        description: The number of members per page
      responses:
        200:
          description: OK
      tags:
      - Channel
      - Members
  /channels/{channel_id}/members/ids:
    post:
      summary: Get channel members by ids
      description: |-
        Get a list of channel members based on the provided user ids.
        ##### Permissions
        Must have the `read_channel` permission.
      operationId: get-a-list-of-channel-members-based-on-the-provided-user-ids-permissionsmust-have-the-read-channel-p
      x-api-path-slug: channelschannel-idmembersids-post
      parameters:
      - in: path
        name: channel_id
        description: Channel GUID
      - in: body
        name: user_ids
        description: List of user ids
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Channel
      - Members
      - By
      - Ids
  /users/{user_id}/teams/{team_id}/channels/members:
    get:
      summary: Get channel members for user
      description: |-
        Get all channel members on a team for a user.
        ##### Permissions
        Logged in as the user and `view_team` permission for the team. Having `manage_system` permission voids the previous requirements.
      operationId: get-all-channel-members-on-a-team-for-a-user-permissionslogged-in-as-the-user-and-view-team-permissi
      x-api-path-slug: usersuser-idteamsteam-idchannelsmembers-get
      parameters:
      - in: path
        name: team_id
        description: Team GUID
      - in: path
        name: user_id
        description: User GUID
      responses:
        200:
          description: OK
      tags:
      - Channel
      - Membersuser
---