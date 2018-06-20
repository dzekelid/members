---
swagger: "2.0"
x-collection-name: ClimaCell
x-complete: 0
info:
  title: ClimaCell Get Groups Group Members
  description: |-
    ### List all Group Members
    Page through a list of all members of a group with a ```group_id```. You can specify the maximum number of results to be retuned, and from which result to start.
  version: 1.0.0
host: api2.climacell.co
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{group_id}/members:
    get:
      summary: Get Groups Group Members
      description: |-
        ### List all Group Members
        Page through a list of all members of a group with a ```group_id```. You can specify the maximum number of results to be retuned, and from which result to start.
      operationId: -list-all-group-memberspage-through-a-list-of-all-members-of-a-group-with-a-group-id-you-can-specify
      x-api-path-slug: groupsgroup-idmembers-get
      parameters:
      - in: path
        name: group_id
        description: UUID of the Group
      - in: query
        name: limit
        description: The maximum number of records to load
      - in: query
        name: offset
        description: The number of records to skip
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Groups
      - Group
      - Members
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