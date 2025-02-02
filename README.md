# Next.js 15 App Router - Unexpected Behavior with Dynamic Routes and Data Fetching

This repository demonstrates an unexpected behavior in Next.js 15's App Router when combining dynamic routes and data fetching.  The issue involves inconsistent data retrieval depending on the navigation method (initial load vs. client-side navigation).

## Bug Description

The bug occurs when fetching data within a page component using a dynamic route.  Upon initial load, the data fetches correctly, but subsequent client-side navigation to other routes using the dynamic segment results in an empty response or an error.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to `/posts/1` (initial load - works).
5. Navigate to `/posts/2` (client-side navigation - fails).

## Expected Behavior

Data should be fetched correctly regardless of the navigation method.

## Actual Behavior

Data fetching fails on client-side navigation to dynamic routes.

## Workaround

The `bugSolution.js` file shows how to work around this issue.