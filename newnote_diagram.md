```mermaid
sequenceDiagram
    participant browser
    participant server
    browser->>server : POST https://studies.cs.helsinki.fi/exampleapp/newnote
   activate server

   server->>browser : 302 https://studies.cs.helsinki.fi/exampleapp/notes
   deactivate server

   browser->>server : GET https://studies.cs.helsinki.fi/exampleapp/notes
   activate server

   server->>browser: HTML document
   deactivate server

    browser->>server : GET https://studies.cs.helsinki.fi/exampleapp/main.css
   activate server

   server->>browser : main.css
   deactivate server

    browser->>server : GET https://studies.cs.helsinki.fi/exampleapp/index.js
   activate server

   server->>browser : index.js
   deactivate server

 browser->>server : GET https://studies.cs.helsinki.fi/exampleapp/data.json
   activate server

   server->>browser : data.json
   deactivate server
