---
name: Meetup
x-slug: meetup
description: Find Meetups so you can do more of what matters to you. Or create your
  own group and meet people near you who share your interests.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
x-kinRank: "9"
x-alexaRank: "902"
tags: Members
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/apis.md
specificationVersion: "0.14"
apis:
- name: Meetup Members
  x-api-slug: meetup
  description: API method for accessing members of Meetup Groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////members
  tags: Events,Groups,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/members-get-openapi.md
- name: Meetup Block member
  x-api-slug: meetup
  description: Blocks a target member from various interactions with the authenticated
    member on the platform
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/blocks/:member_id
  tags: Events,Abuse,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/selfblocksmember-id-post-openapi.md
- name: Meetup Unblock member
  x-api-slug: meetup
  description: Unblocks a previously blocked member from various interactions with
    the authenticated member on the platform
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/blocks/:member_id
  tags: Events,Abuse,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/selfblocksmember-id-delete-openapi.md
- name: Meetup Membership Approval
  x-api-slug: meetup
  description: Approves one or more requests for group membership
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/member/approvals
  tags: Events,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/urlnamememberapprovals-post-openapi.md
- name: Meetup Membership Decline
  x-api-slug: meetup
  description: Declines one or more requests for group membership
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/member/approvals
  tags: Events,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/urlnamememberapprovals-delete-openapi.md
- name: Meetup Member Events
  x-api-slug: meetup
  description: |-
    Gets a listing of all scheduled Meetup Events the authenticated member has RSVP'd to
    that have been announced to the group.
    This listing is ordered from oldest to most recent by default
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/events
  tags: Events,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/selfevents-get-openapi.md
- name: Meetup Member Calendar
  x-api-slug: meetup
  description: Get a listing of all upcoming Meetup events for the authenticated member
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/calendar
  tags: Events,Members,Calendardars
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/selfcalendar-get-openapi.md
- name: Meetup Member groups
  x-api-slug: meetup
  description: |-
    Lists the authenticated member's groups in the order of leadership,
    next upcoming event, then alphabetical order by name
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/groups
  tags: Events,Members,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/selfgroups-get-openapi.md
- name: Meetup
  x-api-slug: meetup
  description: Find Meetups so you can do more of what matters to you. Or create your
    own group and meet people near you who share your interests.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com//
  tags: Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/members/master/_listings/meetup/openapi.md
x-common:
- type: x-base
  url: http://api.meetup.com
- type: x-crunchbase
  url: https://crunchbase.com/organization/meetup
- type: x-developer
  url: http://www.meetup.com/meetup_api/
- type: x-email
  url: privacy@meetup.com
- type: x-email
  url: abuse@meetup.com
- type: x-email
  url: api_license@meetup.com
- type: x-email
  url: arbitration-opt-out@meetup.com
- type: x-email
  url: legal@meetup.com
- type: x-github
  url: https://github.com/meetup
- type: x-pricing
  url: http://www.meetup.com/pricing/
- type: x-privacy
  url: http://www.meetup.com/privacy/
- type: x-support
  url: http://www.meetup.com/help/
- type: x-terms-of-service
  url: http://www.meetup.com/terms/
- type: x-twitter
  url: https://twitter.com/MeetupAPI
- type: x-twitter
  url: https://twitter.com/Meetup
- type: x-website
  url: http://meetup.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---