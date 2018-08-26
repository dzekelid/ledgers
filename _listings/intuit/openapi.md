---
swagger: "2.0"
x-collection-name: Intuit
x-complete: 1
info:
  title: QuickBooks Online V3 API
  description: the-quickbooks-online-accounting-api-is-a-restful-api-that-is-used-to-access-quickbooks-companies-docs-
  version: 1.0.0
host: DefaultParameterValue
basePath: /v3/company/DefaultParameterValue
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /reports/GeneralLedger:
    get:
      summary: Get Reports General Ledger
      description: |-
        Report - General Ledger
        Method : GET

        Docs - https://developer.intuit.com/docs/api/accounting/general%20ledger
      operationId: getReportsGeneralledger
      x-api-path-slug: reportsgeneralledger-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: minorversion
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Reports
      - General
      - Ledger
---