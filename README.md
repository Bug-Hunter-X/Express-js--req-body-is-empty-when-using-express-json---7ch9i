# Express.js - Empty req.body with express.json()

This repository demonstrates a common issue in Express.js applications where `req.body` remains empty when using `express.json()` middleware, even though a JSON payload is sent in the request.

## Bug Description
The problem stems from incorrect or missing `Content-Type` headers in the request.  If the `Content-Type` header is not set to `application/json`, `express.json()` won't parse the request body correctly, resulting in an empty `req.body` object.

## Solution
Ensure that the client sending the request includes the `Content-Type: application/json` header.  This allows `express.json()` middleware to correctly parse the JSON payload into `req.body`.