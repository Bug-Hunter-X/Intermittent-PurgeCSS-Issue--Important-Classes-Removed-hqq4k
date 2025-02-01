# Intermittent PurgeCSS Issue in Tailwind CSS

This repository demonstrates an uncommon bug encountered with PurgeCSS in Tailwind CSS.  The issue is intermittent; PurgeCSS removes crucial classes from the CSS output, leading to unexpected layout issues.  The bug seems to occur randomly and isn't consistently reproducible using the same codebase, making debugging challenging. This repository provides examples of the faulty code and a proposed solution.

## Setup

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm run build` to build the project.

## Reproduction Steps

1. Examine the `bug.js` file to see an example of code using Tailwind CSS classes that are intermittently removed by PurgeCSS.
2. Run `npm run build` multiple times. You will likely see the intermittent error where the important classes are purged.

## Solution

The `bugSolution.js` file contains a possible solution to mitigate this issue.  It incorporates strategies to ensure the important classes are not purged during the build process.  (This could include adding important comments to the classes, or refactoring for better PurgeCSS behavior) 

## Further Investigation

This is an uncommon bug, making it harder to diagnose. Further investigation may be required if the solution doesn't completely resolve the problem. This could involve analyzing PurgeCSS's configuration, reviewing the project's build process, or checking for conflicts with other plugins.