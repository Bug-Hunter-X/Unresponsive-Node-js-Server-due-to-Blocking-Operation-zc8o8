# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.

## Problem

The `blockingServer.js` file shows a simple HTTP server with a request handler that performs a 5-second CPU-bound task. This blocks the event loop, making the server unresponsive to new requests during that time. 

## Solution

The `nonblockingServer.js` file provides a solution by using asynchronous operations or offloading the task to worker threads.  This allows the event loop to continue processing other requests even while the long-running task is in progress. 

This example highlights the importance of asynchronous programming in Node.js to maintain responsiveness and scalability.