```mermaid
sequenceDiagram
    participant browser
    participant server
    
    browser->>server: POST studies.cs.helsinki.fi/exampleapp/new_note_spa 
    Note right of browser: POST request contains the new note as JSON data
    activate server
    server-->>browser: status code 201
    deactivate server
    Note right of browser: The browser adds the note to the local notes array and re-renders the list

```