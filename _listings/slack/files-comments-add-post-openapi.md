---
swagger: "2.0"
x-collection-name: Slack
x-complete: 0
info:
  title: Slack Add File Comments
  description: Add a comment to an existing file.
  version: 1.0.3
host: slack.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /files.comments.edit:
    post:
      summary: Edit File Comments
      description: Edit an existing file comment.
      operationId: files_comments_edit
      x-api-path-slug: files-comments-edit-post
      parameters:
      - in: formData
        name: comment
        description: Text of the comment to edit
      - in: formData
        name: file
        description: File containing the comment to edit
      - in: formData
        name: id
        description: The comment to edit
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
      - Comments
  /files.comments.delete:
    post:
      summary: Delete File Comments
      description: Deletes an existing comment on a file.
      operationId: files_comments_delete
      x-api-path-slug: files-comments-delete-post
      parameters:
      - in: formData
        name: file
        description: File to delete a comment from
      - in: formData
        name: id
        description: The comment to delete
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
      - Comments
  /files.comments.add:
    post:
      summary: Add File Comments
      description: Add a comment to an existing file.
      operationId: files_comments_add
      x-api-path-slug: files-comments-add-post
      parameters:
      - in: formData
        name: comment
        description: Text of the comment to add
      - in: formData
        name: file
        description: File to add a comment to
      - in: header
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Files
      - Comments
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