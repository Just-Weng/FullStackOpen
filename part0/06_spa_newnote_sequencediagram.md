```mermaid
    sequenceDiagram
        participant browser
        participant server

        Note right of browser: browser rerenders changes, sends new note to server
        browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
        activate server
        Note left of server: server does not ask for a redirect and browser stays on the same page
        server->>browser: HTTP status code 201
        deactivate server
        
```