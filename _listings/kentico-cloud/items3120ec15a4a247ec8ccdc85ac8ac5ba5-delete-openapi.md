---
swagger: "2.0"
x-collection-name: Kentico Cloud
x-complete: 0
info:
  title: Kentico Cloud Delete a content item by ID
  description: Delete a content item specified by its internal ID. Note that deleting
    a content item deletes all of its language variants as well.
  version: 1.0.0
host: deliver.kenticocloud.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /975bf280-fd91-488c-994c-2f04416e5ee3/items:
    get:
      summary: Order articles by publish date
      description: Filter the content items by content type by including the `order`
        query parameter and a content element codename.
      operationId: 975bf280Fd91488c994c2f04416e5ee3ItemsGet8
      x-api-path-slug: 975bf280fd91488c994c2f04416e5ee3items-get
      parameters:
      - in: header
        name: Content-Type
      - in: query
        name: order
      - in: query
        name: system.type
      responses:
        200:
          description: OK
      tags:
      - Order
      - Articles
      - By
      - Publish
      - Date
  /items/3120ec15-a4a2-47ec-8ccd-c85ac8ac5ba5:
    get:
      summary: View a content item by ID
      description: Retrieve metadata information about a content item specified by
        its internal ID.
      operationId: Items3120ec15A4a247ec8ccdC85ac8ac5ba5Get
      x-api-path-slug: items3120ec15a4a247ec8ccdc85ac8ac5ba5-get
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - View
      - Content
      - Item
      - By
      - ID
    put:
      summary: Update a content item by ID
      description: Update an existing content item specified by its internal ID.
      operationId: Items3120ec15A4a247ec8ccdC85ac8ac5ba5Put
      x-api-path-slug: items3120ec15a4a247ec8ccdc85ac8ac5ba5-put
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Content
      - Item
      - By
      - ID
    delete:
      summary: Delete a content item by ID
      description: Delete a content item specified by its internal ID. Note that deleting
        a content item deletes all of its language variants as well.
      operationId: Items3120ec15A4a247ec8ccdC85ac8ac5ba5Delete2
      x-api-path-slug: items3120ec15a4a247ec8ccdc85ac8ac5ba5-delete
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Content
      - Item
      - By
      - ID
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