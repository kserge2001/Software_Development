# GitHub Actions: A Comprehensive Guide

## Table of Contents

### 🌱 Getting Started
- [Introduction to GitHub Actions](#introduction-to-github-actions)
- [Key Concepts and Components](#key-concepts-and-components)
- [Your First Workflow](#your-first-workflow)
- [Understanding YAML Syntax](#understanding-yaml-syntax)

### 🚀 Building Effective Workflows
- [Workflow Syntax Reference](#workflow-syntax-reference)
- [Events and Triggers](#events-and-triggers)
- [Jobs and Steps](#jobs-and-steps)
- [Working with Runners](#working-with-runners)
- [Using Actions](#using-actions)
- [Managing Dependencies](#managing-dependencies)

### 💼 Common Use Cases
- [Continuous Integration](#continuous-integration)
- [Automated Testing](#automated-testing)
- [Package Publishing](#package-publishing)
- [Deployment Automation](#deployment-automation)
- [Code Quality Checks](#code-quality-checks)
- [Scheduled Tasks](#scheduled-tasks)

### 🏆 Advanced Techniques
- [Matrix Builds](#matrix-builds)
- [Reusable Workflows](#reusable-workflows)
- [Composite Actions](#composite-actions)
- [Environment Management](#environment-management)
- [Workflow Optimization](#workflow-optimization)
- [Self-hosted Runners](#self-hosted-runners)

### 🔒 Security and Best Practices
- [Secrets Management](#secrets-management)
- [Security Hardening](#security-hardening)
- [Handling Sensitive Data](#handling-sensitive-data)
- [Workflow Best Practices](#workflow-best-practices)
- [GitHub Actions Auditing](#github-actions-auditing)

### 🛠️ Building Custom Actions
- [Types of Custom Actions](#types-of-custom-actions)
- [JavaScript Actions](#javascript-actions)
- [Docker Container Actions](#docker-container-actions)
- [Composite Run Steps Actions](#composite-run-steps-actions)
- [Publishing Actions](#publishing-actions)

### 🌐 Enterprise Implementation
- [Organization-wide Workflows](#organization-wide-workflows)
- [GitHub Actions at Scale](#github-actions-at-scale)
- [Compliance and Governance](#compliance-and-governance)
- [Cost Management](#cost-management)
- [Integration with Enterprise Systems](#integration-with-enterprise-systems)

### 📚 Real-world Examples
- [Complete CI/CD Pipeline](#complete-cicd-pipeline)
- [Multi-platform Build System](#multi-platform-build-system)
- [Microservices Deployment](#microservices-deployment)
- [Release Management](#release-management)
- [Infrastructure as Code](#infrastructure-as-code)

## 🌱 Getting Started

## Introduction to GitHub Actions

GitHub Actions is a powerful automation platform integrated directly into GitHub repositories. It enables you to automate software development workflows right from your GitHub repository, making it easy to build, test, and deploy code.

### What is GitHub Actions?

GitHub Actions is a CI/CD (Continuous Integration/Continuous Delivery) platform that allows you to automate your build, test, and deployment pipeline. You can create workflows that build and test every pull request to your repository, or deploy merged pull requests to production.

### Why Use GitHub Actions?

- **Native Integration**: Built directly into GitHub, eliminating the need for third-party CI/CD services.
- **Community Actions**: Leverage thousands of pre-built actions from the GitHub Marketplace.
- **Infrastructure Management**: GitHub manages the infrastructure, so you don't have to provision, manage, or pay for additional servers.
- **Flexible Workflows**: Build workflows that match your project's specific needs.
- **Matrix Builds**: Easily test against multiple operating systems, platforms, and language versions.
- **Free for Public Repositories**: Generous free tier even for private repositories.

### How GitHub Actions Differs from Other CI/CD Tools

Compared to tools like Jenkins, Travis CI, CircleCI, or GitLab CI/CD, GitHub Actions offers:

1. **Tighter GitHub Integration**: Direct access to GitHub events, repository data, and branch information.
2. **Extensive Marketplace**: Thousands of community-created actions you can include in your workflows.
3. **Simple Workflow Definition**: YAML-based workflow files stored in your repository.
4. **No Additional Accounts**: Uses your existing GitHub account and permissions.
5. **Free Hosted Runners**: Linux, Windows, and macOS runners provided by GitHub.

### Basic Concepts: Workflow, Job, Step, Action

GitHub Actions is structured around several key concepts:

- **Workflow**: An automated procedure that you add to your repository, composed of one or more jobs.
- **Job**: A section of a workflow that executes on the same runner (virtual environment).
- **Step**: A task within a job that can run a script or an action.
- **Action**: A reusable unit of code that can be shared and used in workflows.
- **Event**: An activity that triggers a workflow run (e.g., push, pull request, issue creation).
- **Runner**: A server that runs your workflows when they're triggered.

## Key Concepts and Components

### Events

Events are specific activities that trigger a workflow run. Common events include:

- `push`: When a commit is pushed to a repository branch
- `pull_request`: When a pull request is opened, synchronized, or closed
- `workflow_dispatch`: Manual trigger from the GitHub UI or API
- `schedule`: Workflow runs at specified times
- `repository_dispatch`: External API trigger for workflows
- `issues`: When an issue is opened, edited, deleted, etc.

### Workflows

A workflow is a configurable automated process made up of one or more jobs. It's defined in a YAML file in the `.github/workflows` directory of your repository.

Workflow files have several key sections:
- `name`: The name of the workflow (optional but recommended)
- `on`: The events that trigger the workflow
- `jobs`: The jobs that the workflow will execute

### Jobs

A job is a set of steps that execute on the same runner. Jobs can run independently or sequentially depending on conditions.

Key job configurations:
- `runs-on`: Specifies the type of runner to use
- `needs`: Specifies job dependencies (which jobs must complete first)
- `if`: Conditional execution based on expressions
- `strategy`: Define variations for the job (e.g., matrix)
- `steps`: The individual steps within the job

### Steps

Steps are individual tasks that can run commands, setup tasks, or run an action. Steps are executed in order and are dependent on each other.

Each step can:
- Run a script using `run` command
- Use an action with the `uses` keyword
- Have a `name` for display in the GitHub UI
- Have conditional execution with `if`
- Define environment variables with `env`

### Actions

Actions are reusable units of code that can be shared and imported into workflows. Actions can be:

- From the GitHub Marketplace
- From a public repository
- From a private repository (with some limitations)
- Defined locally in your repository

### Runners

Runners are the servers that execute your workflows. GitHub provides:

- **GitHub-hosted runners**: Virtual machines hosted by GitHub with common software preinstalled
  - Ubuntu Linux
  - Windows Server
  - macOS

- **Self-hosted runners**: Your own servers or VMs that you set up and manage

### Artifacts

Artifacts are files produced during a workflow run that can be stored and shared between jobs or downloaded after the workflow completes.

### Environments

Environments define protection rules and secrets for deployment targets like production, staging, and development.

## Your First Workflow

Let's create a simple workflow that runs whenever you push code to your repository. This workflow will check out your code and run a simple command.

### 1. Create the Workflow File

In your repository, create a new file at `.github/workflows/hello-world.yml`:

```yaml
name: Hello World Workflow

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
        
      - name: Say hello
        run: echo "Hello, GitHub Actions!"
        
      - name: Tell me about the environment
        run: |
          echo "The job is running on a ${{ runner.os }} server!"
          echo "The repository is ${{ github.repository }}"
          echo "The branch is ${{ github.ref }}"
```

### 2. Understand Each Section

- `name: Hello World Workflow`: The name that appears in the GitHub Actions UI
- `on: push, pull_request`: This workflow runs on push and pull request events to the main branch
- `jobs:`: The workflow contains one job called "say-hello"
- `runs-on: ubuntu-latest`: This job runs on the latest Ubuntu GitHub-hosted runner
- `steps:`: A list of steps for the job to execute

The steps in this job:
1. Check out your repository code using the `actions/checkout` action
2. Run a simple "Hello, GitHub Actions!" echo command
3. Print information about the environment using context expressions

### 3. View the Results

After committing this file to your repository:
1. Go to the "Actions" tab in your GitHub repository
2. You should see your "Hello World Workflow" listed
3. Click on a workflow run to see the details
4. Expand the "say-hello" job to see the output from each step

## Understanding YAML Syntax

GitHub Actions workflows are written in YAML, so understanding YAML basics is essential.

### Basic YAML Rules

- YAML is case-sensitive
- Indentation is significant and must use spaces (not tabs)
- Comments start with `#`
- Lists can be written as:
  ```yaml
  items:
    - item1
    - item2
  ```
- Key-value pairs are written as:
  ```yaml
  key: value
  ```
- Multi-line strings can be written using the pipe symbol:
  ```yaml
  description: |
    This is a multi-line
    string that preserves
    line breaks.
  ```

### Understanding Context and Expressions

GitHub Actions provides contextual information during workflow runs through expressions:

- Expressions are denoted by `${{ <expression> }}`
- Contexts include:
  - `github`: Information about the workflow run and event trigger
  - `env`: Environment variables
  - `job`: Information about the current job
  - `steps`: Outputs from previous steps in the job
  - `runner`: Information about the runner executing the job
  - `secrets`: Access to secrets defined in your repository
  - `strategy`: Information about the matrix strategy for the current job
  - `matrix`: Access to the matrix parameters defined in the workflow
  - `needs`: Outputs from jobs that are defined as a dependency

### Example Using Contexts

```yaml
name: Context Example

on: push

jobs:
  show-contexts:
    runs-on: ubuntu-latest
    steps:
      - name: Dump GitHub context
        env:
          GITHUB_CONTEXT: ${{ toJSON(github) }}
        run: echo "$GITHUB_CONTEXT"
        
      - name: Show specific context values
        run: |
          echo "Repository: ${{ github.repository }}"
          echo "Actor: ${{ github.actor }}"
          echo "SHA: ${{ github.sha }}"
          echo "Workflow name: ${{ github.workflow }}"
```

### Common YAML Mistakes to Avoid

1. **Improper Indentation**: Make sure your YAML is indented consistently with spaces
2. **Quotes for Special Characters**: Use quotes around values with special characters like colons
3. **Multi-line Scripts**: Use the pipe `|` symbol for multi-line scripts
4. **Boolean Values**: Use `true` and `false` (lowercase) for boolean values
5. **Expression Syntax**: Always use the full `${{ expression }}` syntax for expressions

## 🚀 Building Effective Workflows

## Workflow Syntax Reference

### Structure of a Workflow File

A complete workflow file typically includes:

```yaml
name: Workflow Name

on: [event1, event2]
  # or more detailed configuration:
  event1:
    types: [activity1, activity2]
    branches: [branch1, branch2]
    # other filters...

env:
  # Workflow-level environment variables
  GLOBAL_VAR: value

jobs:
  job-id:
    name: Job Display Name
    runs-on: ubuntu-latest
    needs: [other-job-id]
    if: github.event_name == 'push'
    environment: production
    
    env:
      # Job-level environment variables
      JOB_VAR: value
    
    strategy:
      matrix:
        node-version: [12.x, 14.x, 16.x]
    
    steps:
      - name: Step display name
        id: step-id
        uses: actions/action-name@version
        with:
          parameter1: value1
          parameter2: value2
        
      - name: Run command
        run: echo "Running a command"
        shell: bash
        env:
          # Step-level environment variables
          STEP_VAR: value
        
      - name: Use output from previous step
        run: echo "Previous step output: ${{ steps.step-id.outputs.output-name }}"
```

### Workflow Properties

#### `name`

The name of the workflow displayed in the GitHub Actions UI:

```yaml
name: Build and Test
```

#### `on`

Specifies which events trigger the workflow:

```yaml
# Simple event list
on: [push, pull_request]

# Detailed event configuration
on:
  push:
    branches: [main, dev]
    paths:
      - 'src/**'
      - '!**.md'
    tags:
      - 'v*'
  pull_request:
    types: [opened, synchronize]
    branches: [main]
  schedule:
    - cron: '0 0 * * *'  # Midnight every day
  workflow_dispatch:
    inputs:
      environment:
        description: 'Environment to deploy to'
        required: true
        default: 'dev'
        type: choice
        options:
        - dev
        - staging
        - prod
```

#### `env`

Define environment variables available to all jobs:

```yaml
env:
  NODE_ENV: production
  SERVER_URL: https://api.example.com
```

#### `defaults`

Set default configurations for all jobs or steps:

```yaml
defaults:
  run:
    shell: bash
    working-directory: ./app
```

#### `concurrency`

Ensure only one workflow using the same concurrency group runs at a time:

```yaml
concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true
```

#### `permissions`

Modify the default permissions granted to the `GITHUB_TOKEN`:

```yaml
# Restrict permissions to minimum necessary
permissions:
  contents: read
  issues: write
  pull-requests: write
```

### Job Properties

#### `runs-on`

Specifies the type of runner to use:

```yaml
# Single runner
runs-on: ubuntu-latest

# Multiple runners (for jobs that can run on any of these)
runs-on: [ubuntu-latest, windows-latest]
```

#### `needs`

Creates job dependencies:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    # build job definition...
    
  test:
    needs: build
    runs-on: ubuntu-latest
    # test job definition...
    
  deploy:
    needs: [build, test]
    runs-on: ubuntu-latest
    # deploy job definition...
```

#### `if`

Conditionally run a job:

```yaml
if: github.event_name == 'push' && github.ref == 'refs/heads/main'
```

#### `strategy`

Define a build matrix for running multiple job configurations:

```yaml
strategy:
  matrix:
    os: [ubuntu-latest, windows-latest, macos-latest]
    node-version: [14.x, 16.x, 18.x]
    include:
      - os: ubuntu-latest
        node-version: 18.x
        extra-param: special-value
    exclude:
      - os: windows-latest
        node-version: 14.x
  fail-fast: true
  max-parallel: 3
```

#### `environment`

Specify a GitHub environment for the job:

```yaml
environment:
  name: production
  url: ${{ steps.deploy.outputs.deployment-url }}
```

## Events and Triggers

Events determine when your workflows run. GitHub Actions supports a wide variety of events.

### Common Events

#### Push and Pull Request Events

```yaml
on:
  push:
    branches:
      - main
      - 'releases/**'
    paths:
      - '**.js'
      - '!docs/**'
    tags:
      - 'v*'
  pull_request:
    types: [opened, reopened, synchronize]
    branches:
      - main
```

#### Manual Events

```yaml
on:
  workflow_dispatch:
    inputs:
      environment:
        description: 'Environment to deploy to'
        required: true
        default: 'staging'
        type: choice
        options:
          - dev
          - staging
          - production
      debug:
        description: 'Enable debug mode'
        required: false
        type: boolean
        default: false
```

#### Scheduled Events

```yaml
on:
  schedule:
    # Runs at 00:00 UTC every day
    - cron: '0 0 * * *'
    # Runs at 15:30 UTC Monday through Friday
    - cron: '30 15 * * 1-5'
```

### Event Filtering

You can filter events based on various criteria:

#### Branch and Tag Filters

```yaml
on:
  push:
    # Branch filters
    branches:
      - main
      - 'releases/**'    # Matches any branch in the releases directory
      - '!releases/**-beta'  # Excludes branches ending with -beta
    
    # Tag filters  
    tags:
      - v1.*            # Matches v1.0, v1.1, etc.
      - 'v[0-9]+.[0-9]+.[0-9]+'  # Regex for semantic versioning
```

#### Path Filters

```yaml
on:
  push:
    paths:
      - 'src/**'        # Files in the src directory
      - '**.js'         # Any JavaScript file
      - 'package.json'  # The package.json file
      - '!**.md'        # Exclude markdown files
      - '!docs/**'      # Exclude the docs directory
```

### Repository Activity Events

GitHub Actions can be triggered by various repository activities:

```yaml
on:
  issues:
    types: [opened, edited, labeled]
  issue_comment:
    types: [created, edited]
  watch:
    types: [started]  # Triggers when someone stars your repository
  fork:
  release:
    types: [published, created, edited]
  discussion:
    types: [created, edited, answered]
```

### External Events

Trigger workflows from external events:

```yaml
on:
  repository_dispatch:
    types: [backend-deployed, api-updated]
```

To trigger this workflow, send a POST request to the GitHub API:

```bash
curl -X POST \
  https://api.github.com/repos/{owner}/{repo}/dispatches \
  -H "Accept: application/vnd.github.v3+json" \
  -H "Authorization: token $GITHUB_TOKEN" \
  -d '{"event_type": "backend-deployed", "client_payload": {"env": "production"}}'
```

## Jobs and Steps

### Step Configuration Options

Steps provide flexibility in how actions and commands are executed:

```yaml
steps:
  - name: Run a script
    id: script
    run: |
      echo "Running multi-line script"
      result=$(./my-script.sh)
      echo "result=$result" >> $GITHUB_OUTPUT
    shell: bash
    working-directory: ./scripts
    env:
      API_TOKEN: ${{ secrets.API_TOKEN }}
    with:
      script-param: value
    continue-on-error: true
    timeout-minutes: 5
    if: ${{ success() && github.event_name == 'push' }}
```

### Job Outputs

Jobs can produce outputs that can be used by other jobs:

```yaml
jobs:
  job1:
    runs-on: ubuntu-latest
    outputs:
      output1: ${{ steps.step1.outputs.test }}
      output2: ${{ steps.step2.outputs.test }}
    steps:
      - id: step1
        run: echo "test=hello" >> $GITHUB_OUTPUT
      - id: step2
        run: echo "test=world" >> $GITHUB_OUTPUT

  job2:
    needs: job1
    runs-on: ubuntu-latest
    steps:
      - run: echo ${{ needs.job1.outputs.output1 }} ${{ needs.job1.outputs.output2 }}
```

### Job Dependencies and Conditions

Control job execution order and conditions:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    # build job steps...

  test:
    needs: build
    if: ${{ success() && github.event_name == 'push' }}
    runs-on: ubuntu-latest
    # test job steps...

  deploy-staging:
    needs: [build, test]
    if: ${{ success() && github.ref == 'refs/heads/develop' }}
    runs-on: ubuntu-latest
    # deploy-staging job steps...

  deploy-production:
    needs: [deploy-staging]
    if: ${{ success() && github.ref == 'refs/heads/main' }}
    runs-on: ubuntu-latest
    # deploy-production job steps...
```

### Conditional Execution with Expressions

#### Using Functions

GitHub Actions provides several built-in functions for expressions:

```yaml
steps:
  - name: Conditional step
    if: ${{ success() && contains(github.event.head_commit.message, 'deploy') }}
    run: echo "Deploy triggered via commit message"

  - name: Check file existence
    id: check_file
    run: echo "exists=$(test -f .env && echo true || echo false)" >> $GITHUB_OUTPUT

  - name: Conditional on file existing
    if: ${{ steps.check_file.outputs.exists == 'true' }}
    run: echo "File exists"

  - name: Conditional on multiple criteria
    if: >-
      ${{ 
        success() && 
        (github.event_name == 'push' || github.event_name == 'workflow_dispatch') && 
        startsWith(github.ref, 'refs/tags/v')
      }}
    run: echo "This is a tagged release"
```

#### Available Functions

- `success()`: Returns true when all previous steps have succeeded
- `always()`: Always returns true, even when canceled or failures occur
- `cancelled()`: Returns true if the workflow was canceled
- `failure()`: Returns true when any previous step fails
- `contains(search, item)`: Returns true if search contains item
- `startsWith(searchString, searchValue)`: Returns true if searchString starts with searchValue
- `endsWith(searchString, searchValue)`: Returns true if searchString ends with searchValue
- `format(string, replaceValue0, replaceValue1, ...)`: Replaces values in string
- `join(array, separator)`: Joins array values with separator
- `toJSON(value)`: Returns a pretty-print JSON representation of value
- `fromJSON(value)`: Returns a JSON object or JSON data type from value

## Working with Runners

### GitHub-hosted Runners

GitHub provides different types of hosted runners:

```yaml
jobs:
  linux-job:
    runs-on: ubuntu-latest
    # or specific version: ubuntu-22.04, ubuntu-20.04
    
  windows-job:
    runs-on: windows-latest
    # or specific version: windows-2022, windows-2019
    
  mac-job:
    runs-on: macos-latest
    # or specific version: macos-12, macos-11
```

#### Runner Specifications

GitHub-hosted runners have specific hardware configurations:

- **Ubuntu**: 2-core CPU, 7 GB RAM, 14 GB SSD
- **Windows**: 2-core CPU, 7 GB RAM, 14 GB SSD
- **macOS**: 3-core CPU, 14 GB RAM, 14 GB SSD

For more resources, consider self-hosted runners.

#### Pre-installed Software

GitHub-hosted runners come with pre-installed software:

```yaml
steps:
  - name: Check Node.js version
    run: node --version

  - name: Check Python version
    run: python --version

  - name: List pre-installed software
    run: |
      npm --version
      java -version
      docker --version
      git --version
```

For a complete list of pre-installed software, see the [GitHub documentation](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners#preinstalled-software).

### Self-hosted Runners

For custom hardware, operating systems, or security needs, you can use self-hosted runners:

```yaml
jobs:
  deploy:
    runs-on: self-hosted
    # or with labels
    # runs-on: [self-hosted, linux, x64, gpu]
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
      - name: Deploy using local resources
        run: ./deploy.sh
```

#### Setting up Self-hosted Runners

1. In your GitHub repository or organization, go to Settings > Actions > Runners
2. Click "New runner" and follow the instructions for your platform
3. Configure the runner with labels to identify its capabilities

#### Using Runner Groups

For organizations, you can create runner groups to manage access to self-hosted runners:

1. Go to Organization Settings > Actions > Runners > New runner group
2. Assign runners to groups
3. Configure which repositories can access each group

## Using Actions

Actions are reusable units of code that can simplify your workflows.

### Using Marketplace Actions

```yaml
steps:
  # Use an action from the marketplace
  - name: Set up Node.js
    uses: actions/setup-node@v3
    with:
      node-version: '16'
      cache: 'npm'
      
  # Use a specific version (by tag)
  - name: Upload artifacts
    uses: actions/upload-artifact@v3.1.0
    with:
      name: build-files
      path: dist/
      
  # Use a specific commit SHA (for security)
  - name: Checkout repository
    uses: actions/checkout@a81bbbf8298c0fa03ea29cdc473d45769f953675
    with:
      fetch-depth: 0
```

### Actions from Public Repositories

```yaml
steps:
  # Use an action from a public repository
  - name: My Custom Action
    uses: username/repo-name@v1
```

### Local Actions

```yaml
steps:
  # Use an action from the same repository
  - name: Local Action
    uses: ./.github/actions/my-action
```

### Action Inputs and Outputs

Actions can accept inputs and produce outputs:

```yaml
steps:
  - name: Generate random number
    id: random
    uses: actions/github-script@v6
    with:
      script: |
        const random = Math.floor(Math.random() * 100);
        core.setOutput('number', random);

  - name: Use the output
    run: echo "Random number is ${{ steps.random.outputs.number }}"
```

## Managing Dependencies

Efficient dependency management is crucial for fast and reliable workflows.

### Caching Dependencies

```yaml
steps:
  - name: Checkout code
    uses: actions/checkout@v3

  - name: Set up Node.js
    uses: actions/setup-node@v3
    with:
      node-version: '16'
      cache: 'npm'
      
  # Manual cache configuration
  - name: Cache dependencies
    uses: actions/cache@v3
    with:
      path: |
        ~/.npm
        node_modules
      key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
      restore-keys: |
        ${{ runner.os }}-node-

  # Install dependencies
  - name: Install dependencies
    run: npm ci
```

### Artifact Management

Artifacts let you share data between jobs and store data after a workflow completes:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Build project
        run: npm run build
      
      # Upload build artifacts
      - name: Upload build artifacts
        uses: actions/upload-artifact@v3
        with:
          name: build-files
          path: |
            dist
            !dist/**/*.map
          retention-days: 5
  
  test:
    needs: build
    runs-on: ubuntu-latest
    steps:
      # Download artifacts from the build job
      - name: Download build artifacts
        uses: actions/download-artifact@v3
        with:
          name: build-files
          path: dist
          
      - name: List downloaded files
        run: ls -R dist
```

## 💼 Common Use Cases

This section covers common GitHub Actions use cases with practical examples.

## Continuous Integration

Continuous Integration (CI) is the practice of automatically integrating code changes from multiple contributors into a shared repository, with automated tests to catch problems early.

### Basic CI Workflow

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 16
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Lint code
      run: npm run lint
      
    - name: Build
      run: npm run build --if-present
      
    - name: Test
      run: npm test
```

### CI for Multiple Language Versions

```yaml
name: CI - Multiple Node.js Versions

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    
    strategy:
      matrix:
        node-version: [14.x, 16.x, 18.x]
        
    steps:
    - uses: actions/checkout@v3
    
    - name: Use Node.js ${{ matrix.node-version }}
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Run tests
      run: npm test
```

### CI with Multiple Operating Systems

```yaml
name: CI - Cross-platform

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ${{ matrix.os }}
    
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest, macos-latest]
        node-version: [16.x]
        
    steps:
    - uses: actions/checkout@v3
    
    - name: Use Node.js ${{ matrix.node-version }}
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Run tests
      run: npm test
      
    - name: Build
      run: npm run build
```

## Automated Testing

GitHub Actions is ideal for running tests automatically on each code change.

### Running Unit Tests

```yaml
name: Unit Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 16
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Run unit tests
      run: npm test
      
    - name: Generate test coverage report
      run: npm run test:coverage
      
    - name: Upload coverage report
      uses: actions/upload-artifact@v3
      with:
        name: coverage-report
        path: coverage/
```

### Running Integration Tests with Services

```yaml
name: Integration Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    
    # Set up service containers
    services:
      postgres:
        image: postgres:13
        env:
          POSTGRES_USER: testuser
          POSTGRES_PASSWORD: testpassword
          POSTGRES_DB: testdb
        ports:
          - 5432:5432
        # Set health checks to wait until postgres has started
        options: >-
          --health-cmd pg_isready
          --health-interval 10s
          --health-timeout 5s
          --health-retries 5
            
      redis:
        image: redis:6
        ports:
          - 6379:6379
        # Set health checks to wait until redis has started
        options: >-
          --health-cmd "redis-cli ping"
          --health-interval 10s
          --health-timeout 5s
          --health-retries 5
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 16
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Run integration tests
      run: npm run test:integration
      env:
        DATABASE_URL: postgres://testuser:testpassword@localhost:5432/testdb
        REDIS_URL: redis://localhost:6379
```

### End-to-End Testing with Cypress

```yaml
name: E2E Tests

on: [push, pull_request]

jobs:
  cypress-run:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout
      uses: actions/checkout@v3
      
    - name: Cypress.io
      uses: cypress-io/github-action@v4
      with:
        build: npm run build
        start: npm start
        wait-on: 'http://localhost:3000'
        browser: chrome
        headless: true
      env:
        NODE_ENV: test
        
    - name: Upload screenshots on failure
      uses: actions/upload-artifact@v3
      if: failure()
      with:
        name: cypress-screenshots
        path: cypress/screenshots
```

## Package Publishing

GitHub Actions can automate publishing packages to registries like npm, PyPI, or GitHub Packages.

### Publishing to npm

```yaml
name: Publish to npm

on:
  release:
    types: [created]

jobs:
  build-and-publish:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 16
        registry-url: 'https://registry.npmjs.org'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Build
      run: npm run build
      
    - name: Test
      run: npm test
      
    - name: Publish to npm
      run: npm publish
      env:
        NODE_AUTH_TOKEN: ${{ secrets.NPM_TOKEN }}
```

### Publishing to GitHub Packages

```yaml
name: Publish to GitHub Packages

on:
  release:
    types: [created]

jobs:
  build-and-publish:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 16
        registry-url: 'https://npm.pkg.github.com'
        scope: '@your-username'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Build
      run: npm run build
      
    - name: Publish to GitHub Packages
      run: npm publish
      env:
        NODE_AUTH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Publishing a Docker Image

```yaml
name: Publish Docker Image

on:
  push:
    tags:
      - 'v*'

jobs:
  build-and-push:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Docker Buildx
      uses: docker/setup-buildx-action@v2
      
    - name: Login to DockerHub
      uses: docker/login-action@v2
      with:
        username: ${{ secrets.DOCKER_USERNAME }}
        password: ${{ secrets.DOCKER_PASSWORD }}
        
    - name: Extract metadata
      id: meta
      uses: docker/metadata-action@v4
      with:
        images: username/app-name
        tags: |
          type=semver,pattern={{version}}
          type=semver,pattern={{major}}.{{minor}}
          
    - name: Build and push
      uses: docker/build-push-action@v3
      with:
        context: .
        push: true
        tags: ${{ steps.meta.outputs.tags }}
        labels: ${{ steps.meta.outputs.labels }}
```

## Deployment Automation

GitHub Actions can automate deployment to various hosting platforms.

### Deploy to AWS S3

```yaml
name: Deploy to S3

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 16
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Build
      run: npm run build
      
    - name
