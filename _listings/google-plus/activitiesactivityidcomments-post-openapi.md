---
swagger: "2.0"
x-collection-name: Google Plus
x-complete: 0
info:
  title: Google Plus Create Activity Comment
  version: 1.0.0
  description: Create a new comment in reply to an activity.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /activities/{activityId}/comments:
    get:
      summary: Get Activity Comments
      description: List all of the comments for an activity.
      operationId: plus.comments.list
      x-api-path-slug: activitiesactivityidcomments-get
      parameters:
      - in: path
        name: activityId
        description: The ID of the activity to get comments for
      - in: query
        name: maxResults
        description: The maximum number of comments to include in the response, which
          is used for paging
      - in: query
        name: pageToken
        description: The continuation token, which is used to page through large result
          sets
      - in: query
        name: sortOrder
        description: The order in which to sort the list of comments
      responses:
        200:
          description: OK
      tags:
      - Comment
    post:
      summary: Create Activity Comment
      description: Create a new comment in reply to an activity.
      operationId: plusDomains.comments.insert
      x-api-path-slug: activitiesactivityidcomments-post
      parameters:
      - in: path
        name: activityId
        description: The ID of the activity to reply to
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Activity
  /comments/{commentId}:
    get:
      summary: Get Comment
      description: Get a comment.
      operationId: plusDomains.comments.get
      x-api-path-slug: commentscommentid-get
      parameters:
      - in: path
        name: commentId
        description: The ID of the comment to get
      responses:
        200:
          description: OK
      tags:
      - Comment
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