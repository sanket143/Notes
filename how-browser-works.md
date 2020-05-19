# How Browser Works

### **The browser's main functionality**

- To present web resource
  - request from the server
  - displaying it in browser window
  - resource is mostly HTML

### **The browser's high livel structure**

Main components
- The user interface
  - address bar, button, menu, etc
  - everything except the the window where we see requested page
- The browser engine
  - marshals actions between the UI and the rendering engine
- The rendering engine
  - displays requested content
  - parses HTML and CSS and displays on the screen
- Networking
  - network calls such as HTTP requests
- UI backend
  - drawing basic widgets like combo boxes and windows
  - generic interface
- JavaScript interpreter
  - parse and execute JavaScript code
- Data Storage
  - a persistence layer
  - browser stores all sorts of data locally, such as cookies.
  - also support storage mechanisms such as localStorage, IndexedDB
  WebSQL and FileSystem

Chrome run multiple instances of _rendering engine:_ one for each tab.
Each tab runs in a separate process.

### **The rendering engine**

By default, the rendering engine can display HTML and XML documents
and images. It can display other types of data via plug-ins or extensions;
for example, displaying PDF documents using PDF viewer plug-in.

**Rendering engines**

Internet Explorer: Trident
Firefox: Gecko
Safari: WebKit
Chrome and Opera : Blink; a fork of WebKit

**The main flow**

Rendering engine receives contents from the requested document.
then following happens
- parsing HTML to construct the DOM tree
- Render tree construction
- Layout of the render tree
- Painting the render tree

References
- https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/

