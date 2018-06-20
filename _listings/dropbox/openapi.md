---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 1
info:
  title: Dropbox for Business API
  description: the-business-version-of-the-dropbox-api-
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
---