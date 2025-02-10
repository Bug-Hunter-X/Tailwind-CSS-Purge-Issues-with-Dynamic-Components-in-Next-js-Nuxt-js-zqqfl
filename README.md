# Tailwind CSS Purge Issues with Dynamic Components in Next.js/Nuxt.js

This repository demonstrates a common issue encountered when using Tailwind CSS with dynamic components in Next.js or Nuxt.js.  The problem stems from Tailwind's purge mechanism failing to correctly identify and include all necessary CSS classes for dynamically rendered content, particularly in server-side rendering (SSR) environments.  This often results in missing styles in dynamically generated components.

## Reproducing the Issue

Clone this repository and follow the instructions in the `bug.js` file to see how the bug manifests.  The `bug.js` file contains a simplified representation of a Next.js/Nuxt.js component that dynamically renders content. You'll notice that certain Tailwind CSS classes are missing resulting in improperly styled elements.

## Solution

The `bugSolution.js` file offers a solution to this problem. It demonstrates a method to effectively address the purge issues and ensure that all required Tailwind CSS classes are included in the final CSS output, even for dynamically generated components.

The primary approach to resolve this is to configure Tailwind's purge options correctly.  Ensure that the purge function is appropriately configured to identify classes from both static and dynamic content effectively. The solution includes options for customizing this behavior.