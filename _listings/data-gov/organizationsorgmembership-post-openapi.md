---
swagger: "2.0"
x-collection-name: Data.Gov
x-complete: 0
info:
  title: Data.gov API Add Organizations Org Membership
  description: Apply for membership to a given organization
  version: "3"
host: catalog.data.gov
basePath: /api/3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizations/{org}/membership/:
    get:
      summary: Get Organizations Org Membership
      description: List membership requests for a given organization
      operationId: getOrganizationsOrgMembership
      x-api-path-slug: organizationsorgmembership-get
      parameters:
      - in: path
        name: org
        description: The organization ID or slug
      - in: query
        name: status
        description: If provided, only return requests ith a given status
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Org
      - Membership
    post:
      summary: Add Organizations Org Membership
      description: Apply for membership to a given organization
      operationId: postOrganizationsOrgMembership
      x-api-path-slug: organizationsorgmembership-post
      parameters:
      - in: path
        name: org
        description: The organization ID or slug
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Org
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