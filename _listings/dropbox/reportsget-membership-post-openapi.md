---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 0
info:
  title: Cloud Elements - Dropbox For Business API Get Membership
  description: Get membership.
  version: "1"
host: api.dropbox.com
basePath: /1/team
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /members/list:
    post:
      summary: List Members
      description: List members.
      operationId: postMembersList
      x-api-path-slug: memberslist-post
      parameters:
      - in: query
        name: cursor
        description: optional encoded value indicating from what point to get the
          next limit members
      - in: query
        name: limit
        description: optional number of results to return per call (default 1000,
          maximum 1000)
      responses:
        200:
          description: OK
      tags:
      - List
      - Members
  /reports/get_membership:
    post:
      summary: Get Membership
      description: Get membership.
      operationId: postReportsGetMembership
      x-api-path-slug: reportsget-membership-post
      parameters:
      - in: query
        name: end_date
        description: optional ending date (exclusive)
      - in: query
        name: start_date
        description: optional starting date (inclusive)
      responses:
        200:
          description: OK
      tags:
      - Membership
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---