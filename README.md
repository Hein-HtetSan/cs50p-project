


### Describe the Project

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

### Install the project

`pip install -e .` tells pip to find `pyproject.toml` in the current directory and install the project in **editable or development** mode.

And then, you can observe that project is now installed with `pip list`.

#### Changes after installed the project
- Nothing changes from how you've been running your project so far. All running command are still working, **but you can call it from anywhere not just the from this directory**.

