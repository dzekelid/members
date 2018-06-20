---
swagger: "2.0"
x-collection-name: CloudFlare
x-complete: 0
info:
  title: CloudFlare Get information about a specific member of an organization
  version: 1.0.0
  description: Get information about a specific member of an organization
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizations/:organization_identifier/members:
    get:
      summary: List all members of a organization
      description: List all members of a organization
      operationId: cloudflare-organization-members-api
      x-api-path-slug: organizationsorganization-identifiermembers-get
      responses:
        200:
          description: OK
      tags:
      - Organization Members
  /organizations/:organization_identifier/members/:identifier:
    delete:
      summary: Remove a member from an organization
      description: Remove a member from an organization
      operationId: cloudflare-organization-members-api
      x-api-path-slug: organizationsorganization-identifiermembersidentifier-delete
      responses:
        200:
          description: OK
      tags:
      - Organization Members
    get:
      summary: Get information about a specific member of an organization
      description: Get information about a specific member of an organization
      operationId: cloudflare-organization-members-api
      x-api-path-slug: organizationsorganization-identifiermembersidentifier-get
      responses:
        200:
          description: OK
      tags:
      - Organization Members
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