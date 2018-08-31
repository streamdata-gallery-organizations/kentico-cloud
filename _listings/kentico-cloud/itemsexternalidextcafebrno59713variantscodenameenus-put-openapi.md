---
swagger: "2.0"
x-collection-name: Kentico Cloud
x-complete: 0
info:
  title: Kentico Cloud Adding localized content
  description: "Add content in a specific language to your new content item by performing
    an upsert.\r\n\r\n* In the request URL, you need to specify the content item you
    are importing to (for example, `/items/external-id/ext-cafe-brno-59713`) and the
    language of the variant (for example, `/variants/codename/en-US`).\r\n* The request
    body must contain the `elements` object in which you specify only the content
    elements you want to update. Omitted elements will remain unchanged.\r\n\r\nSee
    <https://developer.kenticocloud.com/docs/importing-to-kentico-cloud#section-2-adding-localized-content>
    for more details."
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
  /14372844-0a5d-434a-8423-605b8a631623/items:
    get:
      summary: Filtering based on date with Delivery API
      description: |-
        Filter content items directly in the API call using the `element.element_codename` query parameter and *publish from* and *publish until* elements.

        See <https://developer.kenticocloud.com/docs/scheduling-content-unpublishing#section-filtering-by-date-with-the-delivery-api> for more details.
      operationId: 143728440a5d434a8423605b8a631623ItemsGet
      x-api-path-slug: 143728440a5d434a8423605b8a631623items-get
      parameters:
      - in: header
        name: Content-Type
      - in: query
        name: elements.publish_until[gt]
      - in: query
        name: system.type
      responses:
        200:
          description: OK
      tags:
      - Filtering
      - Based
      - "On"
      - Date
      - Delivery
      - API
  /items/codename/on_roasts:
    get:
      summary: View a content item by codename
      description: Retrieve metadata information about a content item specified by
        its codename.
      operationId: ItemsCodenameOnRoastsGet
      x-api-path-slug: itemscodenameon-roasts-get
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
      - Codename
    put:
      summary: Update a content item by codename
      description: Update an existing content item specified by its codename.
      operationId: ItemsCodenameOnRoastsPut
      x-api-path-slug: itemscodenameon-roasts-put
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
      - Codename
    delete:
      summary: Delete a content item by codename
      description: |-
        Delete a content item specified by its codename.

        Note that deleting a content item deletes all of its language variants as well.
      operationId: ItemsCodenameOnRoastsDelete
      x-api-path-slug: itemscodenameon-roasts-delete
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
      - Codename
  /items/3120ec15-a4a2-47ec-8ccd-c85ac8ac5ba5/variants/codename/en-US:
    get:
      summary: View a language variant by language codename
      description: Retrieve content of a variant of a content item. The content item
        is specified by its internal ID and the project language is specified by its
        codename.
      operationId: Items3120ec15A4a247ec8ccdC85ac8ac5ba5VariantsCodenameEnUSGet
      x-api-path-slug: items3120ec15a4a247ec8ccdc85ac8ac5ba5variantscodenameenus-get
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - View
      - Language
      - Variant
      - By
      - Language
      - Codename
    put:
      summary: Upsert a variant by language codename
      description: "Add content to a variant in an active project language, or update
        an existing language variant. The content item is specified by its internal
        ID and the project language is specified by its codename.\r\n\r\n**Note:**
        Only the elements specified in the request body will be modified. Any existing
        comments attached to these elements will be lost on update."
      operationId: Items3120ec15A4a247ec8ccdC85ac8ac5ba5VariantsCodenameEnUSPut
      x-api-path-slug: items3120ec15a4a247ec8ccdc85ac8ac5ba5variantscodenameenus-put
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Upsert
      - Variant
      - By
      - Language
      - Codename
    delete:
      summary: Delete a variant by language codename
      description: "Delete a specific language variant. The content item is specified
        by its external ID and the project language is specified by its codename.\r\n\r\nNote
        that when you delete the last variant of a content item, the whole content
        item is deleted."
      operationId: Items3120ec15A4a247ec8ccdC85ac8ac5ba5VariantsCodenameEnUSDelete3
      x-api-path-slug: items3120ec15a4a247ec8ccdc85ac8ac5ba5variantscodenameenus-delete
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Variant
      - By
      - Language
      - Codename
  /items/external-id/ext-cafe-brno-59713/variants/codename/en-US:
    put:
      summary: Adding localized content
      description: "Add content in a specific language to your new content item by
        performing an upsert.\r\n\r\n* In the request URL, you need to specify the
        content item you are importing to (for example, `/items/external-id/ext-cafe-brno-59713`)
        and the language of the variant (for example, `/variants/codename/en-US`).\r\n*
        The request body must contain the `elements` object in which you specify only
        the content elements you want to update. Omitted elements will remain unchanged.\r\n\r\nSee
        <https://developer.kenticocloud.com/docs/importing-to-kentico-cloud#section-2-adding-localized-content>
        for more details."
      operationId: ItemsExternalIdExtCafeBrno59713VariantsCodenameEnUSPut
      x-api-path-slug: itemsexternalidextcafebrno59713variantscodenameenus-put
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Ing
      - Localized
      - Content
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