# lerna-monorepo demo


1. Component Libraries
2. Modules
3. Utils libraries
4. Abstractions over React-Redux ( Optional but most organizations go with it)

## Component

Most organizations end up building their own component libraries and it is crucial to have it separated from the codebase for reusability of components. There exist a lot of libraries, but when you start building the product, you realize every library has something and misses something. Most commonly available libraries convey a standard UX design pattern. What if your designs don’t fit into those at a later point? So we need a separate components library where we can maintain organization-specific components.

## Modules

At first you may have one module or product, but over time it will grow. To avoid breaking existing modules over time and keeping change lists smaller and limited to individual products, it's essential to split a monolith into multiple modules to manage the chaos of each module within it without impacting other stable modules.

## Utils 

These are common to any project. Almost every one of us ends up creating utils folders in projects to help with little functions like converting currency or converting large numbers like 100000 as 100K and many more. Most of these functions are common and specific to organizations. E.g. a company working with statistics is going to have a helper function to convert large numbers into human-readable figures and eventually they end up copying the same code. Keeping utils separated gives us a unique opportunity to avoid code duplication of such cases and keep consistency across different modules.

## Abstractions over React-Redux

A lot of organizations prefer to do it. AWS, Microsoft Outlook, and many more have already adopted this strategy to abstract React & Redux bindings to create their own simplified functions to quickly bootstrap a new module/product into an existing ecosystem. This helps in faster delivery of new modules since developers don’t get into the same problems of bootstrapping and can focus on product problems rather than setting up the environment. One of the most simplified approaches is presented at react-redux-patch to reduce boilerplate. 