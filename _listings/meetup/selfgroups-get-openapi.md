---
swagger: "2.0"
x-collection-name: Meetup
x-complete: 0
info:
  title: Meetup Member groups
  description: |-
    Lists the authenticated member's groups in the order of leadership,
    next upcoming event, then alphabetical order by name
  version: 1.0.0
host: api.meetup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /members:
    get:
      summary: Members
      description: API method for accessing members of Meetup Groups
      operationId: deprecated
      x-api-path-slug: members-get
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_id
        description: Return members in groups with these ID numbers, separated by
          commas
        type: string
      - in: query
        name: group_urlname
        description: Return members for the group with the given custom URL path
        type: string
      - in: query
        name: member_id
        description: Return the member with this ID
        type: string
      - in: query
        name: relation
        description: Supply the string self as the value for this parameter to get
          the information of the member linked to the API key making the request
        type: string
      - in: query
        name: service
        description: Match users by the external services theyve linked to their member
          account, specified as servicename:identifier
        type: string
      - in: query
        name: topic,groupnum
        description: Return members for the group with given topic and number
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
      - Members
  /self/blocks/:member_id:
    post:
      summary: Block member
      description: Blocks a target member from various interactions with the authenticated
        member on the platform
      operationId: abuse
      x-api-path-slug: selfblocksmember-id-post
      parameters:
      - in: query
        name: comments
        description: An optional string of text describing why you have chosen to
          block this member
        type: string
      - in: query
        name: report
        description: An optional value that represents a type of abuse the target
          member is being blocked for
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Abuse
      - Members
    delete:
      summary: Unblock member
      description: Unblocks a previously blocked member from various interactions
        with the authenticated member on the platform
      operationId: abuse
      x-api-path-slug: selfblocksmember-id-delete
      responses:
        200:
          description: OK
      tags:
      - Events
      - Abuse
      - Members
  /:urlname/member/approvals:
    post:
      summary: Membership Approval
      description: Approves one or more requests for group membership
      operationId: profiles
      x-api-path-slug: urlnamememberapprovals-post
      parameters:
      - in: query
        name: member
        description: Comma-delimited numeric pending member IDs
        type: string
      - in: query
        name: send_copy
        description: Optional boolean value indicating whether or not the org should
          receive a copy of the message sent to the approved members
        type: string
      - in: query
        name: welcome_message
        description: Optional message to send to the members being approved
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Members
    delete:
      summary: Membership Decline
      description: Declines one or more requests for group membership
      operationId: profiles
      x-api-path-slug: urlnamememberapprovals-delete
      parameters:
      - in: query
        name: anon
        description: Optional Boolean value indicating whether the declining members
          email address should be hidden in the resulting response
        type: string
      - in: query
        name: ban
        description: Optional Boolean value indicating whether or not to ban the member
          in the future
        type: string
      - in: query
        name: explanation
        description: Optional explanation to send to the members being declined
        type: string
      - in: query
        name: member
        description: Comma-delimited numeric pending member IDs
        type: string
      - in: query
        name: send_copy
        description: Optional Boolean value indicating whether or not to send a copy
          to the member issuing the decline
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Members
  /self/events:
    get:
      summary: Member Events
      description: |-
        Gets a listing of all scheduled Meetup Events the authenticated member has RSVP'd to
        that have been announced to the group.
        This listing is ordered from oldest to most recent by default
      operationId: events
      x-api-path-slug: selfevents-get
      parameters:
      - in: query
        name: desc
        description: When true, sorts results in descending order
        type: string
      - in: query
        name: fields
        description: A comma-delimited list of optional fields names which may be
          appended to the response
        type: string
      - in: query
        name: page
        description: Number of results to return
        type: string
      - in: query
        name: rsvp
        description: Comma-delimited list of RSVP responses
        type: string
      - in: query
        name: scroll
        description: A string representing an alias for a point on a timeline
        type: string
      - in: query
        name: status
        description: Comma-delimited list of event statuses
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Members
  /self/calendar:
    get:
      summary: Member Calendar
      description: Get a listing of all upcoming Meetup events for the authenticated
        member
      operationId: events
      x-api-path-slug: selfcalendar-get
      parameters:
      - in: query
        name: fields
        description: A comma-delimited list of optional fields names which may be
          appended to the response
        type: string
      - in: query
        name: page
        description: Number of results to return in a page
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Members
      - Calendardars
  /self/groups:
    get:
      summary: Member groups
      description: |-
        Lists the authenticated member's groups in the order of leadership,
        next upcoming event, then alphabetical order by name
      operationId: groups
      x-api-path-slug: selfgroups-get
      parameters:
      - in: query
        name: fields
        description: A comma-delimited list of optional fields to append to the response
        type: string
      - in: query
        name: page
        description: Number of groups to return in a single page of results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Members
      - Groups
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