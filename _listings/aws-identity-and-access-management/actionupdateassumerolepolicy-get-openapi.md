---
swagger: "2.0"
x-collection-name: AWS Identity and Access Management
x-complete: 0
info:
  title: AWS Identity and Access Management API Update Assume Role Policy
  version: 1.0.0
  description: Updates the policy that grants an IAM entity permission to assume a
    role.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreatePolicy:
    get:
      summary: Create Policy
      description: Creates a new managed policy for your AWS account.
      operationId: createPolicy
      x-api-path-slug: actioncreatepolicy-get
      parameters:
      - in: query
        name: Description
        description: A friendly description of the policy
        type: string
      - in: query
        name: Path
        description: The path for the policy
        type: string
      - in: query
        name: PolicyDocument
        description: The JSON policy document that you want to use as the content
          for the new      policy
        type: string
      - in: query
        name: PolicyName
        description: The friendly name of the policy
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=CreatePolicyVersion:
    get:
      summary: Create Policy Version
      description: Creates a new version of the specified managed policy.
      operationId: createPolicyVersion
      x-api-path-slug: actioncreatepolicyversion-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy to which you
          want to add a new      version
        type: string
      - in: query
        name: PolicyDocument
        description: The JSON policy document that you want to use as the content
          for this new version of      the policy
        type: string
      - in: query
        name: SetAsDefault
        description: Specifies whether to set this version as the policys default
          version
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=DeletePolicy:
    get:
      summary: Delete Policy
      description: Deletes the specified managed policy.
      operationId: deletePolicy
      x-api-path-slug: actiondeletepolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=DeletePolicyVersion:
    get:
      summary: Delete Policy Version
      description: Deletes the specified version from the specified managed policy.
      operationId: deletePolicyVersion
      x-api-path-slug: actiondeletepolicyversion-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy from which you
          want to delete a      version
        type: string
      - in: query
        name: VersionId
        description: The policy version to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=GetPolicy:
    get:
      summary: Get Policy
      description: |-
        Retrieves information about the specified managed policy, including the policy's
              default version and the total number of IAM users, groups, and roles to which the policy is
              attached.
      operationId: getPolicy
      x-api-path-slug: actiongetpolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the managed policy that you
          want information      about
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=GetPolicyVersion:
    get:
      summary: Get Policy Version
      description: |-
        Retrieves information about the specified version of the specified managed policy,
              including the policy document.
      operationId: getPolicyVersion
      x-api-path-slug: actiongetpolicyversion-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the managed policy that you
          want information      about
        type: string
      - in: query
        name: VersionId
        description: Identifies the policy version to retrieve
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=ListAttachedGroupPolicies:
    get:
      summary: List Attached Group Policies
      description: Lists all managed policies that are attached to the specified IAM
        group.
      operationId: listAttachedGroupPolicies
      x-api-path-slug: actionlistattachedgrouppolicies-get
      parameters:
      - in: query
        name: GroupName
        description: The name (friendly name, not ARN) of the group to list attached
          policies for
        type: string
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PathPrefix
        description: The path prefix for filtering the results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Attached Group Policies
  /?Action=ListAttachedRolePolicies:
    get:
      summary: List Attached Role Policies
      description: Lists all managed policies that are attached to the specified IAM
        role.
      operationId: listAttachedRolePolicies
      x-api-path-slug: actionlistattachedrolepolicies-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PathPrefix
        description: The path prefix for filtering the results
        type: string
      - in: query
        name: RoleName
        description: The name (friendly name, not ARN) of the role to list attached
          policies for
        type: string
      responses:
        200:
          description: OK
      tags:
      - Attached Role Policies
  /?Action=ListAttachedUserPolicies:
    get:
      summary: List Attached User Policies
      description: Lists all managed policies that are attached to the specified IAM
        user.
      operationId: listAttachedUserPolicies
      x-api-path-slug: actionlistattacheduserpolicies-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PathPrefix
        description: The path prefix for filtering the results
        type: string
      - in: query
        name: UserName
        description: The name (friendly name, not ARN) of the user to list attached
          policies for
        type: string
      responses:
        200:
          description: OK
      tags:
      - Attached Use rPolicies
  /?Action=ListGroupPolicies:
    get:
      summary: List Group Policies
      description: |-
        Lists the names of the inline policies that are embedded in the specified IAM
              group.
      operationId: listGroupPolicies
      x-api-path-slug: actionlistgrouppolicies-get
      parameters:
      - in: query
        name: GroupName
        description: The name of the group to list policies for
        type: string
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Group Policies
  /?Action=ListPolicies:
    get:
      summary: List Policies
      description: |-
        Lists all the managed policies that are available in your AWS account, including your
              own customer-defined managed policies and all AWS managed policies.
      operationId: listPolicies
      x-api-path-slug: actionlistpolicies-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: OnlyAttached
        description: A flag to filter the results to only the attached policies
        type: string
      - in: query
        name: PathPrefix
        description: The path prefix for filtering the results
        type: string
      - in: query
        name: Scope
        description: The scope to use for filtering the results
        type: string
      responses:
        200:
          description: OK
      tags:
      - listPolicies
  /?Action=ListRolePolicies:
    get:
      summary: List Role Policies
      description: |-
        Lists the names of the inline policies that are embedded in the specified IAM
              role.
      operationId: listRolePolicies
      x-api-path-slug: actionlistrolepolicies-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: RoleName
        description: The name of the role to list policies for
        type: string
      responses:
        200:
          description: OK
      tags:
      - Role Policies
  /?Action=ListUserPolicies:
    get:
      summary: List User Policies
      description: Lists the names of the inline policies embedded in the specified
        IAM user.
      operationId: listUserPolicies
      x-api-path-slug: actionlistuserpolicies-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: UserName
        description: The name of the user to list policies for
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=AttachGroupPolicy:
    get:
      summary: Attach Group Policy
      description: Attaches the specified managed policy to the specified IAM group.
      operationId: attachGroupPolicy
      x-api-path-slug: actionattachgrouppolicy-get
      parameters:
      - in: query
        name: GroupName
        description: The name (friendly name, not ARN) of the group to attach the
          policy to
        type: string
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          attach
        type: string
      responses:
        200:
          description: OK
      tags:
      - Group Policies
  /?Action=AttachRolePolicy:
    get:
      summary: Attach Role Policy
      description: Attaches the specified managed policy to the specified IAM role.
      operationId: attachRolePolicy
      x-api-path-slug: actionattachrolepolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          attach
        type: string
      - in: query
        name: RoleName
        description: The name (friendly name, not ARN) of the role to attach the policy
          to
        type: string
      responses:
        200:
          description: OK
      tags:
      - Role Policies
  /?Action=AttachUserPolicy:
    get:
      summary: Attach User Policy
      description: Attaches the specified managed policy to the specified user.
      operationId: attachUserPolicy
      x-api-path-slug: actionattachuserpolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          attach
        type: string
      - in: query
        name: UserName
        description: The name (friendly name, not ARN) of the IAM user to attach the
          policy to
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=DeleteAccountPasswordPolicy:
    get:
      summary: Delete Account Password Policy
      description: Deletes the password policy for the AWS account.
      operationId: deleteAccountPasswordPolicy
      x-api-path-slug: actiondeleteaccountpasswordpolicy-get
      parameters:
      - in: query
        name: LimitExceeded
        description: The request was rejected because it attempted to create resources
          beyond the current      AWS account limits
        type: string
      - in: query
        name: NoSuchEntity
        description: The request was rejected because it referenced an entity that
          does not exist
        type: string
      - in: query
        name: ServiceFailure
        description: The request processing has failed because of an unknown error,
          exception or      failure
        type: string
      responses:
        200:
          description: OK
      tags:
      - Account Password Policies
  /?Action=DeleteGroupPolicy:
    get:
      summary: Delete Group Policy
      description: |-
        Deletes the specified inline policy that is embedded in the specified IAM
              group.
      operationId: deleteGroupPolicy
      x-api-path-slug: actiondeletegrouppolicy-get
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
      - Group Policies
  /?Action=DeleteRolePolicy:
    get:
      summary: Delete Role Policy
      description: |-
        Deletes the specified inline policy that is embedded in the specified IAM
              role.
      operationId: deleteRolePolicy
      x-api-path-slug: actiondeleterolepolicy-get
      parameters:
      - in: query
        name: PolicyName
        description: The name of the inline policy to delete from the specified IAM
          role
        type: string
      - in: query
        name: RoleName
        description: The name (friendly name, not ARN) identifying the role that the
          policy is embedded      in
        type: string
      responses:
        200:
          description: OK
      tags:
      - Role Policies
  /?Action=DeleteUserPolicy:
    get:
      summary: Delete User Policy
      description: |-
        Deletes the specified inline policy that is embedded in the specified IAM
              user.
      operationId: deleteUserPolicy
      x-api-path-slug: actiondeleteuserpolicy-get
      parameters:
      - in: query
        name: PolicyName
        description: The name identifying the policy document to delete
        type: string
      - in: query
        name: UserName
        description: The name (friendly name, not ARN) identifying the user that the
          policy is embedded      in
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=DetachGroupPolicy:
    get:
      summary: Detach Group Policy
      description: Removes the specified managed policy from the specified IAM group.
      operationId: detachGroupPolicy
      x-api-path-slug: actiondetachgrouppolicy-get
      parameters:
      - in: query
        name: GroupName
        description: The name (friendly name, not ARN) of the IAM group to detach
          the policy      from
        type: string
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          detach
        type: string
      responses:
        200:
          description: OK
      tags:
      - Group Policies
  /?Action=DetachRolePolicy:
    get:
      summary: Detach Role Policy
      description: Removes the specified managed policy from the specified role.
      operationId: detachRolePolicy
      x-api-path-slug: actiondetachrolepolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          detach
        type: string
      - in: query
        name: RoleName
        description: The name (friendly name, not ARN) of the IAM role to detach the
          policy      from
        type: string
      responses:
        200:
          description: OK
      tags:
      - Role Policies
  /?Action=DetachUserPolicy:
    get:
      summary: Detach User Policy
      description: Removes the specified managed policy from the specified user.
      operationId: detachUserPolicy
      x-api-path-slug: actiondetachuserpolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          detach
        type: string
      - in: query
        name: UserName
        description: The name (friendly name, not ARN) of the IAM user to detach the
          policy      from
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=GetAccountPasswordPolicy:
    get:
      summary: Get Account Password Policy
      description: Retrieves the password policy for the AWS account.
      operationId: getAccountPasswordPolicy
      x-api-path-slug: actiongetaccountpasswordpolicy-get
      parameters:
      - in: query
        name: PasswordPolicy
        description: Contains information about the account password policy
        type: string
      responses:
        200:
          description: OK
      tags:
      - Accounts
  /?Action=GetContextKeysForCustomPolicy:
    get:
      summary: Get Context Keys For Custom Policy
      description: Gets a list of all of the context keys referenced in the input
        policies.
      operationId: getContextKeysForCustomPolicy
      x-api-path-slug: actiongetcontextkeysforcustompolicy-get
      parameters:
      - in: query
        name: PolicyInputList.member.N
        description: A list of policies for which you want the list of context keys
          referenced in those      policies
        type: string
      responses:
        200:
          description: OK
      tags:
      - Context Keys For Custom Policies
  /?Action=GetContextKeysForPrincipalPolicy:
    get:
      summary: Get Context Keys For Principal Policy
      description: |-
        Gets a list of all of the context keys referenced in all of the IAM policies attached
              to the specified IAM entity.
      operationId: getContextKeysForPrincipalPolicy
      x-api-path-slug: actiongetcontextkeysforprincipalpolicy-get
      parameters:
      - in: query
        name: PolicyInputList.member.N
        description: An optional list of additional policies for which you want the
          list of context keys      that are referenced
        type: string
      - in: query
        name: PolicySourceArn
        description: The ARN of a user, group, or role whose policies contain the
          context keys that you want      listed
        type: string
      responses:
        200:
          description: OK
      tags:
      - Context Keys For Principal Policies
  /?Action=GetGroupPolicy:
    get:
      summary: Get Group Policy
      description: |-
        Retrieves the specified inline policy document that is embedded in the specified IAM
              group.
      operationId: getGroupPolicy
      x-api-path-slug: actiongetgrouppolicy-get
      parameters:
      - in: query
        name: GroupName
        description: The name of the group the policy is associated with
        type: string
      - in: query
        name: PolicyName
        description: The name of the policy document to get
        type: string
      responses:
        200:
          description: OK
      tags:
      - Group Policies
  /?Action=GetRolePolicy:
    get:
      summary: Get Role Policy
      description: |-
        Retrieves the specified inline policy document that is embedded with the specified
              IAM role.
      operationId: getRolePolicy
      x-api-path-slug: actiongetrolepolicy-get
      parameters:
      - in: query
        name: PolicyName
        description: The name of the policy document to get
        type: string
      - in: query
        name: RoleName
        description: The name of the role associated with the policy
        type: string
      responses:
        200:
          description: OK
      tags:
      - Role Policies
  /?Action=GetUserPolicy:
    get:
      summary: Get User Policy
      description: |-
        Retrieves the specified inline policy document that is embedded in the specified IAM
              user.
      operationId: getUserPolicy
      x-api-path-slug: actiongetuserpolicy-get
      parameters:
      - in: query
        name: PolicyName
        description: The name of the policy document to get
        type: string
      - in: query
        name: UserName
        description: The name of the user who the policy is associated with
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=ListEntitiesForPolicy:
    get:
      summary: List Entities For Policy
      description: |-
        Lists all IAM users, groups, and roles that the specified managed policy is attached
              to.
      operationId: listEntitiesForPolicy
      x-api-path-slug: actionlistentitiesforpolicy-get
      parameters:
      - in: query
        name: EntityFilter
        description: The entity type to use for filtering the results
        type: string
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PathPrefix
        description: The path prefix for filtering the results
        type: string
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy for which you
          want the      versions
        type: string
      responses:
        200:
          description: OK
      tags:
      - Entities For Policies
  /?Action=ListPolicyVersions:
    get:
      summary: List Policy Versions
      description: |-
        Lists information about the versions of the specified managed policy, including the
              version that is currently set as the policy's default version.
      operationId: listPolicyVersions
      x-api-path-slug: actionlistpolicyversions-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy for which you
          want the      versions
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policy Versions
  /?Action=PutGroupPolicy:
    get:
      summary: Put Group Policy
      description: |-
        Adds or updates an inline policy document that is embedded in the specified IAM
              group.
      operationId: putGroupPolicy
      x-api-path-slug: actionputgrouppolicy-get
      parameters:
      - in: query
        name: GroupName
        description: The name of the group to associate the policy with
        type: string
      - in: query
        name: PolicyDocument
        description: The policy document
        type: string
      - in: query
        name: PolicyName
        description: The name of the policy document
        type: string
      responses:
        200:
          description: OK
      tags:
      - Group Policies
  /?Action=PutRolePolicy:
    get:
      summary: Put Role Policy
      description: |-
        Adds or updates an inline policy document that is embedded in the specified IAM
              role.
      operationId: putRolePolicy
      x-api-path-slug: actionputrolepolicy-get
      parameters:
      - in: query
        name: PolicyDocument
        description: The policy document
        type: string
      - in: query
        name: PolicyName
        description: The name of the policy document
        type: string
      - in: query
        name: RoleName
        description: The name of the role to associate the policy with
        type: string
      responses:
        200:
          description: OK
      tags:
      - Role Policies
  /?Action=PutUserPolicy:
    get:
      summary: Put User Policy
      description: |-
        Adds or updates an inline policy document that is embedded in the specified IAM
              user.
      operationId: putUserPolicy
      x-api-path-slug: actionputuserpolicy-get
      parameters:
      - in: query
        name: PolicyDocument
        description: The policy document
        type: string
      - in: query
        name: PolicyName
        description: The name of the policy document
        type: string
      - in: query
        name: UserName
        description: The name of the user to associate the policy with
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users Policies
  /?Action=SetDefaultPolicyVersion:
    get:
      summary: Set Default Policy Version
      description: |-
        Sets the specified version of the specified policy as the policy's default (operative)
              version.
      operationId: setDefaultPolicyVersion
      x-api-path-slug: actionsetdefaultpolicyversion-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy whose default
          version you want to      set
        type: string
      - in: query
        name: VersionId
        description: The version of the policy to set as the default (operative) version
        type: string
      responses:
        200:
          description: OK
      tags:
      - Default Policy Versions
  /?Action=SimulateCustomPolicy:
    get:
      summary: Simulate Custom Policy
      description: |-
        Simulate how a set of IAM policies and optionally a resource-based policy works with
              a list of API actions and AWS resources to determine the policies' effective permissions.
      operationId: simulateCustomPolicy
      x-api-path-slug: actionsimulatecustompolicy-get
      parameters:
      - in: query
        name: ActionNames.member.N
        description: A list of names of API actions to evaluate in the simulation
        type: string
      - in: query
        name: CallerArn
        description: The ARN of the IAM user that you want to use as the simulated
          caller of the APIs
        type: string
      - in: query
        name: ContextEntries.member.N
        description: A list of context keys and corresponding values for the simulation
          to use
        type: string
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PolicyInputList.member.N
        description: A list of policy documents to include in the simulation
        type: string
      - in: query
        name: ResourceArns.member.N
        description: A list of ARNs of AWS resources to include in the simulation
        type: string
      - in: query
        name: ResourceHandlingOption
        description: Specifies the type of simulation to run
        type: string
      - in: query
        name: ResourceOwner
        description: An AWS account ID that specifies the owner of any simulated resource
          that does not      identify its owner in the resource ARN, such as an S3
          bucket or object
        type: string
      - in: query
        name: ResourcePolicy
        description: A resource-based policy to include in the simulation provided
          as a string
        type: string
      responses:
        200:
          description: OK
      tags:
      - Custom Policies
  /?Action=SimulatePrincipalPolicy:
    get:
      summary: Simulate Principal Policy
      description: |-
        Simulate how a set of IAM policies attached to an IAM entity works with a list of
              API actions and AWS resources to determine the policies' effective permissions.
      operationId: simulatePrincipalPolicy
      x-api-path-slug: actionsimulateprincipalpolicy-get
      parameters:
      - in: query
        name: ActionNames.member.N
        description: A list of names of API actions to evaluate in the simulation
        type: string
      - in: query
        name: CallerArn
        description: The ARN of the IAM user that you want to specify as the simulated
          caller of the APIs
        type: string
      - in: query
        name: ContextEntries.member.N
        description: A list of context keys and corresponding values for the simulation
          to use
        type: string
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PolicyInputList.member.N
        description: An optional list of additional policy documents to include in
          the simulation
        type: string
      - in: query
        name: PolicySourceArn
        description: The Amazon Resource Name (ARN) of a user, group, or role whose
          policies you want to      include in the simulation
        type: string
      - in: query
        name: ResourceArns.member.N
        description: A list of ARNs of AWS resources to include in the simulation
        type: string
      - in: query
        name: ResourceHandlingOption
        description: Specifies the type of simulation to run
        type: string
      - in: query
        name: ResourceOwner
        description: An AWS account ID that specifies the owner of any simulated resource
          that does not      identify its owner in the resource ARN, such as an S3
          bucket or object
        type: string
      - in: query
        name: ResourcePolicy
        description: A resource-based policy to include in the simulation provided
          as a string
        type: string
      responses:
        200:
          description: OK
      tags:
      - Principal Policies
  /?Action=UpdateAccountPasswordPolicy:
    get:
      summary: Update Account Password Policy
      description: Updates the password policy settings for the AWS account.
      operationId: updateAccountPasswordPolicy
      x-api-path-slug: actionupdateaccountpasswordpolicy-get
      parameters:
      - in: query
        name: AllowUsersToChangePassword
        description: Allows all IAM users in your account to use the AWS Management
          Console to change their own      passwords
        type: string
      - in: query
        name: HardExpiry
        description: Prevents IAM users from setting a new password after their password
          has      expired
        type: string
      - in: query
        name: MaxPasswordAge
        description: The number of days that an IAM user password is valid
        type: string
      - in: query
        name: MinimumPasswordLength
        description: The minimum number of characters allowed in an IAM user password
        type: string
      - in: query
        name: PasswordReusePrevention
        description: Specifies the number of previous passwords that IAM users are
          prevented from reusing
        type: string
      - in: query
        name: RequireLowercaseCharacters
        description: Specifies whether IAM user passwords must contain at least one
          lowercase character      from the ISO basic Latin alphabet (a to z)
        type: string
      - in: query
        name: RequireNumbers
        description: Specifies whether IAM user passwords must contain at least one
          numeric character (0      to 9)
        type: string
      - in: query
        name: RequireSymbols
        description: 'Specifies whether IAM user passwords must contain at least one
          of the following      non-alphanumeric characters:'
        type: string
      - in: query
        name: RequireUppercaseCharacters
        description: Specifies whether IAM user passwords must contain at least one
          uppercase character      from the ISO basic Latin alphabet (A to Z)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Account Password Policy
  /?Action=UpdateAssumeRolePolicy:
    get:
      summary: Update Assume Role Policy
      description: Updates the policy that grants an IAM entity permission to assume
        a role.
      operationId: updateAssumeRolePolicy
      x-api-path-slug: actionupdateassumerolepolicy-get
      parameters:
      - in: query
        name: PolicyDocument
        description: The policy that grants an entity permission to assume the role
        type: string
      - in: query
        name: RoleName
        description: The name of the role to update with the new policy
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assume Role Policy
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