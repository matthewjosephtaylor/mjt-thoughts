# Git submodules are broken by design

They are too complex difficult and fragile to consider using for something as precious as source code.

I recommend avoiding them at all costs. I can't even imagine this insanity being used anywhere.

I note that even the linux kernel doesn't use submodules as far as I can tell: https://github.com/torvalds/linux

I discovered a nice pattern that works in their place:

- create/init a repo named 'lib' (name it whatever you want, I'm using this name as the example name)
- create directories and add code (modules) under the 'lib' directory
- add/commit from the root of the 'lib' repo via normal `git add .; git commit ...`
- AFTER the code is committed create/cd into a 'module' folder and init a new git repo as the 'module' repo (again name it whatever you want, this is just the example name)
  - IMPORTANT that the main lib has at least one file already added/committed to the 'lib' repo under the module directory, otherwise git will try to think of it as a submodule and provide you with lots of lovely scary warnings (which is _exactly_ what we are desperately trying to avoid)
- cd into the 'module' directory and do another `git add .; git commit ...`
  - this adds the files to the 'module' git repo which is _independent_ of th e 'lib' repo

From now one one can add/commit to either the 'lib' repo _or_ cd into the 'module' repo to add/commit there. These two repos now _share_ the same working tree as 99% of devs most likely would expect/want them to be shared, and are _independent_ which means that the code now lives in both places and can be managed independently as needed.

Now one can _clone_ the 'module's independently into various projects using the same 'order of git operations' trick, and push/pull modules AND push/pull the entire project (which will also contain the source code for the module)

