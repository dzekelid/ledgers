---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Get uncleared items for account/ledger
  version: 1.0.0
  description: Get uncleared items for account/ledger.
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
  /api/account/{id}/ledger:
    post:
      summary: Retrieve ledger posting details for an account
      description: Retrieve ledger posting details for an account.
      operationId: Account_GetLedgerByidBydataContract
      x-api-path-slug: apiaccountidledger-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Ledger
      - Posting
      - Detailsan
      - Account
  /api/account/ledger:
    post:
      summary: Retrive ledger postings without account id
      description: Retrive ledger postings without account id.
      operationId: Account_GetAllLedgerBydataContract
      x-api-path-slug: apiaccountledger-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Retrive
      - Ledger
      - Postings
      - Without
      - Account
      - Id
  /api/accounting/exports/ledgerentriescsv:
    post:
      summary: Get ledger items formatted for export csv
      description: Get ledger items formatted for export csv.
      operationId: AccountingExport_ExportLedgerEntriesCsvBydataContract
      x-api-path-slug: apiaccountingexportsledgerentriescsv-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Ledger
      - Items
      - Formattedexport
      - Csv
  /api/posting/transaction/{ledgerEntryId}:
    get:
      summary: Get ledger entry details by Id
      description: Get ledger entry details by id.
      operationId: Posting_GetTransactionByledgerEntryIdByaccountId
      x-api-path-slug: apipostingtransactionledgerentryid-get
      parameters:
      - in: query
        name: accountId
        description: Account Id to filter ledger lines
      - in: path
        name: ledgerEntryId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Ledger
      - Entry
      - Details
      - By
      - Id
  /api/posting/suspense:
    get:
      summary: Get all ledger postings in the suspense account
      description: Get all ledger postings in the suspense account.
      operationId: Posting_GetSuspensePostingsBypageSizeBypageNumber
      x-api-path-slug: apipostingsuspense-get
      parameters:
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Ledger
      - Postings
      - In
      - Suspense
      - Account
  /api/posting/addadjustmentitem:
    post:
      summary: Add adjustment to ledger entry
      description: Add adjustment to ledger entry.
      operationId: Posting_AddAdjustmentItemByadjustmentItemDataContract
      x-api-path-slug: apipostingaddadjustmentitem-post
      parameters:
      - in: body
        name: adjustmentItemDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Adjustment
      - To
      - Ledger
      - Entry
  /api/posting/{accountId}/uncleared:
    post:
      summary: Get uncleared items for account/ledger
      description: Get uncleared items for account/ledger.
      operationId: Posting_GetAccountUnclearedItemsByaccountIdByunclearedItemsDataContract
      x-api-path-slug: apipostingaccountiduncleared-post
      parameters:
      - in: path
        name: accountId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: unclearedItemsDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Uncleared
      - Itemsaccount
      - Ledger
  /api/transfer/suspend:
    post:
      summary: Move funds to suspense account to another ledger
      description: Move funds to suspense account to another ledger.
      operationId: Transfer_ProcessSuspendFundsBysuspendDataContract
      x-api-path-slug: apitransfersuspend-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: suspendDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Move
      - Funds
      - To
      - Suspense
      - Account
      - To
      - Another
      - Ledger
  /api/transfer/unsuspend:
    post:
      summary: Move funds from suspense account to another ledger
      description: Move funds from suspense account to another ledger.
      operationId: Transfer_ProcessUnsuspendFundsBysuspendDataContract
      x-api-path-slug: apitransferunsuspend-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: suspendDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Move
      - Funds
      - From
      - Suspense
      - Account
      - To
      - Another
      - Ledger
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