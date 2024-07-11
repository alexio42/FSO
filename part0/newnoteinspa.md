```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>browser: JavaScript code handles submitted form data
    browser->>browser: JavaScript code rerenders the note list

    browser->>server: POST https://fullstack-exampleapp.herokuapp.com/new_note_spa
    activate server
    server-->>browser: status code 201
    deactivate server

    Note left of server: Server does not request a redirect this time
```