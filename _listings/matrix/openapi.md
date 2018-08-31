swagger: "2.0"
x-collection-name: Matrix
x-complete: 1
info:
  title: Matrix
  version: 1.0.0
host: /register
basePath: http://localhost:8008/_matrix/client/api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /login:
    get:
      summary: Get the login mechanism to use when logging in.
      description: All login stages MUST be mentioned if there is >1 login type.
      operationId: get_login_info
      x-api-path-slug: login-get
      responses:
        200:
          description: OK
      tags:
      - Login
      - Mechanism
      - To
      - Use
      - When
      - Logging
      - In
    post:
      summary: Submit a login action.
      description: If this is part of a multi-stage login, there MUST be a session
        key.
      operationId: submit_login
      x-api-path-slug: login-post
      parameters:
      - in: body
        name: body
        description: A login submission
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Submit
      - Login
      - Action