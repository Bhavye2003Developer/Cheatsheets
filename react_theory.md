# What is CDN? Why Use CDN?

## CDN (Content Delivery Network)
A CDN is a network of servers designed to provide resources such as images, files, etc., to users efficiently. These servers are strategically placed around the world and are called edge servers. The locations where they are situated are known as points of presence (POP). By fetching data from the nearest server, CDN reduces latency and increases efficiency.

## Cross-Origin
Cross-origin is a mechanism that allows a domain to request resources from another domain securely to display on its own domain. The requests can be made anonymously or with user credentials.

## CORS (Cross-Origin Resource Sharing)
CORS is used when you have a backend on one domain and a frontend on another. To ensure that only your frontend can access your backend, you restrict access to your backend, preventing other domains from accessing it. This ensures controlled access to the domain.

## React: Library, Not a Framework
- **React.createElement:** Creates a ReactElement inside React, returning an object that gets converted to an HTML element.
- **ReactDOM.createRoot:** Creates a root for a React app connected to an HTML element.
- **root.render:** Puts the ReactElement (object) into the HTML page by converting it into an HTML element.

### Rendering
Rendering involves changing/manipulating the actual DOM. When a ReactElement is rendered onto the DOM, it becomes an HTML element.

## npm (Node Package Manager)
npm manages packages that are installed in a project, their versions, and dependencies. It doesn't stand for "Node Package Manager," but it manages the packages and dependencies for a project.

### package.json
A configuration file for npm that contains all the packages and their versions required for the project.

### Bundlers
Node packages that bundle the app for production, minimizing, optimizing, and caching the code. Examples include Webpack, Vite, and Parcel.

### Types of Dependencies
- **Dev Dependencies:** Required during the development phase, installed with `npm install -D`.
- **Normal Dependencies:** Used in production as well.

### package-lock.json
Tracks the exact version of each package used in the project.

## Parcel
- **Features:**
  - Bundling
  - Dev build
  - Local server
  - HMR (Hot Module Replacement)
  - File Watching Algorithm (written in C++)
  - Faster builds due to caching
  - Image optimization
  - Minification of files in production
  - Compression
  - Consistent hashing
  - Diagnostics
  - Tree shaking (removing unused code)
  - Different dev and production bundles
  - Differential bundling (supporting older browsers)

### Commands
- `npx parcel build index.html`: Builds the project.
- `npx parcel index.html` or `npm run start`: Starts the project.

## JSX (JavaScript XML)
JSX is an HTML-like or XML-like syntax that gets transpiled before it reaches the JS engine in the browser. Parcel uses Babel to transpile JSX into `React.createElement`, which returns a ReactElement (object) rendered as an HTML element.

### React Components
Everything in React is a component, either class-based or functional.

#### Functional Components
Normal JavaScript functions that return JSX or a ReactElement.

#### Component Composition
Components inside other components.

### React Hooks
Helper functions that keep the UI layer consistent with the data layer.

- **useState:** Generates state variables and updates the UI as data changes.
- **useEffect:** Takes a callback function and a dependency array, controlling when the effect runs.

## Monolith vs. Microservice Architecture
- **Monolith Architecture:** A large project containing APIs, UI, Auth, DB, SMS, etc., where a small change requires rebuilding the entire project.
- **Microservice Architecture:** Different services for different jobs, deployed independently and interacting via ports.

### Data Fetching
- **On page load:** API call followed by rendering the UI.
- **On page load with rerender:** Render UI first, then make an API call and rerender the UI with the fetched data for better UX.

## React: SPA (Single Page Application)
SPAs load components interchangeably as routes change without reloading the entire page.

### Routing Types
- **Client-Side Routing:** Components load without making network calls for separate pages.
- **Server-Side Routing:** Fetches pages from the server, reloading the entire page.

## GraphQL
Deals with overfetching data, loading only the required data for the app from complex JSON.

## Rendering Phases
- **Render Phase:** Finding differences between the old and new state of components (reconciliation).
- **Commit Phase:** Actually updating the DOM.

## Single Responsibility Principle
Each component should have a single responsibility, leading to modular, maintainable, testable, and reusable code.

### Custom Hooks
Normal utility functions with their own state and lifecycle that can use other hooks.

### Code Splitting
Breaking the app into smaller chunks to load components only when needed, reducing the bundle size.

## Writing CSS
- **Normal CSS**
- **Sass/SCSS**
- **Styled Components**
- **UI Libraries:** Chakra UI, Bootstrap, Ant Design, MUI, Tailwind CSS

## Higher-Order Component
A function that takes a component, adds extra features, modifies it, and returns the modified component.

## Controlled Components
Components controlled by parent components via state.

## Props Drilling
Passing props through multiple components to get data to the required component. This can be avoided using React Context or state management libraries like Redux.

## Redux: State Management
- **Redux Store:** A global object containing slices to avoid a cluttered store.
- **Slices:** Logical partitions within the store.
- **Reducers:** Functions that modify slices.
- **Selectors:** Functions to read data from slices, subscribing to the store to automatically update components when data changes.

## useRef
Similar to useState but doesn't cause rerender when its value changes.

## Debouncing and Throttling
- **Debouncing:** Ensures a function executes only after a certain amount of time has passed since its last invocation.
- **Throttling:** Ensures a function executes at most once every specified interval.

## Memoization
Remembering output given an input to avoid recomputation, similar to caching. Use `useMemo` for variables dependent on state variables.

## React Context
Avoids props drilling by providing a global store accessible by any component.

## Custom Hooks
Small functions containing other hooks to manage side effects and state in functional components.
