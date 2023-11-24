# gpt-arxiv-fetcher

# Overview
This repository hosts the implementation of a GPT-based system designed to interact with the arXiv API to fetch the latest research papers. The project integrates an OpenAPI schema for seamless interaction with arXiv's services. This first project is inspired by https://github.com/daveshap weekly_arxiv.

## Features
- **ArXiv API Integration**: Utilizes the OpenAPI 3.0.0 specification to interact with arXiv's API, enabling users to fetch the latest research papers based on specific search criteria.
- **GPT-Powered Queries**: Custom GPT instructions are configured to trigger specific actions, enhancing user interaction with the system.

## Schema Details
The OpenAPI schema defines the structure for API requests and responses. Key components include:
- `search_query`: User-defined search term.
- `sortBy` and `sortOrder`: Parameters to sort the fetched results.
- `max_results`: Limits the number of results returned.

## Custom GPT Instructions and User Interaction
- **Trigger Command**: Typing `Arxiv!` in the GPT interface initiates the action.
- **User Prompt**: Upon receiving the `Arxiv!` command, the system will ask: 
  - _"Would you like me to search ArXiv for any recent development on this topic? Please specify the topic or search query."_
- **Command Execution**: Replace `<topic or search query here>` with the user's actual query and call the `export.arxiv.org` API using the `getArxivPapers` operation to fetch relevant papers.

## Usage
1. Configure your GPT instance with the OpenAPI schema.
2. Use the custom command `Arxiv!` followed by your search term.
3. The system will process your request and fetch results from arXiv.

## Prerequisites
- GPT setup capable of integrating with OpenAPI.
- Internet access for API calls.

## Installation
Provide instructions on how to set up and run your project.

## Contributing
Contributions to enhance or extend the project's capabilities are welcome. Please read `CONTRIBUTING.md` for details on our code of conduct and the process for submitting pull requests.

## License
This project is licensed under the [MIT License](LICENSE.md) - see the `LICENSE.md` file for details.

## Repository Structure

- `/docs`: Contains the documentation for custom GPT instructions (`CustomInstructions.md`) and the guide to create new actions (`ActionCreationGuide.md`).
- `/schemas`: Holds the OpenAPI schema for the arXiv API (`arXivAPISchema.yml`).
- `/src`: The source directory where the main application code (`main.py`) resides.
- `/tests`: Includes test scripts (`test_main.py`) to validate the application's functionality.
- `requirements.txt`: Lists all the dependencies required to run the project.
