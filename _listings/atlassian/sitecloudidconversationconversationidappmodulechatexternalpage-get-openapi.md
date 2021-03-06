---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Software Cloud API Get a list of chat:externalPage modules
  description: Authentication required, with scope participate:conversation
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /site/:
    get:
      summary: Get list of sites
      description: Authentication required, with scope participate:conversation
      operationId: GetAllHandler
      x-api-path-slug: site-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Sites
  /site/{cloudId}/conversation:
    get:
      summary: Get a list of conversations
      description: The API returns the list of conversations the app has access to
        Authentication required, with scope participate:conversation
      operationId: ConversationGetAllHandler
      x-api-path-slug: sitecloudidconversation-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: query
        name: cursor
        description: The cursor is a string, that you can use to scroll through the
          data set to get more results
      - in: query
        name: exclude-direct
        description: Exclude direct messages from a response
      - in: query
        name: include-archived
        description: Include archived conversations into response
      - in: query
        name: include-private
        description: Include private conversations into response
      - in: query
        name: limit
        description: A maximum number of conversations to return per call
      - in: query
        name: query
        description: A string containing full or part of conversations name
      - in: query
        name: sort
        description: A sort order of the conversations lists
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Conversations
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:actionTarget:
    get:
      summary: Get a list of chat:actionTarget modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatActionTargetGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatactiontarget-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:actionTarget
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:bot:
    get:
      summary: Get a list of chat:bot modules
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbot-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:bot
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:bot:messages:
    get:
      summary: Get a list of chat:bot:messages modules
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotMessageGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbotmessages-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:bot:messages
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:dialog:
    get:
      summary: Get a list of chat:dialog modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatDialogGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatdialog-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:dialog
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:externalPage:
    get:
      summary: Get a list of chat:externalPage modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatExternalPageGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatexternalpage-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:externalPage
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:glance:
    get:
      summary: Get a list of chat:glance modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatGlanceGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatglance-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:glance
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:sidebar:
    get:
      summary: Get a list of chat:sidebar modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatSidebarGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatsidebar-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:sidebar
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:webhook:
    get:
      summary: Get a list of chat:webhook modules
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatWebhookGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatwebhook-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:webhook
      - Modules
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