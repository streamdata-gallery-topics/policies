---
swagger: "2.0"
info:
  title: AWS Route 53 API Get Traffic Policy Instance
  version: 1.0.0
  description: Gets information about a specified traffic policy instance.Send a GET
    request to the /Amazon Route 53 APIversion/trafficpolicyinstance resource.NoteAfter
    you submit a CreateTrafficPolicyInstance or anUpdateTrafficPolicyInstance request,
    there's a brief delay while Amazon Route 53creates the resource record sets that
    are specified in the traffic policy definition. Formore information, see the State
    response element.NoteIn the Amazon Route 53 console, traffic policy instances
    are known as policy records.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/trafficpolicyinstance/Id:
    get:
      summary: Get Traffic Policy Instance
      description: Gets information about a specified traffic policy instance
      operationId: gettrafficpolicyinstance
      parameters:
      - in: path
        name: Id
        description: The ID of the traffic policy instance that you want to get information
          about
        type: string
      responses:
        200:
          description: OK
      tags:
      - traffic policies
definitions: []
x-collection-name: AWS Route 53
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