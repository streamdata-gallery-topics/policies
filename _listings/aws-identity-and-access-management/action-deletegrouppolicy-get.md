---
swagger: "2.0"
info:
  title: AWS Identity and Access Management API Delete Group Policy
  version: 1.0.0
  description: |-
    Deletes the specified inline policy that is embedded in the specified IAM
          group.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteGroupPolicy:
    get:
      summary: ' Delete Group Policy '
      description: |-
        Deletes the specified inline policy that is embedded in the specified IAM
              group
      operationId: deleteGroupPolicy
      parameters:
      - in: query
        name: GroupName
        description: The name (friendly name, not ARN) identifying the group that
          the policy is embedded      in
        type: string
      - in: query
        name: PolicyName
        description: The name identifying the policy document to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - group policies
definitions: []
x-collection-name: AWS Identity and Access Management
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