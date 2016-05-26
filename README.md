# dbuggr-node-inspector
Testing node-inspector regarding its suitability for dbuggr

## setting up basic node inspector example
- `clone` this repo
- navigate to that local repo in console
- install the node-inspector npm package with `npm install node-inspector --save`
- start node-inspector using `node-inspector`
  - this starts a server, we can connect to using the printed url
  - however, no process to debug is started yet
- so, to start a process using `node --debug examples/index.js` (which is a simple server) in a second console
  - now, we can navigate our browser to `http://localhost:3000/` to see a page delivered by the server application
- refreshing the debug window gives us a view on local source code files
  - we can also set a breakpoint in the server's request handler, and refresh the delivered page
  - the page won't return as we hit the breakpoint in our code
    - from here on we can inspect the local variables like the request, and even modify it on the fly
- we can also pause at the beginning of an execution using `node --debug-brk examples/index.js`
