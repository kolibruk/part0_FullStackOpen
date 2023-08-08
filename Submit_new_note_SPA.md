```mermaid
sequenceDiagram
    actor user
    participant browser
    participant server

    user->>browser: Clicks "Save" button
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created {"message":"note created"}
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes