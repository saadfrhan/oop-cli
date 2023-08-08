# Node.js TypeScript CLI Template

This repository is a Node.js TypeScript template for creating CLI applications. It comes preconfigured with TypeScript, allowing you to write your code in a type-safe manner.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Publishing to NPM Registry](#publishing-to-npm-registry)
  - [Obtain NPM Token:](#obtain-npm-token)
  - [Obtain GitHub Token:](#obtain-github-token)
  - [Add Tokens as GitHub Repository Secrets:](#add-tokens-as-github-repository-secrets)
- [Project Structure](#project-structure)
- [Available Scripts](#available-scripts)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)
- [Author](#author)
- [Contact](#contact)

## Prerequisites

Make sure you have the following tools installed on your system:

- [Node.js](https://nodejs.org/en) (v18.x recommended)
- [pnpm](https://pnpm.io/) (Version 8 or later)

## Getting Started

To use this template, follow these steps:

1. Click on the "Use this template" button to create a new repository based on this template.
1. Clone your newly created repository to your local machine.
1. Install the project dependencies using pnpm:

```bash
pnpm install
```

1. Clear repository metadata using the following command:

```bash
pnpm clear-metadata
```

## Publishing to NPM Registry
The `.github\workflows\publish.yml` file makes use of two repository secrets to publish this package in the NPM registry: 
1) `secrets.GHP_TOKEN` 
2) `secrets.NPM_TOKEN`

### Obtain NPM Token:

1. Go to the NPM website (https://www.npmjs.com/) and sign in with your NPM account.
1. Click on your profile icon in the top right corner and select "Access Tokens" from the dropdown menu.
1. Click on the "Generate New Token" button, then click on "Classic Token".
1. Type the name for the Token select the "Publish" radio button, then press "Generate Token".
1. Copy the generated NPM token.

### Obtain GitHub Token:

1. Go to your GitHub account (https://github.com/) and sign in.
1. Click on your profile icon in the top right corner and select "Settings" from the dropdown menu (or the right-side sheet).
1. In the left sidebar, navigate to "Developer settings" > "Personal access tokens."
1. Click on "Tokens (classic)".
1. Click on "Generate new token" and then "Generate new token (classic)".
1. Enter something on the "Note" input, and specify the expiry time on the "Expiration" input.
1. Checkmark on `repo` and `write:packages`.
1. Click on "Generate token".
1. Copy the generated GitHub token.

### Add Tokens as GitHub Repository Secrets:

1. If you had cloned, forked or used this repository as a template, follow the next steps.
1. Click on the "Settings" tab in the repository menu.
1. In the left sidebar, click on "Secrets and variables".
1. Click on "Actions".
1. Click on the "New repository secret" button.
1. For NPM, set the secret name as `NPM_TOKEN` and paste the NPM token as the secret value.
1. Click "Add secret" to save the secret.
1. Go back.
1. Click on the "New repository secret" button.
1. For GitHub, set the secret name as `GHP_TOKEN` and paste the GitHub token as the secret value.
1. Click "Add secret" to save the secret.

## Project Structure
| File name | Description |
| :--------------------------------- | :----------------------------------------------------------------------------------------------------------------------------- |
| `├── .changeset`  _(directory)_    | Contains configuration files for versioning and managing changes in the project. |
| `　　├── config.json`              | Configuration file for changeset management. |
| `　　└── README.md`                | README file for the changeset directory, providing an overview of its purpose and usage. |
| `├── .github`  _(directory)_       | Contains GitHub-related files and workflows for automating tasks like linting, testing, and publishing. |
| `　　└── workflows`  _(directory)_ | GitHub Actions workflows for continuous integration and publishing tasks. |
| `　　　　├── main.yml`             | GitHub Actions workflow triggered on every push to run linting and building tasks. |
| `　　　　└── publish.yml`          | GitHub Actions workflow triggered on successful completion of the main workflow to handle the publishing process if necessary. |
| `├── src`  _(directory)_           | Contains the source code files for the CLI application. |
| `　　├── utils` _(directory)_      | Contains utility functions used in the application. |
| `　　　　└── beautifyName.ts`       | Utility function to beautify strings. |
| `　　├── index.ts`                 | Entry point of the CLI application. |
| `　　└── types.ts`                 | This file contains a TypeScript type for the inputQuestions array. |
| `├── .gitignore`                   | File specifying which files and directories should be ignored by Git version control. |
| `├── CHANGELOG.md`                 | File documenting the changes and updates made to the project over time. |
| `├── LICENSE`                      | The MIT license. |
| `├── package.json`                 | File defining the project's metadata and dependencies. |
| `├── pnpm-lock.yaml`               | File generated by the pnpm package manager, containing the dependencies and their versions. |
| `├── README.md`                    | Main README file providing an overview and instructions for using the CLI template. |
| `└── tsconfig.json`                | Configuration file for TypeScript, specifying compiler options and project settings.                                           |


## Available Scripts
- `pnpm start`: Builds the project and starts the CLI application.
- `pnpm build`: Compiles the TypeScript code to CommonJS (CJS) and ECMAScript modules (ESM) formats, and generates declaration files (d.ts).
- `pnpm lint`: Checks for TypeScript type errors and enforces strict type checking.
- `pnpm release`: Builts the project and then publishes changeset updates.
- `pnpm clear-metadata`: Use this command to clear repostory metadata and add your own values.

## Contributing
We welcome contributions! If you find any issues or have improvements to suggest, feel free to open a pull request.

## License
This project is licensed under the [MIT License](./LICENSE).

## Acknowledgments

This template is built using the following key dependencies:

- [TypeScript](https://www.typescriptlang.org): For adding static typing to JavaScript.
- [Tsup](https://github.com/egoist/tsup): For bundling TypeScript files.
- [Changesets](https://github.com/changesets/changesets): For managing version updates and changelogs.
- [Inquirer](https://github.com/SBoudrias/Inquirer.js): For interactive CLI prompts.

## Author

Saad Shamsi

## Contact

Contact
For any inquiries or questions, please reach out to me on [Twitter](https://x.com/SaadShamsi09).
