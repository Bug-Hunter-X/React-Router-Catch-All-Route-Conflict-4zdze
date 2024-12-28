# React Router Catch-All Route Conflict

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) interferes with other routes. The problem arises when the catch-all route is defined in a way that it unintentionally captures requests meant for other specific routes.

## Problem Description

The original `App.js` shows a setup where a catch-all route is placed after other, more specific routes.  This leads to the catch-all route always being matched regardless of the URL.

## Solution

The `AppSolution.js` demonstrates the solution. By ensuring that the catch-all route is placed *last* in the route definition, we ensure that it only matches if no other route matches.  This fixes the unintended route capturing.