---
swagger: "2.0"
x-collection-name: Flat
x-complete: 1
info:
  title: Flat
  description: the-flat-api-allows-you-to-easily-extend-the-abilities-of-the-flat-platformhttpsflat-io-with-a-wide-range-of-use-cases-including-the-following-creating-and-importing-new-music-scores-using-musicxml-or-midi-files--browsing-updating-copying-exporting-the-users-scores-for-example-in-mp3-wav-or-midi--managing-educational-resources-with-flat-for-education-creating--updating-the-organization-accounts-the-classes-rosters-and-assignments--the-flat-api-is-built-on-http--our-api-is-restful-it-has-predictable-resource-urls--it-returns-http-response-codes-to-indicate-errors--it-also-accepts-and-returns-json-in-the-http-body--
  termsOfService: https://flat.io/legal
  contact:
    name: Flat
    url: https://flat.io/support
    email: developers@flat.io
  version: 2.1.0
host: api.flat.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{group}/scores:
    get:
      summary: List group's scores
      description: Get the list of scores shared with a group.
      operationId: getGroupScores
      x-api-path-slug: groupsgroupscores-get
      parameters:
      - in: path
        name: group
        description: Unique identifier of the group
      - in: query
        name: parent
        description: Filter the score forked from the score id `parent`
      responses:
        200:
          description: OK
      tags:
      - List
      - Groups
      - Scores
  /scores/{score}:
    get:
      summary: Get a score's metadata
      description: |-
        Get the details of a score identified by the `score` parameter in the URL.
        The currently authenticated user must have at least a read access to the document to use this API call.
      operationId: getScore
      x-api-path-slug: scoresscore-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Scores
      - Metadata
    put:
      summary: Edit a score's metadata
      description: |-
        This API method allows you to change the metadata of a score document (e.g. its `title` or `privacy`), all the properties are optional.

        To edit the file itself, create a new revision using the appropriate method (`POST /v2/scores/{score}/revisions/{revision}`).
      operationId: editScore
      x-api-path-slug: scoresscore-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Scores
      - Metadata
  /users/{user}/likes:
    get:
      summary: List liked scores
      description: ""
      operationId: gerUserLikes
      x-api-path-slug: usersuserlikes-get
      parameters:
      - in: query
        name: ids
        description: Return only the identifiers of the scores
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - List
      - Liked
      - Scores
  /users/{user}/scores:
    get:
      summary: List user's scores
      description: Get the list of scores owned by the User
      operationId: getUserScores
      x-api-path-slug: usersuserscores-get
      parameters:
      - in: query
        name: No Name
      - in: query
        name: parent
        description: Filter the score forked from the score id `parent`
      responses:
        200:
          description: OK
      tags:
      - List
      - Users
      - Scores
---