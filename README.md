# VUE.JS E-Commerce Project 

## Overview

### :mount_fuji: The Challenge

Wanting to combine one of my interests, building custom mechanical keyboards, with my pursuit of learning new web technologies such as Vue.JS, Typescript and Cypress, I decided to take on the challenge of building a fully fledged web store with the most important core functionalities.

Customers can enjoy a minimalistic and responsive design on desktop and mobile devices, a simple e-commerce flow, a robust, refresh persistent shopping cart and fast loading times, due to client side form validation and optimized image content.

Shop owners can easily add new products through the products file. Subsequently, product category boxes, product pages, page routes and SEO metadata are created automatically and components styled dynamically.

"Happy" and "unhappy" customer purchase flows have E2E tests, the navbar has implementation tests and the cart some component tests to gain a small impression of Cypress's abilities. 

## Process

### :wrench: Built with

- [Vue.js](https://vuejs.org/) - JS Frontend Framework
- [Vue Router](https://router.vuejs.org/) - The official Router for Vue.js
- [TypeScript](https://www.typescriptlang.org/) - JS but type safe
- [Vite.js](https://vitejs.dev/) - Packaging and frontend tooling
- [Crypess](https://www.cypress.io/) - Component and E2E Testing for JS
- [ESLint](https://eslint.org/) / [Prettier](https://prettier.io/) - Linting and formatting
- [Git](https://git-scm.com/) - Version control
- HTML5

### :bulb: What I've learned

#### Vue Router

- Use route parameters and props to create routes and render product pages dynamically, irrespective of the shop's catalog size
- Catch if customers have entered a wrong route or a missing product ID and forward them to the 404 page
- Lazy load/import pages to decrease loading times on landing page visit and further navigation
- Allow customers to go back to the previously seen page using a web history
- Adjust the scrolling behavior to reset the view to the page top when visiting a route
- Run logic, such as overwriting metadata, before entering a new route
  
#### Typescript

Although my use of TypeScript is at times "patchy", it has helped me a lot to find problems before they happened when it comes to passing props for components and using Pinia store functions with product data.

- Typescript basics such as interfaces, types, typed functions, generics etc.
- Use typed props and default props for Vue components to ensure the proper data is passed
- Enforce proper types for newly added shop products

#### Cypress Testing

- Write E2E tests for happy and unhappy customer paths
- Write isolated Component / Integration tests 
- Run tests for different viewport sizes
- Track and mock functions with spies and stubs

#### Search Engine Optimization (Open Graph / Meta Tags / Unhead / HTML Semantics)

- Add and change metadata dynamically within a single page application using Unhead
- Use Open Graph meta tags to offer customers a more pleasant experience when sharing the app on the web
- Semantically structure a web page with HTML tags such as header, main, section, article etc.

#### Page Optimization

- Use Lighthouse Report in Google Chrome to assess app performance
- Convert images to more web friendly, smaller format WEBP for faster loading times
- Use lazy loading on images
- Use Srcset for responsive images (learned, but not yet implemented)
- Lazy load pages (see Vue Router)

#### Code and project cleanliness

- Lint with ESLint
- Format with Prettier in combination with the TailwindCSS plugin to sort HTML classes
- Organize directories properly for a "bigger" project

