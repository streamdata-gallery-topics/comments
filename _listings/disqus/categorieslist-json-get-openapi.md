---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Categories List
  description: Categories List
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /aet/dismiss.json:
    post:
      summary: Aet Dismiss
      description: Aet Dismiss
      operationId: aet-dismiss
      x-api-path-slug: aetdismiss-json-post
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
  /aet/export.json:
    post:
      summary: Aet Export
      description: Aet Export
      operationId: aet-export
      x-api-path-slug: aetexport-json-post
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name) You must be a moderator
          on the selected forum
        type: string
      - in: query
        name: full
        description: Defaults to false                         If true, export all
          emails collected so far
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
  /aet/pendingExportInfo.json:
    get:
      summary: Aet PendingExportInfo
      description: Aet PendingExportInfo
      operationId: aet-pendingexportinfo
      x-api-path-slug: aetpendingexportinfo-json-get
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Export
  /aet/subscribe.json:
    post:
      summary: Aet Subscribe
      description: Aet Subscribe
      operationId: aet-subscribe
      x-api-path-slug: aetsubscribe-json-post
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
  /blacklists/backfillCounters.json:
    post:
      summary: Blacklists BackfillCounters
      description: Blacklists BackfillCounters
      operationId: blacklists-backfillcounters
      x-api-path-slug: blacklistsbackfillcounters-json-post
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Black Lists
  /blacklists/list.json:
    get:
      summary: Blacklists List
      description: Blacklists List
      operationId: blacklists-list
      x-api-path-slug: blacklistslist-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: query
        description: Defaults to null
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      - in: query
        name: type
        description: 'Defaults to null                         Choices: domain, word,
          ip, user, thread_slug, email'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Black Lists
  /blacklists/remove.json:
    post:
      summary: Blacklists Remove
      description: Blacklists Remove
      operationId: blacklists-remove
      x-api-path-slug: blacklistsremove-json-post
      parameters:
      - in: query
        name: domain
        description: Defaults to []                         Domain Name
        type: string
      - in: query
        name: email
        description: Defaults to []                         Email address (defined
          by RFC 5322)
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: ip
        description: Defaults to []                         IP address in CIDR notation
        type: string
      - in: query
        name: user
        description: Defaults to []                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      - in: query
        name: word
        description: Defaults to []                         Maximum length of 200
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Black Lists
  /categories/details.json:
    get:
      summary: Categories Details
      description: Categories Details
      operationId: categories-details
      x-api-path-slug: categoriesdetails-json-get
      parameters:
      - in: query
        name: category
        description: Looks up a category by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
  /categories/list.json:
    get:
      summary: Categories List
      description: Categories List
      operationId: categories-list
      x-api-path-slug: categorieslist-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
x-streamrank:
  polling_total_time_average: "0.1"
  polling_size_download_average: "89"
  streaming_total_time_average: "0.05"
  streaming_size_download_average: "48.5"
  change_yes: "2"
  change_no: "0"
  time_percentage: "49"
  size_percentage: "46"
  change_percentage: "100"
  last_run: "2018-05-04"
  days_run: "0"
  minute_run: "0"
---