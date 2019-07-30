### talkbox
---
https://github.com/cournape/talkbox
https://github.com/tkunic/TalkBox

https://github.com/joshuafleck/talkbox
https://github.com/cournape/talkbox/tree/master/scikits/talkbox

http://scikits.appspot.com/talkbox

```py 
// setup.py
import os
import sys

import setuptools
from numpy.distutils.core import setup

from common import *

def configuration(parent_package='', top_path=None, package_name=DISTNAME):
  if os.path.exists(): os.remove('MANIFEST')
  
  from numpy.distutils.misc_util import Configuration
  config = Configuration(None, parent_package, top_path,
    namespace_packages = ['scikits'])
    
  config.set_options(
    ignore_setup_xxx_py=True,
    assume_default_configuration=True,
    delegate_options_to_subpackages=True,
    quiet=True,
  )
  
  config.add_subpackage('scikits')
  config.add_subpackage(DISTNAME)
  config.add_data_files('scikits/__init__.py')
  
  return config
  
if __name__ == "__main__":
  setup(configuration = configuration,
    install_requires = 'numpy',
    packages = setuptools.find_packages(),
    include_package_data = True,
    name = DISTNAME,
    version = VERSION,
    description = DESCRIPTION,
    long_description = LONG_DESCRIPTION,
    license = LICENSE,
    #test_suite="tester",
    zip_safe = False,
    classifiers = CLASSIFIERS,
  )


```

```
```

```
```


