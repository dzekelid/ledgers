---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Contra funds between ledgers
  version: 1.0.0
  description: Contra funds between ledgers.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/transfer/contra:
    post:
      summary: Contra funds between ledgers
      description: Contra funds between ledgers.
      operationId: Transfer_ProcessContraPaymentBycontraDataContract
      x-api-path-slug: apitransfercontra-post
      parameters:
      - in: body
        name: contraDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Contra
      - Funds
      - Between
      - Ledgers
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