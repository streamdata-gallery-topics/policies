---
swagger: "2.0"
x-collection-name: AWS Auto Scaling
x-complete: 0
info:
  title: AWS Auto Scaling API Delete Policy
  version: 1.0.0
  description: Deletes the specified Auto Scaling policy.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeletePolicy:
    get:
      summary: Delete Policy
      description: Deletes the specified Auto Scaling policy.
      operationId: deletePolicy
      x-api-path-slug: actiondeletepolicy-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the Auto Scaling group
        type: string
      - in: query
        name: PolicyName
        description: The name or Amazon Resource Name (ARN) of the policy
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=DescribePolicies:
    get:
      summary: Describe Policies
      description: Describes the policies for the specified Auto Scaling group.
      operationId: describePolicies
      x-api-path-slug: actiondescribepolicies-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of items to be returned with each call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      - in: query
        name: PolicyNames.member.N
        description: One or more policy names or policy ARNs to be described
        type: string
      - in: query
        name: PolicyTypes.member.N
        description: One or more policy types
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=ExecutePolicy:
    get:
      summary: Execute Policy
      description: Executes the specified policy.
      operationId: executePolicy
      x-api-path-slug: actionexecutepolicy-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name or Amazon Resource Name (ARN) of the Auto Scaling group
        type: string
      - in: query
        name: BreachThreshold
        description: The breach threshold for the alarm
        type: string
      - in: query
        name: HonorCooldown
        description: If this parameter is true, Auto Scaling waits for the cooldown
          period to complete before executing the policy
        type: string
      - in: query
        name: MetricValue
        description: The metric value to compare to BreachThreshold
        type: string
      - in: query
        name: PolicyName
        description: The name or ARN of the policy
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