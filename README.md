# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js servers where long-running requests can cause the server to become unresponsive.  The provided code simulates a long-running task within the request handler, blocking the event loop and preventing other requests from being processed.  A solution is also provided to address this problem using asynchronous operations.

## Bug

The `server.js` file contains a simple HTTP server that simulates a long-running task (5-second delay).  During this delay, the server becomes unresponsive to new requests.  This behavior is characteristic of a blocking operation within the event loop, a common problem in Node.js when not handling asynchronous tasks correctly.

## Solution

The `server-solution.js` file showcases how to resolve this by using asynchronous operations.  This allows the event loop to remain responsive and process other requests, even while the long-running task is executing.