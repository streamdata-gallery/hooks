---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 1
info:
  title: Eventbrite
  description: create-manage--promote-events--add-eventmanagement-features-to-your-site--show-the-world-what-exciting-things-are-happening-around-them-
  version: 1.0.0
host: www.eventbrite.com
basePath: /%7Bdata-type%7D/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /webhooks/{id}/:
    get:
      summary: Get Webhooks
      description: Returns a webhook for the specified webhook as webhook.
      operationId: getWebhooks
      x-api-path-slug: webhooksid-get
      responses:
        200:
          description: OK
      tags:
      - Webhooks
    delete:
      summary: Delete Webhooks
      description: Deletes the specified webhook object.
      operationId: deleteWebhooks
      x-api-path-slug: webhooksid-delete
      responses:
        200:
          description: OK
      tags:
      - Webhooks
  /webhooks/:
    get:
      summary: Get Webhooks
      description: Returns the list of webhook objects that belong to the authenticated
        user.
      operationId: getWebhooks
      x-api-path-slug: webhooks-get
      responses:
        200:
          description: OK
      tags:
      - Webhooks
    post:
      summary: Post Webhooks
      description: Creates a webhook for the authenticated user.
      operationId: postWebhooks
      x-api-path-slug: webhooks-post
      parameters:
      - in: query
        name: actions
        description: Determines what actions will trigger the webhook
        type: query
      - in: query
        name: endpoint_url
        description: The target URL of the Webhook subscription
        type: query
      - in: query
        name: event_id
        description: The ID of the event that triggers this webhook
        type: query
      responses:
        200:
          description: OK
      tags:
      - Webhooks
---