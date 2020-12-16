# How To Export Code From Notebooks in nbdev
> API details.


The below cell doesn't get exported to any module and is hidden from the docs due to the `#hide` flag.

The below cell will export to `default_module.py`, because there is no argument to export and the default was set to `default_module` in the first cell.

The below cell will export to `module1.py` because the argument `module1` was passed to export.

The below cell will export to `module2.py` because the argument `module2` was passed to export.

To export code, first **make sure a notebook exists for each module.  If you don't do this, you will get an error.  The notebooks can be minimal like the ones demonstrated in this repository**

There are two choices for exporting notebooks:

1. run `nbdev_build_lib` from the command line.  
2. run `nbdev.export.notebook2script` in python:

```python
from nbdev.export import notebook2script
notebook2script()
```

    Converted index.ipynb.
    Converted module1.ipynb.
    Converted module2.ipynb.

