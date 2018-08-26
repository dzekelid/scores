---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Post User Scores
  description: Posts a score for the user
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{application}/scores:
    get:
      summary: Get Application Scores
      description: Scores for the user and their friends.
      operationId: getApplicationScores
      x-api-path-slug: applicationscores-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Scores
    delete:
      summary: Delete Application Scores
      description: Deletes all the scores for the application.
      operationId: deleteApplicationScores
      x-api-path-slug: applicationscores-delete
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Scores
  /{user}/scores:
    get:
      summary: Get User Scores
      description: The scores for the user
      operationId: getUserScores
      x-api-path-slug: userscores-get
      parameters:
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Scores
    post:
      summary: Post User Scores
      description: Posts a score for the user
      operationId: postUserScores
      x-api-path-slug: userscores-post
      parameters:
      - in: query
        name: score
        description: Numeric score with value < 0
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Scores
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