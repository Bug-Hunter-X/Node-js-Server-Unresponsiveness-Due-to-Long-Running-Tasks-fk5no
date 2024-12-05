# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js servers: unresponsiveness due to long-running tasks blocking the event loop. The `bug.js` file shows a server that performs a long computation, making it unresponsive to new requests.  The `bugSolution.js` file provides a solution using asynchronous operations to prevent this issue.

## How to Reproduce

1. Clone the repository.
2. Run `node bug.js`.
3. Try to access the server in your browser or using `curl`. Observe that it might be unresponsive or slow to respond to requests during the long computation.

## Solution

The solution involves using asynchronous operations or offloading the long-running task to a worker thread or other process to avoid blocking the event loop.