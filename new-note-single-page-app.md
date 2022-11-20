# diagram-http-NEW-NOTE
## What will happen if we will add new note with submit button from the form
```mermaid
sequenceDiagram
    participant BROWSER
    participant SERVER
    BROWSER->>SERVER: The POST request to the address https://studies.cs.helsinki.fi/exampleapp/new_note_spa as JSON-data defined to the Content-Type header
    SERVER->>BROWSER: The server responds {"message":"note created"} with status code 201 created. This time the server does not ask for a redirect, the browser stays on the same page, and it sends no further HTTP requests
