---
name: Flat
x-slug: flat
description: Whether youre a beginner or a professional composer, our user-friendly
  music composition software gives you all the tools that you need to make your own
  sheet music. You can write, listen, share and discover music scores right in your
  web browser on any device
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/flat-logo.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Scores
created: "2018-08-26"
modified: "2018-08-26"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/scores/master/_listings/flat/apis.md
specificationVersion: "0.14"
apis:
- name: Flat - List group's scores
  x-api-slug: groupsgroupscores-get
  description: Get the list of scores shared with a group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/flat-logo.png
  humanURL: http://flat.io
  baseURL: https://api.flat.io//v2
  tags: API Provider, Music, Profiles, Relative Data, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/scores/master/_listings/flat/groupsgroupscores-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/scores/master/_listings/flat/groupsgroupscores-get-openapi.md
- name: Flat - Get a score's metadata
  x-api-slug: scoresscore-get
  description: |-
    Get the details of a score identified by the `score` parameter in the URL.
    The currently authenticated user must have at least a read access to the document to use this API call.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/flat-logo.png
  humanURL: http://flat.io
  baseURL: https://api.flat.io//v2
  tags: API Provider, Music, Profiles, Relative Data, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/scores/master/_listings/flat/scoresscore-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/scores/master/_listings/flat/scoresscore-get-openapi.md
- name: Flat - List user's scores
  x-api-slug: usersuserscores-get
  description: Get the list of scores owned by the User
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/flat-logo.png
  humanURL: http://flat.io
  baseURL: https://api.flat.io//v2
  tags: API Provider, Music, Profiles, Relative Data, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/scores/master/_listings/flat/usersuserscores-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/scores/master/_listings/flat/usersuserscores-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://fitbit.api.gallery.streamdata.io
- type: x-api-stack
  url: http://flat.stack.network
- type: x-developer
  url: https://flat.io/developers
- type: x-embeddable
  url: https://flat.io/developers/embed
- type: x-github
  url: https://github.com/FlatIO
- type: x-pricing
  url: https://flat.io/pricing
- type: x-privacy-policy
  url: https://flat.io/help/en/policies/#coppa-and-ferpa-compliance
- type: x-support
  url: https://flat.io/help
- type: x-twitter
  url: https://twitter.com/flat_io
- type: x-website
  url: http://flat.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---