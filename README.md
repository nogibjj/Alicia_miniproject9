[![CI](https://github.com/AliciaXia222/IDS_706_miniproject_1/actions/workflows/cicd.yml/badge.svg)](https://github.com/AliciaXia222/IDS_706_miniproject_1/actions/workflows/cicd.yml)
# IDS_706_miniproject_1
This repository is only a test for Course IDS 706 miniproject1, "creating a template in github".
It incorporates various tools and libraries to support the development and deployment of data engineering projects. Below, we provide an overview of each feature included in this environment.

* 'Makefile'

It is a simple way to define and execute frequently used commands for automation. Here's a breakdown of what each target does:
    
    * 'Pytest': Pytest is a testing framework for Python. It allows you to write and run tests to ensure the correctness of your code. In data engineering, it's essential to validate the accuracy and reliability of your data pipelines and transformation processes.
    
    * 'Pylint': Pylint is a code linter for Python. It helps ensure your code adheres to coding standards and best practices, which is crucial for maintaining code quality in a collaborative environment.
   
    * 'test': This target runs your test suite using pytest. It provides verbose output (-vv), calculates code coverage (--cov=main), and specifies the coverage report generation directory (--cov=mylib). It's a good practice to ensure your code is tested thoroughly.
    
    * 'format': This target formats your Python code using black, a code formatter. Consistent code formatting enhances code readability and maintainability.
    
    * 'lint': This target performs code linting using pylint. It disables specific lint checks (--disable=R,C), ignores certain files (--ignore-patterns=test_.*?py *.py mylib/*.py), and checks for code quality and adherence to coding standards.
    
    * 'container-lint': This target runs hadolint, a Dockerfile linter, to check the quality and adherence to best practices of your Dockerfile.
    
    * 'refactor': This target combines the format and lint targets. It's a convenient way to ensure your code is well-formatted and linted before further actions.
   
    * 'deploy': This target is a placeholder for deployment-related actions. You can customize it to perform tasks like deploying your data engineering project to a production environment.
   
    * 'all': This target defines the default build process for your project. It specifies that when you run make all, it should execute the install, lint, test, format, and deploy targets in that order.

    ## To use this Makefile, 

        1. open your terminal
        2. navigate to your project directory
        3. run the desired command using make. 
            For example, I can install dependencies by running 'make install', run tests with 'make test', or format my code with 'make format'.

** Also I need make sure I have the required tools (pytest, black, pylint, hadolint, etc.) installed in my development environment to use this Makefile effectively.

* 'GitHub Actions'

    I set up workflows to automate tasks such as running tests, installing package, linting code, formatting code and deploying my data engineering projects. It helps ensure that code is continuously integrated and tested as I make changes with the 'cicd.yml' file.

* 'Dokerfile':
    I made this configuration well-suited for a data engineering or development environment where I need Python, Docker, GPU support (NVIDIA CUDA), Jupyter notebooks, and code linting/formating tools like Pylint, Black, and others. It also includes extensions for GitHub integration and Makefile support. Make sure to provide the necessary setup instructions and scripts in my "setup.sh" file to complete the environment setup.

Overall, this environment is aim to make data analytics workstream more efficient and automated.
