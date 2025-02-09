# React Router v6 Nested Route Bug

This repository demonstrates a common issue encountered when using nested routes with React Router v6.  The problem occurs when a catch-all route (`/*`) is present; it intercepts all requests, preventing nested routes from rendering correctly.

## Bug Description

The provided `App.js` shows a simple setup with nested routes. However, due to the presence of the `/*` catch-all route, even when navigating to a nested path, the `NotFound` component will always render.

## Solution

The solution, implemented in `AppSolution.js`, addresses this problem by carefully ordering routes.  The catch-all route should always be the last route defined to allow for other routes to be matched first.