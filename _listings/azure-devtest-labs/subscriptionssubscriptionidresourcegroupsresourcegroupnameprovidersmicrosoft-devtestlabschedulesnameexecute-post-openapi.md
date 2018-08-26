---
swagger: "2.0"
x-collection-name: Azure DevTest Labs
x-complete: 0
info:
  title: Azure DevTest Labs API Global Schedules Execute
  description: Execute a schedule. This operation can take a while to complete.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/providers/Microsoft.DevTestLab/schedules:
    get:
      summary: Global Schedules List By Subscription
      description: List schedules in a subscription.
      operationId: GlobalSchedules_ListBySubscription
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-devtestlabschedules-get
      parameters:
      - in: query
        name: $expand
        description: Specify the $expand query
      - in: query
        name: $filter
        description: The filter to apply to the operation
      - in: query
        name: $orderby
        description: The ordering expression for the results, using OData notation
      - in: query
        name: $top
        description: The maximum number of resources to return from the operation
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Global Schedules
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/schedules:
    get:
      summary: Global Schedules List By Resource Group
      description: List schedules in a resource group.
      operationId: GlobalSchedules_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlabschedules-get
      parameters:
      - in: query
        name: $expand
        description: Specify the $expand query
      - in: query
        name: $filter
        description: The filter to apply to the operation
      - in: query
        name: $orderby
        description: The ordering expression for the results, using OData notation
      - in: query
        name: $top
        description: The maximum number of resources to return from the operation
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Global Schedules
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/schedules/{name}:
    get:
      summary: Global Schedules Get
      description: Get schedule.
      operationId: GlobalSchedules_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlabschedulesname-get
      parameters:
      - in: query
        name: $expand
        description: Specify the $expand query
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Global Schedules
    put:
      summary: Global Schedules Create Or Update
      description: Create or replace an existing schedule.
      operationId: GlobalSchedules_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlabschedulesname-put
      parameters:
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      - in: body
        name: schedule
        description: A schedule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Global Schedules
    delete:
      summary: Global Schedules Delete
      description: Delete schedule.
      operationId: GlobalSchedules_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlabschedulesname-delete
      parameters:
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Global Schedules
    patch:
      summary: Global Schedules Update
      description: Modify properties of schedules.
      operationId: GlobalSchedules_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlabschedulesname-patch
      parameters:
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      - in: body
        name: schedule
        description: A schedule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Global Schedules
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/schedules/{name}/execute:
    post:
      summary: Global Schedules Execute
      description: Execute a schedule. This operation can take a while to complete.
      operationId: GlobalSchedules_Execute
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlabschedulesnameexecute-post
      parameters:
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Global Schedules
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