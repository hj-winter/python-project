# README of {{cookiecutter.project}}

This package was made by [{{cookiecutter.author}}](https://github.com/{{cookiecutter.author}})

{% if cookiecutter.license == "MIT" %}
This project is licensed under the [MIT License](LICENSE).
{% elif cookiecutter.license == "BSD" %}
This project is licensed under the [BSD License](LICENSE).
{% endif %}


## Template For Python Projects

This is a template for Python projects. What you get:

- Source code and test code is seperated in different directories.
- External libraries installed and managed by [Pip](https://pypi.org/project/pip/).
- Setup for tests using [Pytest](https://docs.pytest.org/en/stable/).
- Bechmark tests using [Pytest-Benchmark](https://github.com/ionelmc/pytest-benchmark)
- Continuous testing with [Github-Actions](https://github.com/features/actions/).
- Code coverage reports, including automatic upload to [Codecov](https://codecov.io).
- Code documentation with [Mkdocs](https://www.mkdocs.org/).
- Example of own Python package with the use of [Cython](https://cython.org/)
- Optional: Use of [VSCode](https://code.visualstudio.com/) with the Python and UnitTest extension.

## Structure

``` text
├── setup.py
├── setup.cfg
├── pyproject.toml
├── ... other config files ...
├── tests
│   ├── __init__.py
│   ├── test_vector.py
│   ├── test_computations.py
│   └── conftest.py
├── docs
│   ├── api.md
│   └── index.md
├── fastvector
│   ├── __init__.py
│   ├── vector.py
│   ├── dtypes.py
│   ├── version.py
│   └── cython_computations.pyx
│   └── computations.py
└── benchmarks
│   ├── __init__.py
│   └── test_computations.py
└── tests
    ├── __init__.py
    ├── test_computations.py
    └── test_vector.py
```

### Commands

```bash
# Build and Install (local)
pip install -e .
```

```bash
# Test
pytest tests
```

```bash
# Code Coverage
pytest --cov=fastvector tests --cov-report=html
```

```bash
# Benchmarks
pytest --benchmark-columns=min,max,mean,stddev --benchmark-sort=mean benchmarks
```
