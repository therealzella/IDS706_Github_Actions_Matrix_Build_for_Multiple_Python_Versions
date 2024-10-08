# IDS706_Github_Actions_Matrix_Build_for_Multiple_Python_Versions

This repository is for the IDS706 course's assignment: IDS706_Github_Actions_Matrix_Build_for_Multiple_Python_Versions

![CI](https://github.com/therealzella/IDS706-python-github-template/actions/workflows/ci.yml/badge.svg)

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Testing](#testing)
- [CI/CD Documentation](#cicd-documentation)
- [Makefile Commands](#makefile-commands)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This repository is a Python project template designed for the IDS706 course. It includes:
- A `main.py` file with the core functionality.
- A `main_test.py` file with unit tests for the project.
- A `Makefile` for automating common tasks like formatting, linting, and testing.
- A `.gitignore` file to keep unnecessary files out of your repository.
- A `requirements.txt` file to manage dependencies.

## Installation
To set up this project locally, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/therealzella/IDS706-python-github-template.git
    ```

2. Navigate to the project directory:
    ```sh
    cd IDS706-python-github-template
    ```

3. Create a virtual environment (optional but recommended):
    ```sh
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

4. Install the required packages:
    ```sh
    make install
    ```

## Usage
You can run the main script using:
```sh
python main.py
```

## Testing
To run tests to validate changes, use the following command:
```sh
make test
```

## CI/CD Documentation
This project utilizes GitHub Actions for continuous integration and deployment, ensuring that all code pushed to the main branch is automatically tested across multiple Python versions. The CI/CD process includes:

  - ### Continuous Integration and Deployment
  - **CI/CD Process**: This project uses GitHub Actions for continuous integration. Our CI pipeline automatically runs on every push or pull request to the `main` branch.
  - **Matrix Strategy**: We test the project across multiple versions of Python (3.7, 3.8, and 3.9) to ensure compatibility and robustness across different environments.- **Workflow Steps**:
  - **Setup**: The workflow sets up the Python environment based on the matrix configuration.
  - **Dependency Installation**: Dependencies are installed using the requirements file.
  - **Linting**: Code is linted with flake8 to ensure it meets our coding standards.
  - **Testing**: Tests are executed using pytest to validate functionality.

- Automated Testing: On every push or pull request to the main branch, the CI pipeline runs linting, testing, and other checks defined in the ci.yml file.
- Steps Included in the Workflow:
  - Setup of the specified Python environment using actions/setup-python@v3.
  - Installation of dependencies via make install.
  - Linting with flake8 to maintain code quality.
  - Running unit tests with pytest.
