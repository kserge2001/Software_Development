# Node.js: A Comprehensive Guide from Beginner to Senior

## Table of Contents

### 🌱 Beginner Level
- [Introduction to Node.js](#introduction-to-nodejs)
- [Setting Up the Development Environment](#setting-up-the-development-environment)
- [Node.js Fundamentals](#nodejs-fundamentals)
- [Working with Modules](#working-with-modules)
- [Basic Asynchronous Programming](#basic-asynchronous-programming)
- [Essential Built-in Modules](#essential-built-in-modules)
- [npm and Package Management](#npm-and-package-management)
- [Building Simple CLI Applications](#building-simple-cli-applications)

### 🚀 Intermediate Level
- [Express.js Framework](#expressjs-framework)
- [RESTful API Development](#restful-api-development)
- [Advanced Asynchronous Patterns](#advanced-asynchronous-patterns)
- [Database Integration](#database-integration)
- [Authentication and Authorization](#authentication-and-authorization)
- [Error Handling and Debugging](#error-handling-and-debugging)
- [Working with TypeScript](#working-with-typescript)
- [Testing Node.js Applications](#testing-nodejs-applications)

### 🏆 Senior Level
- [Advanced Design Patterns](#advanced-design-patterns)
- [Microservices Architecture](#microservices-architecture)
- [Scalability and Performance Optimization](#scalability-and-performance-optimization)
- [Security Best Practices](#security-best-practices)
- [Containerization and Orchestration](#containerization-and-orchestration)
- [CI/CD and DevOps for Node.js](#cicd-and-devops-for-nodejs)
- [Monitoring and Logging](#monitoring-and-logging)
- [Building Production-Ready Applications](#building-production-ready-applications)

### 📚 Additional Resources
- [Node.js Project Examples](#nodejs-project-examples)
- [Community and Continued Learning](#community-and-continued-learning)
## 🌱 Beginner Level

## Introduction to Node.js

### What is Node.js?

Node.js is an open-source, cross-platform JavaScript runtime environment that executes JavaScript code outside of a web browser. It allows developers to use the same language (JavaScript) for both client and server-side programming, enabling the development of fast and scalable network applications.

### History and Evolution

- Created by Ryan Dahl in 2009 to address the limitations of traditional web servers
- Initially released for Linux only, now fully cross-platform
- Built on Chrome's V8 JavaScript engine (same engine that powers Google Chrome)
- Evolved from version 0.x to current LTS (Long Term Support) versions
- Managed by the OpenJS Foundation (formerly the Node.js Foundation)
- Significant milestones:
  - 2009: Initial release
  - 2011: Introduction of npm
  - 2015: Node.js Foundation formed and io.js merger
  - 2018: Node.js 10.0.0 with improved performance and diagnostic tools
  - 2019: Node.js 12.0.0 with ES6 modules support
  - 2021: Node.js 16.0.0 with stable timers promises API
  - 2023: Node.js 20.0.0 with enhanced performance and feature set

### Why Use Node.js?

- **JavaScript Everywhere**: Use the same language for frontend and backend development
- **Non-blocking I/O**: Asynchronous and event-driven architecture makes it efficient for I/O operations
- **Single-threaded Event Loop**: Efficiently handles concurrent connections with a single thread
- **Fast Execution**: V8 engine provides fast JavaScript execution by compiling to machine code
- **Rich Ecosystem**: npm (Node Package Manager) is the largest software registry in the world
- **Lightweight and Efficient**: Small memory footprint and optimal resource consumption
- **Corporate Adoption**: Used by major companies including Netflix, PayPal, Uber, LinkedIn, and NASA
- **Strong Community**: Active development community with frequent updates and enhancements

### Common Use Cases

- **Web APIs and Backends**: Building fast, scalable RESTful services
- **Real-time Applications**: Chat applications, collaboration tools, live updates
- **Streaming Services**: Video/audio streaming platforms with efficient data handling
- **Microservices Architecture**: Building small, focused services that work together
- **Single Page Applications**: Backend services for modern web applications
- **Command-line Tools**: Creating cross-platform utilities and development tools
- **Internet of Things (IoT)**: Lightweight server for IoT devices and data processing
- **DevOps and Tooling**: Build systems, task runners, and automation tools

### Node.js vs Traditional Server-side Technologies

| Feature | Node.js | PHP | Python | Java | Ruby |
|---------|---------|-----|--------|------|------|
| **Execution Model** | Non-blocking, Event-driven | Primarily blocking | Primarily blocking | Multi-threaded | Primarily blocking |
| **Performance** | High (for I/O operations) | Moderate | Moderate | High | Moderate |
| **Concurrency** | Event Loop | Process/Thread per Request | Asyncio/Threads | Threads | Process/Threads |
| **Learning Curve** | Moderate (if familiar with JS) | Low to Moderate | Low | Steep | Low to Moderate |
| **Ecosystem** | Very large (npm) | Large (Composer) | Very large (pip) | Very large (Maven) | Large (RubyGems) |
| **Use Cases** | Real-time, API, Microservices | Web applications, CMS | Data science, Web, Automation | Enterprise, Android, Big Data | Web applications, Prototyping |

### When to Use Node.js (and When Not To)

**Ideal for:**
- I/O intensive applications (APIs, data streaming)
- Real-time applications requiring live updates
- Single page applications with JSON APIs
- Applications benefiting from JavaScript on both ends
- Rapid prototyping and development

**Less ideal for:**
- CPU-intensive applications (complex calculations, data processing)
- Heavy server-side rendering applications
- Applications requiring mature, stable patterns (where other languages have established solutions)

### Practice Exercise: Node.js Exploration

1. **Research Task**: Find and list five major companies using Node.js in production. For each company, identify:
   - What they're using Node.js for
   - Why they chose Node.js
   - Any performance or development benefits they've reported

2. **Comparison Activity**: Compare Node.js with a server-side technology you're familiar with:
   - Create a table comparing features, strengths, and weaknesses
   - Identify scenarios where each would be the better choice
   - Consider factors like development speed, performance, and maintainability

3. **Case Study Analysis**: Pick an application type (e.g., chat app, content management system, e-commerce platform) and:
   - Outline how you would architect it in Node.js
   - Identify the key Node.js strengths that benefit this particular application
   - Describe potential challenges and how you might address them

## Setting Up the Development Environment

This section covers everything you need to get started with Node.js development, from installation to creating your first application.

### Installing Node.js

#### Windows

1. Visit the [Node.js official website](https://nodejs.org/)
2. Download the LTS (Long Term Support) version
3. Run the installer and follow the installation wizard
4. Verify installation by opening Command Prompt and typing:
   ```bash
   node -v
   npm -v
   ```

#### macOS

1. Using Homebrew (recommended):
   ```bash
   brew install node
   ```
2. Using the installer:
   - Download the macOS installer from the [Node.js website](https://nodejs.org/)
   - Run the installer and follow the prompts
3. Verify installation:
   ```bash
   node -v
   npm -v
   ```

#### Linux

1. Ubuntu/Debian:
   ```bash
   curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
   sudo apt-get install -y nodejs
   ```

2. Fedora:
   ```bash
   sudo dnf install nodejs
   ```

3. Arch Linux:
   ```bash
   sudo pacman -S nodejs npm
   ```

4. Verify installation:
   ```bash
   node -v
   npm -v
   ```

### Version Management with NVM (Recommended)

NVM (Node Version Manager) allows you to install and manage multiple Node.js versions, which is essential for working with different projects:

#### Installing NVM (macOS/Linux)

```bash
# Install NVM
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

# Add to your profile (if not done automatically)
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"

# Verify installation
nvm --version
```

#### Installing NVM (Windows)

## Core Concepts

### Event Loop

The event loop is a fundamental concept in Node.js that enables non-blocking I/O operations.

#### How the Event Loop Works

1. JavaScript code is executed synchronously until the call stack is empty
2. Asynchronous operations (I/O, timers, etc.) are offloaded to the system kernel when possible
3. When asynchronous operations complete, the associated callbacks enter the callback queue
4. Once the call stack is empty, the event loop picks callbacks from the queue and executes them

#### Event Loop Phases

1. **Timers**: Executes callbacks scheduled by `setTimeout()` and `setInterval()`
2. **Pending callbacks**: Executes I/O callbacks deferred to the next loop iteration
3. **Idle, prepare**: Used internally by Node.js
4. **Poll**: Retrieves new I/O events and executes their callbacks
5. **Check**: Executes callbacks scheduled by `setImmediate()`
6. **Close callbacks**: Executes close event callbacks (e.g., `socket.on('close', ...)`)

#### Example: Understanding the Event Loop

```javascript
console.log('Script start');

setTimeout(() => {
  console.log('setTimeout');
}, 0);

setImmediate(() => {
  console.log('setImmediate');
});

process.nextTick(() => {
  console.log('nextTick');
});

Promise.resolve().then(() => {
  console.log('Promise resolved');
});

console.log('Script end');
```

Output:
```
Script start
Script end
nextTick
Promise resolved
setTimeout
setImmediate
```

### Modules

Node.js uses modules to organize code into reusable components.

#### CommonJS Modules (Traditional Node.js)

```javascript
// math.js
function add(a, b) {
  return a + b;
}

function subtract(a, b) {
  return a - b;
}

module.exports = {
  add,
  subtract,
};
```

```javascript
// app.js
const math = require('./math');

console.log(math.add(5, 3));      // 8
console.log(math.subtract(5, 3)); // 2
```

#### ECMAScript Modules (ES Modules)

As of Node.js 14+, ES Modules are supported natively.

```javascript
// mathES.mjs
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}

// Export default
export default function multiply(a, b) {
  return a * b;
}
```

```javascript
// appES.mjs
import multiply, { add, subtract } from './mathES.mjs';

console.log(add(5, 3));       // 8
console.log(subtract(5, 3));  // 2
console.log(multiply(5, 3));  // 15
```

To use ES Modules:
- Use `.mjs` extension, OR
- Set `"type": "module"` in package.json

#### Built-in Modules

```javascript
// Using built-in modules
const fs = require('fs');
const path = require('path');
const http = require('http');

// Reading a file
fs.readFile(path.join(__dirname, 'example.txt'), 'utf8', (err, data) => {
  if (err) {
    console.error('Error reading file:', err);
    return;
  }
  console.log('File content:', data);
});
```

### NPM (Node Package Manager)

NPM is the default package manager for Node.js and the world's largest software registry.

#### Managing Dependencies

```bash
# Initialize a new project
npm init

# Install a package and save as dependency
npm install express

# Install a package and save as dev dependency
npm install jest --save-dev

# Install a specific version
npm install lodash@4.17.21

# Install packages globally
npm install -g nodemon

# Update packages
npm update

# List installed packages
npm list
```

#### package.json

The `package.json` file manages project dependencies and settings:

```json
{
  "name": "my-node-app",
  "version": "1.0.0",
  "description": "A sample Node.js application",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js",
    "test": "jest"
  },
  "dependencies": {
    "express": "^4.17.1",
    "mongoose": "^6.0.7"
  },
  "devDependencies": {
    "jest": "^27.2.0",
    "nodemon": "^2.0.12"
  }
}
```

#### Using Package Scripts

```bash
# Run the start script
npm start

# Run the dev script
npm run dev

# Run the test script
npm test
```

#### Creating and Publishing NPM Packages

```bash
# Create a new package
mkdir my-package
cd my-package
npm init

# Publish package
npm login
npm publish
```

### Practice Exercise: Working with Modules and NPM

1. Create a module that exports utility functions (e.g., string manipulation, math operations)
2. Create a main application that imports and uses these functions
3. Add a third-party package like `lodash` or `moment` to your project
4. Set up a npm script that runs your application with nodemon
5. Create a program that demonstrates the event loop by using setTimeout, setImmediate, and process.nextTick

## Asynchronous Programming

Node.js is built around asynchronous programming to handle concurrent operations efficiently.

### Callbacks

Callbacks are functions passed as arguments to other functions, to be executed after a certain operation completes.

```javascript
// Example: Reading a file with callbacks
const fs = require('fs');

fs.readFile('example.txt', 'utf8', (err, data) => {
  if (err) {
    console.error('Error reading file:', err);
    return;
  }
  console.log('File content:', data);
});

console.log('Reading file...');
```

#### Callback Hell

Nested callbacks can lead to "callback hell" or "pyramid of doom":

```javascript
fs.readFile('file1.txt', 'utf8', (err, data1) => {
  if (err) {
    console.error(err);
    return;
  }
  fs.readFile('file2.txt', 'utf8', (err, data2) => {
    if (err) {
      console.error(err);
      return;
    }
    fs.readFile('file3.txt', 'utf8', (err, data3) => {
      if (err) {
        console.error(err);
        return;
      }
      // Process data1, data2, and data3
      console.log(data1, data2, data3);
    });
  });
});
```

### Promises

Promises provide a cleaner way to handle asynchronous operations and avoid callback hell.

```javascript
// Creating a promise
const fs = require('fs').promises;

// Using promises
fs.readFile('example.txt', 'utf8')
  .then(data => {
    console.log('File content:', data);
    return fs.readFile('example2.txt', 'utf8');
  })
  .then(data => {
    console.log('Second file content:', data);
  })
  .catch(err => {
    console.error('Error reading file:', err);
  });

// Creating custom promises
function readFilePromise(filePath) {
  return new Promise((resolve, reject) => {
    fs.readFile(filePath, 'utf8', (err, data) => {
      if (err) {
        reject(err);
      } else {
        resolve(data);
      }
    });
  });
}

// Using Promise.all to run promises in parallel
Promise.all([
  fs.readFile('file1.txt', 'utf8'),
  fs.readFile('file2.txt', 'utf8'),
  fs.readFile('file3.txt', 'utf8'),
])
  .then(([data1, data2, data3]) => {
    console.log(data1, data2, data3);
  })
  .catch(err => {
    console.error('Error reading files:', err);
  });
```

### Async/Await

Async/await is a more modern and readable syntax for working with promises.

```javascript
// Basic async/await syntax
const fs = require('fs').promises;

async function readFiles() {
  try {
    const data1 = await fs.readFile('file1.txt', 'utf8');
    const data2 = await fs.readFile('file2.txt', 'utf8');
    console.log(data1, data2);
  } catch (err) {
    console.error('Error reading files:', err);
  }
}

readFiles();

// Parallel execution with async/await
async function readFilesParallel()

# Node.js: A Comprehensive Guide

## Table of Contents
- [Introduction to Node.js](#introduction-to-nodejs)
- [Node.js Architecture and Event Loop](#nodejs-architecture-and-event-loop)
- [Setting Up the Development Environment](#setting-up-the-development-environment)
- [Core Modules and Global Objects](#core-modules-and-global-objects)
- [NPM and Package Management](#npm-and-package-management)
- [File System Operations](#file-system-operations)
- [Creating HTTP Servers](#creating-http-servers)
- [Express.js Framework](#expressjs-framework)
- [RESTful API Development](#restful-api-development)
- [Database Integration](#database-integration)
- [Authentication and Security](#authentication-and-security)
- [Error Handling and Debugging](#error-handling-and-debugging)
- [Deployment and Production](#deployment-and-production)
- [Best Practices](#best-practices)
- [Sample Projects and Real-world Applications](#sample-projects-and-real-world-applications)
- [Resources for Further Learning](#resources-for-further-learning)

## Introduction to Node.js

### What is Node.js?

Node.js is an open-source, cross-platform JavaScript runtime environment that executes JavaScript code outside a web browser. It allows developers to use JavaScript to write command-line tools and server-side scripts to produce dynamic web page content before the page is sent to the user's browser.

### History and Evolution

- Created by Ryan Dahl in 2009
- Built on Chrome's V8 JavaScript engine
- Initially focused on providing an event-driven, non-blocking I/O model
- Gained popularity as a solution for scalable network applications
- Has evolved with significant improvements in performance, stability, and features
- Maintained by the Node.js Foundation (merged into the OpenJS Foundation)

### Why Use Node.js?

- **JavaScript Everywhere**: Allows developers to use JavaScript for both client and server-side programming
- **Asynchronous & Non-blocking**: Efficiently handles concurrent operations without creating multiple threads
- **Fast Execution**: V8 engine compiles JavaScript to native machine code before execution
- **Rich Ecosystem**: Huge library of open-source packages via npm
- **Cross-platform**: Runs on Windows, macOS, Linux, and other operating systems
- **Lightweight and Efficient**: Perfect for microservices and real-time applications
- **Corporate Adoption**: Used by major companies like Netflix, PayPal, Uber, LinkedIn, and Walmart

### Node.js vs Traditional Server-side Languages

Comparing Node.js with languages like PHP, Python, Ruby, and Java:

- **Single-threaded vs Multi-threaded**: Node.js uses a single thread with event-based callbacks, while many traditional languages use multiple threads
- **Asynchronous vs Synchronous**: Node.js is designed for non-blocking operations, while many traditional languages use blocking operations by default
- **JavaScript Ecosystem**: Allows sharing code between frontend and backend
- **Performance**: Generally faster for I/O-intensive operations, may not be optimal for CPU-intensive tasks

### Use Cases

#### Perfect for:
- Real-time applications (chat, gaming)
- Single-page applications
- APIs and microservices
- Streaming applications
- Command-line tools
- IoT (Internet of Things) applications

#### Not ideal for:
- CPU-intensive applications
- Heavy computational tasks
- Applications requiring thread-level parallelism

### Practice Exercise: Understanding Node.js

1. Research and list 5 popular applications built with Node.js
2. Compare Node.js to a traditional server-side language you're familiar with
3. Define a scenario where Node.js would be the ideal choice and explain why

## Node.js Architecture and Event Loop

### V8 JavaScript Engine

The V8 engine is the core component that executes JavaScript code in Node.js:

- Developed by Google for Chrome
- Compiles JavaScript to machine code rather than interpreting it
- Provides memory management and garbage collection
- Implements ECMAScript standards

### Single-Threaded Nature

Node.js operates primarily on a single thread, but that doesn't mean it can only perform one operation at a time:

- The main thread executes JavaScript code
- I/O operations are offloaded to system kernels whenever possible
- Callbacks are triggered when operations complete
- This architecture allows handling thousands of concurrent connections

### The Event Loop

The event loop is the heart of Node.js asynchronous programming model:

```
   ┌───────────────────────────┐
┌─>│           timers          │
│  └─────────────┬─────────────┘
│  ┌─────────────┴─────────────┐
│  │     pending callbacks     │
│  └─────────────┬─────────────┘
│  ┌─────────────┴─────────────┐
│  │       idle, prepare       │
│  └─────────────┬─────────────┘      ┌───────────────┐
│  ┌─────────────┴─────────────┐      │   incoming:   │
│  │           poll            │<─────┤  connections, │
│  └─────────────┬─────────────┘      │   data, etc.  │
│  ┌─────────────┴─────────────┐      └───────────────┘
│  │           check           │
│  └─────────────┬─────────────┘
│  ┌─────────────┴─────────────┐
└──┤      close callbacks      │
   └───────────────────────────┘
```

The event loop goes through these phases in order:

1. **Timers**: Execute callbacks scheduled by `setTimeout()` and `setInterval()`
2. **Pending callbacks**: Execute I/O callbacks deferred to the next loop iteration
3. **Idle, prepare**: Used internally
4. **Poll**: Retrieve new I/O events; execute I/O related callbacks
5. **Check**: Execute `setImmediate()` callbacks
6. **Close callbacks**: Execute close event callbacks (e.g., socket.on('close', ...))

### Non-blocking I/O

Node.js handles I/O operations asynchronously:

```javascript
// Blocking code example (NOT Node.js style)
const data = fs.readFileSync('/path/to/file');
console.log(data);
console.log('File reading complete');

// Non-blocking code example (Node.js style)
fs.readFile('/path/to/file', (err, data) => {
    if (err) throw err;
    console.log(data);
});
console.log('File reading started'); // This executes before the file is read
```

### Libuv

Libuv is a multi-platform support library that provides the event loop and asynchronous I/O:

- Abstracts operating system differences
- Provides thread pool for operations that can't be done asynchronously at the OS level
- Handles file system operations, DNS resolution, and networking

### Worker Threads

For CPU-intensive tasks, Node.js provides Worker Threads:

```javascript
const { Worker, isMainThread, parentPort, workerData } = require('worker_threads');

if (isMainThread) {
    // This code runs in the main thread
    const worker = new Worker(__filename, {
        workerData: { someData: 'Hello from main thread' }
    });
    
    worker.on('message', (message) => {
        console.log(`Message from worker: ${message}`);
    });
    
    worker.on('error', (error) => {
        console.error(error);
    });
    
    worker.on('exit', (code) => {
        if (code !== 0) {
            console.error(`Worker stopped with exit code ${code}`);
        }
    });
} else {
    // This code runs in the worker thread
    console.log(`Worker received: ${workerData.someData}`);
    
    // Perform CPU-intensive task
    const result = performComplexCalculation();
    
    // Send result back to main thread
    parentPort.postMessage(result);
}

function performComplexCalculation() {
    // Simulate CPU-intensive work
    let result = 0;
    for (let i = 0; i < 10000000; i++) {
        result += i;
    }
    return result;
}
```

### Practice Exercise: Event Loop and Asynchronous Code

1. Write a program that demonstrates the non-blocking nature of Node.js:
   - Read a file asynchronously
   - While the file is being read, log messages to the console
   - After the file is read, log its contents

2. Implement a simple task that uses `setTimeout`, `setImmediate`, and `process.nextTick` to demonstrate the event loop phases

## Setting Up the Development Environment

### Installing Node.js

#### Windows, macOS, and Linux
1. Visit the [official Node.js website](https://nodejs.org/)
2. Download the LTS (Long Term Support) version
3. Follow the installation instructions for your OS
4. Verify installation by opening a terminal and running:
   ```
   node -v
   npm -v
   ```

#### Using a Version Manager (Recommended)

For macOS/Linux:
```bash
# Install NVM (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

# Install Node.js
nvm install --lts

# Switch between versions
nvm use 16  # Use Node.js version 16.x
```

For Windows:
- Download and install [nvm-windows](https://github.com/coreybutler/nvm-windows)

### Code Editors and IDEs

Several code editors work well for Node.js development:

- **Visual Studio Code** (recommended)
  - Free and open-source
  - Built-in debugging
  - Excellent JavaScript/TypeScript support
  - Useful extensions: ESLint, Prettier, Node.js Extension Pack

- **WebStorm**
  - Commercial IDE specifically for JavaScript
  - Powerful features and integrations
  - Built-in tools for Node.js

- **Atom**, **Sublime Text**, or **Vim**
  - Lightweight alternatives with plugin support

### Essential Tools

#### Debugging Tools
- Built-in Node.js debugger
- Chrome DevTools for Node.js
- VS Code debugging

```bash
# Basic debugging with Node.js
node inspect app.js

# With Chrome DevTools
node --inspect app.js
# Then open Chrome and navigate to chrome://inspect
```

#### Development Utilities
- **nodemon**: Automatically restart applications when file changes are detected
```bash
npm install -g nodemon
nodemon app.js
```

- **npm** or **yarn**: Package managers
- **ESLint**: Code linting
- **Prettier**: Code formatting

### Hello World in Node.js

Create a file called `app.js`:

```javascript
// Load the HTTP module
const http = require('http');

// Set the hostname and port
const hostname = '127.0.0.1';
const port = 3000;

// Create the HTTP server
const server = http.createServer((req, res) => {
  // Set the response HTTP header
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  
  // Send the response
  res.end('Hello, World!\n');
});

// Start the server
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

Run the server:
```bash
node app.js
```

Visit `http://localhost:3000` in your browser to see "Hello, World!".

### Practice Exercise: Environment Setup

1. Install Node.js using a version manager
2. Set up your preferred code editor with extensions for Node.js development
3. Create a "Hello World" HTTP server
4. Modify the server to serve different messages based on the URL path
5. Install and use nodemon to automatically restart your server when changes are made

## Core Modules and Global Objects

### Core Modules

Node.js comes with several built-in modules that provide essential functionality:

#### HTTP/HTTPS
For creating web servers and making HTTP requests:

```javascript
const http = require('http');

// Create a simple server
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});

server.listen(3000, '127.0.0.1', () => {
  console.log('Server running at http://127.0.0.1:3000/');
});

// Make an HTTP request
http.get('http://example.com', (res) => {
  let data = '';
  
  res.on('data', (chunk) => {
    data += chunk;
  });
  
  res.on('end', () => {
    console.log(data);
  });
}).on('error', (err) => {
  console.error(`Error: ${err.message}`);
});
```

#### File System (fs)
For working with files and directories:

```javascript
const fs = require('fs');

// Synchronous file reading
try {
  const data = fs.readFileSync('file.txt', 'utf8');
  console.log(data);
} catch (err) {
  console.error(err);
}

// Asynchronous file reading
fs.readFile('file.txt', 'utf8', (err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(data);
});

// Promises-based API (Node.js 10+)
const fsPromises = fs.promises;

async function readFile() {
  try {
    const data = await fsPromises.readFile('file.txt', 'utf8');
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}

readFile();
```

#### Path
For working with file and directory paths:

```javascript
const path = require('path');

// Platform-independent path handling
const filePath = path.join(__dirname, 'subfolder', 'file.txt');
console.log(filePath);

// Path components
console.log(path.basename(filePath)); // file.txt
console.log(path.dirname(filePath));  // /path/to/subfolder
console.log(path.extname(filePath));  // .txt

// Resolve absolute path
console.log(path.resolve('subfolder', 'file.txt'));

// Normalize path
console.log(path.normalize('/path//to/////file.txt')); // /path/to/file.txt
```

#### Events
For working with event-driven architecture:

```javascript
const EventEmitter = require('events');

// Create custom event emitter
class MyEmitter extends EventEmitter {}
const myEmitter = new MyEmitter();

// Register event listener
myEmitter.on('event', (a, b) => {
  console.log(a, b);
});

// Emit event
myEmitter.emit('event', 'Hello', 'World');
```

#### Utility Modules
Other commonly used core modules:

- **os**: Operating system-related information
- **url**: URL parsing and formatting
- **querystring**: Parse and format URL query strings
- **crypto**: Cryptographic functionality
- **stream**: Working with streaming data
- **buffer**: Handling binary data
- **child_process**: Spawn subprocesses
- **util**: Utility functions
- **assert**: For testing
- **zlib**: Compression/decompression

### Global Objects

Node.js provides several global objects available in all modules:

#### global
The global namespace object (similar to `window` in browsers):

```javascript
global.customVariable = 'This is global';
console.log(customVariable); // 'This is global'
```

#### process
Information about the current Node.js process:

```javascript
// Current working directory
console.log(process.cwd());

// Environment variables
console.log(process.env.NODE_ENV);

// Command-line arguments
console.log(process.argv);

// Process ID
console.log(process.pid);

// Exit

