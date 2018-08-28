---
swagger: "2.0"
x-collection-name: Azure Blockchain Workbench
x-complete: 0
info:
  title: Azure Blockchain Workbench Get Ledgers Connections Transactions
  description: Lists the transactions for a connected blockchain network.
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/ledgers/connections:
    get:
      summary: Get Ledgers Connections
      description: Lists the connected blockchain networks.
      operationId: ConnectionsGet
      x-api-path-slug: apiv1ledgersconnections-get
      parameters:
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: top
        description: The maximum number of items to return
      responses:
        200:
          description: OK
      tags:
      - Ledgers
      - Connections
  /api/v1/ledgers/connections/{connectionId}:
    get:
      summary: Get Ledgers Connections
      description: Gets the connected blockchain network matching a specific connection
        ID.
      operationId: ConnectionGet
      x-api-path-slug: apiv1ledgersconnectionsconnectionid-get
      parameters:
      - in: path
        name: connectionId
        description: The id of the connection
      responses:
        200:
          description: OK
      tags:
      - Ledgers
      - Connections
  /api/v1/ledgers/connections/{connectionId}/blocks:
    get:
      summary: Get Ledgers Connections Blocks
      description: Lists the blocks for a connected blockchain network.
      operationId: BlocksGet
      x-api-path-slug: apiv1ledgersconnectionsconnectionidblocks-get
      parameters:
      - in: path
        name: connectionId
        description: The id of the connection
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: top
        description: The maximum number of items to return
      responses:
        200:
          description: OK
      tags:
      - Ledgers
      - Connections
      - Blocks
  /api/v1/ledgers/connections/{connectionId}/blocks/{blockId}:
    get:
      summary: Get Ledgers Connections Blocks Blockid
      description: Gets the block matching a specific block ID.
      operationId: BlockGet
      x-api-path-slug: apiv1ledgersconnectionsconnectionidblocksblockid-get
      parameters:
      - in: path
        name: blockId
        description: The id of the block
      - in: path
        name: connectionId
        description: The connectionId of the block
      responses:
        200:
          description: OK
      tags:
      - Ledgers
      - Connections
      - Blocks
      - Blockid
  /api/v1/ledgers/connections/{connectionId}/transactions:
    get:
      summary: Get Ledgers Connections Transactions
      description: Lists the transactions for a connected blockchain network.
      operationId: TransactionsGet
      x-api-path-slug: apiv1ledgersconnectionsconnectionidtransactions-get
      parameters:
      - in: path
        name: connectionId
        description: The id of the connection
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: top
        description: The maximum number of items to return
      responses:
        200:
          description: OK
      tags:
      - Ledgers
      - Connections
      - Transactions
  /api/v1/ledgers/connections/{connectionId}/transactions/{transactionId}:
    get:
      summary: Get Ledgers Connections Transactions Transactionid
      description: Gets the transaction matching a specific transaction ID.
      operationId: TransactionGet
      x-api-path-slug: apiv1ledgersconnectionsconnectionidtransactionstransactionid-get
      parameters:
      - in: path
        name: connectionId
        description: The connectionId of the transaction
      - in: path
        name: transactionId
        description: The id of the transaction
      responses:
        200:
          description: OK
      tags:
      - Ledgers
      - Connections
      - Transactions
      - Transactionid
  /api/v1/ledgers:
    get:
      summary: Get Ledgers
      description: Lists the supported blockchain types, such as Ethereum or Hyperledger
        Fabric.
      operationId: LedgersGet
      x-api-path-slug: apiv1ledgers-get
      parameters:
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: top
        description: The maximum number of items to return
      responses:
        200:
          description: OK
      tags:
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