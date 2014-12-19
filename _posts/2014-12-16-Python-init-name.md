---
layout: post
title: "Python: meaning of __init__ and __main__"
description: "from my personal experience"
category: codes
tags: [tutorial, usage, python]
---
{% include JB/setup %}


### What does `if __name__ == “__main__” do`? 
[link](http://stackoverflow.com/questions/419163/what-does-if-name-main-do)

When the Python interpreter reads a source file, it executes all of the code found in it. Before executing the code, it will define a few special variables. For example, if the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value "__main__". If this file is being imported from another module, __name__ will be set to the module's name.
In the case of your script, let's assume that it's executing as the main function, e.g. you said something like  
`python threading_example.py`  
on the command line. After setting up the special variables, it will execute the import statement and load those modules. It will then evaluate the def block, creating a function object and creating a variable called myfunction that points to the function object. It will then read the if statement and see that __name__ does equal "__main__", so it will execute the block shown there.

One of the reasons for doing this is that sometimes you write a module (a .py file) where it can be executed directly. Alternatively, it can also be imported and used in another module. By doing the main check, you can have that code only execute when you want to run the module as a program and not have it execute when someone just wants to import your module and call your functions themselves.

### [What is `__init__.py` for?](http://stackoverflow.com/questions/448271/what-is-init-py-for)

Files name __init__.py are used to mark directories on disk as Python package directories. If you have the files

```  
mydir/spam/__init__.py   
mydir/spam/module.py  
```  

And mydir is on your path, you can import the code in module.py as  

```  
import spam.module  
or  
from spam import module  
``` 
   
If you remove the __init__.py file, Python will no longer look for submodules inside that directory, so attempts to import the module will fail.

The __init__.py file is usually empty, but can be used to export selected portions of the package under more convenient name, hold convenience functions, etc. Given the example above, the contents of the init module can be accessed as

  
