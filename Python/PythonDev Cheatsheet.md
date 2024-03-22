# Install an Editable Package

``` sh
#install:
pip install -e .

#uinstall:
pip uninstall my_package
```

This command tells pip to install the package in editable mode. It essentially creates a link from the site-packages directory to your package's source code. As a result, you can freely develop your package and test it across different projects on your system without having to reinstall it after each change.

