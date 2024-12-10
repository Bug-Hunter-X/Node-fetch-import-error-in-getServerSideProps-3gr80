# Next.js node-fetch Issue in getServerSideProps

This repository demonstrates a common error encountered when using `node-fetch` within the `getServerSideProps` function in a Next.js application.  The problem arises because API routes in Next.js have a different environment than the client-side and don't inherently support `node-fetch`.

## Problem

The `pages/about.js` file attempts to fetch data using `node-fetch` inside `getServerSideProps`.  This results in an error because `node-fetch` is not available in the API routes environment.

## Solution

The solution involves using the built-in `fetch` API provided by Next.js or a suitable alternative for server-side data fetching.