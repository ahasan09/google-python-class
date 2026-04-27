# Improvement Plan: google-python-class

## Overview
Python learning exercises from Google's Python Class. No dependencies, no tests, and no type annotations. Exercises reflect Python 2-era coding style in places.

## Improvements

### Modernization
- Audit all exercises for Python 2-style code (e.g., `print` statements, `unicode`/`str` confusion, old-style string formatting) and update to Python 3.13+ idiomatic style
- Replace `%` string formatting with f-strings throughout
- Add type hints to all function signatures

### Testing
- Add pytest tests for every exercise function — currently there is no automated way to verify solutions
- Place tests in a `tests/` folder mirroring the exercise structure
- Add a root `conftest.py` with any shared fixtures

### Code Quality
- Add `ruff` for linting and `black` for formatting
- Add a `pyproject.toml` with project metadata and tool configuration
- Add a `requirements-dev.txt` (or Poetry/uv group) for pytest, ruff, and black

### Documentation
- Add a docstring to each exercise function describing the expected inputs and outputs
- Add a root `README.md` with instructions for running exercises and tests

### DevOps
- Add GitHub Actions CI that runs `pytest` on every push
- Add a pre-commit config for `ruff` and `black`
