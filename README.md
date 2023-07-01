# Github-Actions
The project consists of three parts.

The First part aims to demonstrate the ability to create functions and handle errors, as well as utilize an external library for advanced mathematical operations. Additionally, the project includes unit tests to ensure the correctness of the code.

Second part should handle the error when dividing by zero and include appropriate tests, including tests to verify the handling of this error. The application is also containerized using Docker, which facilitates its deployment and execution in different environments.

Third part:


## First part:
1. Creation of code that includes 4 functions (subtraction, multiplication, division) and a function that utilizes the numpy library - calculating the average from an array.
![2](https://github.com/Ulania/Github-Actions/assets/96245511/d6ffd276-f6b7-44e2-b764-8db3f216dfcc)

2. Along with the code execution, code from another library is also executed (calculating the average using numpy).

    The execution of code from another library is done using the import statement. In the code, using import logging, we import the logging library, which is used to log information at various levels of importance, such as DEBUG, INFO, WARNING, ERROR, CRITICAL. Inside the if name == 'main': block, we initialize logging using logging.basicConfig(level=logging.INFO), which means we will log only INFO level or higher information.
![3](https://github.com/Ulania/Github-Actions/assets/96245511/464a8e49-14f8-44fa-827d-9f7b8a8ae692)

3. For the division function, an error is handled when the denominator value is equal to 0 (the message "MIANOWNIK NIE MOŻE MIEĆ ZERA" is displayed).
For the division function, we handle the error by checking if the denominator value is equal to 0. If it is, a ValueError exception is raised with the appropriate message: "MIANOWNIK NIE MOŻE MIEĆ ZERA". This way, the function informs the user that the provided value is invalid, and it's not possible to perform the division operation.
![4](https://github.com/Ulania/Github-Actions/assets/96245511/03a58bba-4d7d-4a1f-ada9-529cf75924ba)

4. Unit tests for each function (for division, an additional Unitest is written to check if the appropriate error is returned).
![5](https://github.com/Ulania/Github-Actions/assets/96245511/995459db-941c-4fa1-a1d2-91e36879c1d0)

5. Execution of local tests to verify if they all pass.
![6](https://github.com/Ulania/Github-Actions/assets/96245511/f3f27648-1bf1-4078-9eee-37a0857e2bcd)

6. Building a Git action that, upon committing to the main/master branch, builds the environment and runs the tests.

    A main.yml file was created in the .github/workflows directory. It contains instructions for building the application, installing dependencies, running tests, or deploying the application.

    a) Defining a trigger that starts the workflow upon committing to the main branch.
![7](https://github.com/Ulania/Github-Actions/assets/96245511/86eb2f55-b92b-439d-9f1b-84a1013ab331)

    b) Configuring the environment in which the tests are executed.
![8](https://github.com/Ulania/Github-Actions/assets/96245511/8db2f669-1349-46d3-8d2c-334152d08f1a)

    c) Cloning the repository and fetching dependencies.
![9](https://github.com/Ulania/Github-Actions/assets/96245511/b02d06e9-3fd2-4b5f-b7d6-09872f85740c)

    d) Running the tests.
![10](https://github.com/Ulania/Github-Actions/assets/96245511/86d06562-01e0-4ce1-bd0d-0293c5225aa9)

    Upon committing to the main branch, it will be detected by the workflow, and then the environment will be built, and the tests described in the test script will be executed.
![11](https://github.com/Ulania/Github-Actions/assets/96245511/b734ae04-5875-4051-9c3f-245aa56aa7ad)
    ![12](https://github.com/Ulania/Github-Actions/assets/96245511/9a8ed849-d0ce-4d20-b2f1-1c3f7076b99e)



## Second part:
1. Created code that contains 3 functions (subtraction, multiplication, division) and they are attached to 3 different endpoints (e.g., api/add; api/sub).
![1](https://github.com/Ulania/Github-Actions/assets/96245511/50a40946-5ddd-4213-a688-f3a0639039be)

2. For the division function, an error is handled when the denominator value is equal to 0 (returning a bad request 400).
![2](https://github.com/Ulania/Github-Actions/assets/96245511/4ebccfa7-ed4f-4430-bfed-f147cea45005)

3. Tests for each endpoint.
![3](https://github.com/Ulania/Github-Actions/assets/96245511/af4659cc-5213-4734-b3bb-7a6e13ddc1fa)

    Created a Dockerfile that deploys the REST API application in a container (without tests).
![4](https://github.com/Ulania/Github-Actions/assets/96245511/22c71ad8-53db-4d79-8fe7-44c5ee738f98)

    ![5](https://github.com/Ulania/Github-Actions/assets/96245511/6c397ee3-09a3-4f0f-a03b-0f9058cfd559)

    ![6](https://github.com/Ulania/Github-Actions/assets/96245511/22cc1ac2-afa0-487b-b4fa-88cd4f7a4b30)

4. Ran tests locally to verify if all of them pass.
![7](https://github.com/Ulania/Github-Actions/assets/96245511/c8725ac6-e814-494a-b453-40d52b904622)

5. Built a Git action that, upon committing to the main/master branch:

- Sets up the test environment.
- Builds the image locally and runs the image with the REST API application.
- Runs tests related to sending requests to the REST API from the test environment (no additional Docker is built for tests).
![8](https://github.com/Ulania/Github-Actions/assets/96245511/a495cdd3-1ca4-4d98-ae6f-7e9260a6d5ff)



## Third part:
