---
swagger: "2.0"
x-collection-name: CloudFlare
x-complete: 1
info:
  title: CloudFlare
  version: 1.0.0
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
    patch:
      summary: Change the Roles of an Organization&#39;s Member
      description: Change the Roles of an Organization&#39;s Member
      operationId: cloudflare-organization-members-api
      x-api-path-slug: organizationsorganization-identifiermembersidentifier-patch
      parameters:
      - in: query
        name: roles
        description: Array of Roles associated with this Membertttttttttttttt[3536bcfad5faccb999b47003c79917fb]
      - in: header
        name: X-AUTH-EMAIL
        description: Email address associated with your account
      - in: header
        name: X-AUTH-KEY
        description: API key generated on the My Account page
      responses:
        200:
          description: OK
      tags:
      - Organization Members
---