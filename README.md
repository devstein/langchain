# 🦜️🔗 LangChain

⚡ Building applications with LLMs through composability ⚡

[![lint](https://github.com/hwchase17/langchain/actions/workflows/lint.yml/badge.svg)](https://github.com/hwchase17/langchain/actions/workflows/lint.yml)
[![test](https://github.com/hwchase17/langchain/actions/workflows/test.yml/badge.svg)](https://github.com/hwchase17/langchain/actions/workflows/test.yml)
[![linkcheck](https://github.com/hwchase17/langchain/actions/workflows/linkcheck.yml/badge.svg)](https://github.com/hwchase17/langchain/actions/workflows/linkcheck.yml)
[![Downloads](https://static.pepy.tech/badge/langchain/month)](https://pepy.tech/project/langchain)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/langchainai.svg?style=social&label=Follow%20%40LangChainAI)](https://twitter.com/langchainai)
[![](https://dcbadge.vercel.app/api/server/6adMQxSpJS?compact=true&style=flat)](https://discord.gg/6adMQxSpJS)
[![Open in Dev Containers](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/hwchase17/langchain)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/hwchase17/langchain)
[![GitHub star chart](https://img.shields.io/github/stars/hwchase17/langchain?style=social)](https://star-history.com/#hwchase17/langchain)


Looking for the JS/TS version? Check out [LangChain.js](https://github.com/hwchase17/langchainjs).

**Production Support:** As you move your LangChains into production, we'd love to offer more comprehensive support.
Please fill out [this form](https://forms.gle/57d8AmXBYp8PP8tZA) and we'll set up a dedicated support Slack channel.

## Quick Install

`pip install langchain`
or
`conda install langchain -c conda-forge`

## 🤔 What is this?

Large language models (LLMs) are emerging as a transformative technology, enabling developers to build applications that they previously could not. However, using these LLMs in isolation is often insufficient for creating a truly powerful app - the real power comes when you can combine them with other sources of computation or knowledge.

This library aims to assist in the development of those types of applications. Common examples of these applications include:

**❓ Question Answering over specific documents**

- [Documentation](https://langchain.readthedocs.io/en/latest/use_cases/question_answering.html)
- End-to-end Example: [Question Answering over Notion Database](https://github.com/hwchase17/notion-qa)

**💬 Chatbots**

- [Documentation](https://langchain.readthedocs.io/en/latest/use_cases/chatbots.html)
- End-to-end Example: [Chat-LangChain](https://github.com/hwchase17/chat-langchain)

**🤖 Agents**

- [Documentation](https://langchain.readthedocs.io/en/latest/modules/agents.html)
- End-to-end Example: [GPT+WolframAlpha](https://huggingface.co/spaces/JavaFXpert/Chat-GPT-LangChain)

## 📖 Documentation

Please see [here](https://langchain.readthedocs.io/en/latest/?) for full documentation on:

- Getting started (installation, setting up the environment, simple examples)
- How-To examples (demos, integrations, helper functions)
- Reference (full API docs)
- Resources (high-level explanation of core concepts)

## 🚀 What can this help with?

There are six main areas that LangChain is designed to help with.
These are, in increasing order of complexity:

**📃 LLMs and Prompts:**

This includes prompt management, prompt optimization, a generic interface for all LLMs, and common utilities for working with LLMs.

**🔗 Chains:**

Chains go beyond a single LLM call and involve sequences of calls (whether to an LLM or a different utility). LangChain provides a standard interface for chains, lots of integrations with other tools, and end-to-end chains for common applications.

**📚 Data Augmented Generation:**

Data Augmented Generation involves specific types of chains that first interact with an external data source to fetch data for use in the generation step. Examples include summarization of long pieces of text and question/answering over specific data sources.

**🤖 Agents:**

Agents involve an LLM making decisions about which Actions to take, taking that Action, seeing an Observation, and repeating that until done. LangChain provides a standard interface for agents, a selection of agents to choose from, and examples of end-to-end agents.

**🧠 Memory:**

Memory refers to persisting state between calls of a chain/agent. LangChain provides a standard interface for memory, a collection of memory implementations, and examples of chains/agents that use memory.

**🧐 Evaluation:**

[BETA] Generative models are notoriously hard to evaluate with traditional metrics. One new way of evaluating them is using language models themselves to do the evaluation. LangChain provides some prompts/chains for assisting in this.

For more information on these concepts, please see our [full documentation](https://langchain.readthedocs.io/en/latest/).

## 💁 Contributing

As an open-source project in a rapidly developing field, we are extremely open to contributions, whether it be in the form of a new feature, improved infrastructure, or better documentation.

For detailed information on how to contribute, see [here](.github/CONTRIBUTING.md).


<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `root` directory is for configuring and setting up the LangChain project. It includes files and directories for building, testing, formatting, and linting the project, as well as documentation and configuration files for Docker, Poetry, and Read the Docs. It also includes directories for managing the development container, GitHub-related files, and testing the codebase. The `langchain` directory contains various modules and classes for building applications with LLMs through composability, while the `tests` directory is for testing the codebase.

### Files
#### .dockerignore
This file specifies files and directories that should be excluded from Docker builds and deployments.

#### .flake8
This file is the configuration file for Flake8, a Python linter. It specifies files and directories to exclude from linting, sets the maximum line length to 88 characters, and extends the list of ignored errors to include E203.

#### .gitignore
This file specifies files and directories that should be ignored by Git when tracking changes in the repository, including common files and directories that should not be committed, as well as integration test artifacts and specific files with certain attributes.

#### .readthedocs.yaml
This file is the configuration file for Read the Docs, a documentation hosting platform. It specifies the version of Python and other tools needed for building the documentation, as well as the location of the Sphinx configuration file. It also declares the Python requirements required to build the documentation.

#### CITATION.cff
This file contains citation information for LangChain, including the author's name, release date, and URL.

#### Dockerfile
This file is a Dockerfile for running unit tests. It defines the version of Poetry to install, creates a Python virtual environment for Poetry and installs it, sets the working directory for the app, installs the Poetry dependencies, and sets the entrypoint to run tests using Poetry.

#### Makefile
This file is a Makefile that provides commands for building, testing, formatting, and linting the codebase. It includes commands for generating code coverage reports, building and cleaning documentation, running tests, and running tests in a Docker container. Additionally, it provides commands for formatting the code and running linters.

#### poetry.toml
This file is the configuration file for Poetry, a dependency manager for Python. It includes settings for virtual environments and the installer.

#### pyproject.toml
This file (`pyproject.toml`) contains metadata about the project, including its name, version, description, license, and repository information, as well as a list of Python dependencies and their corresponding versions required for the project. It also includes scripts that can be run using the Poetry package manager, and various dependency groups such as docs, test, test_integration, lint, and typing, along with their respective dependencies. Additionally, it contains configuration settings for various tools used in the project such as Ruff, Mypy, and Coverage, and options for pytest such as registering custom markers and setting strict markers and durations.

### Directories
#### .devcontainer
The `.devcontainer` directory is for configuring and setting up a development container for the Langchain project. It includes a Dockerfile for creating the container, a devcontainer.json configuration file for specifying settings and customizations, and a docker-compose.yaml file for defining the container service and network.

#### .github
The `.github` directory is for managing the LangChain repository's GitHub-related files and directories. It includes files such as `CONTRIBUTING.md` and `PULL_REQUEST_TEMPLATE.md` that provide guidelines for contributing to the repository and creating pull requests. It also includes the `ISSUE_TEMPLATE` directory for storing issue templates, the `actions` directory for GitHub Actions related to the repository, and the `workflows` directory for automating various tasks such as testing and creating releases.

#### docs
The `docs` directory is for documenting the LangChain codebase. It includes files and subdirectories for building Sphinx documentation, providing an introduction to the framework, listing core modules, and documenting integrations, use cases, and additional resources. It also includes directories for working with different modules in the codebase, such as agents, chains, indexes, memory, models, prompts, and utilities, as well as documenting the installation and usage of LangChain's tracing feature.

#### langchain
The `langchain` directory is for building applications with LLMs through composability. It contains various modules and classes for handling chained inputs, caching, math utilities, document transformers, and formatting. Additionally, it includes subdirectories for creating and executing agents, implementing callback handlers, defining reusable components, and providing chat model classes. The directory also contains a Docker Compose configuration file for running the Langchain application locally and a directory for managing the Langchain CLI tool and its related configuration files. Other subdirectories include `client` for interacting with the LangChain+ API, `docstore` for implementing and providing different types of document stores, `embeddings` for implementing and providing wrappers for various embedding models, `evaluation` for evaluating and generating functionality related to language models, `experimental` for implementing and testing new features and functionalities, `graphs` for creating and manipulating graphs using NetworkX and Neo4j, `indexes` for creating and managing indexes for text data, `llms` for wrappers and implementations of various large language models APIs, `memory` for storing various classes and modules related to conversation memory, `output_parsers` for parsing the output of an LLM call into various formats, `prompts` for creating and formatting prompt templates for LLMs, `retrievers` for implementing various retrievers that retrieve relevant documents based on a query, and `tools` for providing a collection of tools for various tasks such as file management, web scraping, API operations, querying, and searching from different sources. Additionally, it includes the `utilities` directory for various utility classes and functions that provide wrappers and shims for various APIs and services, and the `vectorstores` directory for implementing various vector stores and their wrappers.

#### tests
The `tests` directory is for testing the `langchain` codebase. It includes instructions for running integration and unit tests, common test data, and entry points for all tests. The `integration_tests` directory is for testing the integration of the codebase with external APIs and services, while the `unit_tests` directory is for testing various modules and classes in the codebase. Additionally, the `mock_servers` directory is for implementing mock servers for testing purposes.

<!--- END SELFDOC --->