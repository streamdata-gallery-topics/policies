---
swagger: "2.0"
x-collection-name: AWS Key Management Service
x-complete: 0
info:
  title: AWS Key Management Service API List Key Policies
  version: 1.0.0
  description: Retrieves a list of policies attached to a key.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListKeyPolicies:
    get:
      summary: List Key Policies
      description: Retrieves a list of policies attached to a key.
      operationId: listKeyPolicies
      x-api-path-slug: actionlistkeypolicies-get
      parameters:
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key (CMK)
        type: string
      - in: query
        name: Limit
        description: When paginating results, specify the maximum number of items
          to return in the response
        type: string
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only in a
          subsequent request after      you receive a response with truncated results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
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