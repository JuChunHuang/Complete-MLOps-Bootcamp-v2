# Example Package

```
hello-world
└── hello_world
    ├── __init__.py
    └── main.py
```

# Virtual Environments

```bash
conda create -n hellodemo python=3.10
conda activate hellodemo
pip install setuptools twine
# this will create a dist folder with an installable package
python setup.py sdist
# create an account and an API token in test.pypi.org first to upload our package to the test server
twine upload --repository-url https://test.pypi.org/legacy/ \
  dist/hello_world_akjshya-0.0.1.tar.gz

pip install -i https://test.pypi.org/simple/ hello-world-akjshya==0.0.1

# another example
python setup.py sdist
twine upload --repository-url https://upload.pypi.org/legacy/ \
  dist/prediction_model_manifoldailearning-1.0.0.tar.gz
```