---
title: uv setup
tags: uv python setup notes
---

## UV Setup and Execution Steps

1.  **Create the virtual environment:**
    
    ```shell
    uv venv
    ```
    
    This creates a virtual environment named `.venv` in the current directory.

2.  **Install dependencies:**
    
    ```shell
    uv sync
    ```
    
    This installs all dependencies listed in `pyproject.toml` into the active virtual environment.

3.  **Install Playwright browser dependencies:**
    
    ```shell
    uv run playwright install
    ```
    
    This downloads the necessary browser binaries required by Playwright.

4.  **Run the sample application:**
    
    ```shell
    uv run python cli.py --computer local-playwright
    ```

    This executes the `cli.py` script within the `uv` managed environment, using the local Playwright browser.

## Example Runtimes

To run the provided examples using `uv`, execute the following commands from the project root:

Everything in the `examples/` folder requires special API keys to Scrapers

```shell
# Runs the local playwright version
uv run python simple_cua_loop.py

# Needs the docker container running
uv run python simple_cua_docker_loop.py
```