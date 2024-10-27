# CS50P Final Project - Flaskr (Simple Blog Project)

## Introduction

This project is a web-based blog application developed for the CS50P final project. It uses the Flask framework to allow users to create, edit, and delete blog posts with user authentication. This project showcases my learning in CS50P and Flask.

## Contributor

- Hein Htet San

## Course

- Edx: CS50 Python


## Project Structure

The project has the following structure:

```
flask_tuto/
├── flaskr/
│   ├── __init__.py
│   ├── auth.py
│   ├── blog.py
│   ├── db.py
│   ├── templates/
│   │   ├── auth/
│   │   │   ├── login.html
│   │   │   ├── register.html
│   │   ├── blog/
│   │   │   ├── create.html
│   │   │   ├── index.html
│   │   │   ├── update.html
│   ├── static/
│   │   ├── style.css
├── tests/
│   ├── test_auth.py
│   ├── test_blog.py
│   ├── test_db.py
├── venv/
├── pyproject.toml
├── README.md
```

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed Python 3.6 or later.
- You have a basic understanding of Python and Flask.
- You have installed `pip`, the Python package installer.

## Dependencies

The project relies on the following dependencies:

- **Flask**: A micro web framework for Python.
- **pytest**: A framework for testing Python code.

To install these dependencies, you can use the following command:

```sh
pip install -r requirements.txt
```

The `requirements.txt` file should include:

```
pytest
coverage
flask
pytest
```


## Run the Project

To run the project, follow these steps:

1. **Clone the repo**

    ```sh
    # clone the repo
    git clone https://github.com/Hein-HtetSan/cs50p-project.git  

    # change to project dir
    cd cs50p-project

    # create virtual env
    python -m venv .venv
    ```

2. **Activate the Virtual Environment**:
    Ensure you are in the project directory and activate the virtual environment:

    ```sh
    source venv/bin/activate  # On macOS/Linux
    .\venv\Scripts\activate   # On Windows
    ```

3. **Run the Flask Development Server**:
    Start the Flask development server:

    ```sh
    flask --app flaskr run --debug
    ```

    The application will be available at `http://127.0.0.1:5000/`.

4. **Don't forget to init the database**

    ```sh
    flask --app flaskr init-db
    # Initialized the database.
    ```

4. **Access the Application**:
    Open your web browser and navigate to `http://127.0.0.1:5000/` to access the blog application.

### **Included Routes**

For user auth
- http://localhost:5000/auth/register
- http://localhost:5000/auth/login
- http://localhost:5000/logout

For post
- http://localhost:5000/
- http://localhost:5000/create
- http://localhost:5000/id/update
- http://localhost:5000/delete



### Additional Commands

- **Initialize the Database**:
  If you need to initialize the database, run:

  ```sh
  flask init-db
  ```

- **Run in Debug Mode**:
  To run the application in debug mode, set the `FLASK_ENV` environment variable to `development`:

  ```sh
  export FLASK_ENV=development  # On macOS/Linux
  set FLASK_ENV=development     # On Windows
  ```

  Then, run the Flask development server as usual.



## Describe the Project

Create `pyproject.toml` file describes project and how to build it.

```
[project]
name="flaskr"
version="1.0.0"
description="The basic blog app built in the flask tutorial."
dependencies = [
    "flask",
]

[build-system]
requires = ['flit_core<4']
build-backend = "flit_core.buildapi"
```

## Install the project

`pip install -e .` tells pip to find `pyproject.toml` in the current directory and install the project in **editable or development** mode.

And then, you can observe that project is now installed with `pip list`.

#### Changes after installed the project
- Nothing changes from how you've been running your project so far. All running command are still working, **but you can call it from anywhere not just the from this directory**.


## Testing

To test the project, you can use the `pytest` framework. First, ensure `pytest` is installed:

```sh
pip install pytest
```

### Running Tests

To run the tests, simply execute:

```sh
pytest
```

This command will automatically find and run all the test files in the `tests` directory.

**Included Tests**

- **Authentication Tests**: Located in `test_auth.py`, these tests cover user authentication functionalities such as login, logout, and register

- **Blog Tests**: Located in `test_blog.py`, these tests cover blog-related functionalities such as creating, editing, and deleting posts.

- **Database Tests**: Located in `test_db.py`, these tests cover database-related functionalities to ensure the database operations are working correctly.

## References

- flask Doc
- Python Doc
- CS50 Python

**Copyright - 2024, Hein Htet Sna**