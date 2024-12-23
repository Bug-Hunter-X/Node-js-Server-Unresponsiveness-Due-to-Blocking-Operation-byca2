# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation blocking the event loop.  The `blockingServer.js` file shows the problematic code, while `nonblockingServer.js` provides a solution using asynchronous operations.

## Problem

The `blockingServer.js` file uses a `while` loop to simulate a long-running task within the request handler.  This blocks the event loop, preventing Node.js from handling other requests or events.  As a result, the server becomes unresponsive.

## Solution

The `nonblockingServer.js` file demonstrates how to resolve the issue by using asynchronous operations.  Real-world solutions often involve using Promises, async/await, or other techniques to prevent blocking the event loop.